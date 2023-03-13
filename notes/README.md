Todos:

- [ ] Base C compiler for boostrap
	- [ ] Zig C compiler ?
		- Pro: static ELF distribution
		- Pro: small size (24M)
		- Con: maybe bad support?
		- Usage: zig cc
	 - [x] GNU C Compiler
	 - [x] LLVM/Clang
- [ ] libc
	- [ ] musl?
		- Pro: less moving parts
		- con: compatibility?
```
../musl-1.2.3/configure --srcdir=../musl-1.2.3 --prefix=../out --disable-static

```

	- [x] gnu libc?
- [ ] Linker ?
	- [ ] Need to bootstrap it
	- [ ] Careful with host linker
	- [ ] Maybe mold? https://github.com/rui314/mold
	- [ ] `readelf -p .comment` check linker
	- [ ] `LD_DEBUG=all`
	- [ ] Check LSB for linker details
	- [ ] GNU batch loader has doc
	- [ ] No formal definition, but have to rely in the de-facto standards
- [ ] Library RUN_PATH
	- `readelf -d`
	- patchelf
- [ ] Bootstrap environment tools
	- [ ] `binutils` for:
		- `ar`
		- `readelf`
	- [ ] `posix shell` for `configure`
	- [ ] `coreutils` ?
	- [ ] `tar` ? - Handle in myq ?
	- [ ] `gnu make`
- [ ] Dhall for configuring pkgs
	- [ ] https://docs.dhall-lang.org/tutorials/Language-Tour.html
	- [ ] Con: dhall is limiting in some regards
- [ ] Json for configuring pkgs:
	- [ ] Pro: as simple as it gets
	- [ ] Pro: can use jsonschema infered from rust types
	- [ ] Con: very verbose to type, will need an iterpreted language to type it
- [ ] Isolation
	- [ ] Linux namespaces
		Varios tipos: https://man7.org/linux/man-pages/man7/namespaces.7.html
		- [ ] Mount 
		- [ ] etc...
		- [ ] User namespaces: https://man7.org/linux/man-pages/man7/user_namespaces.7.html
	- [ ] Seccomp?
	- [ ] Cgroups?

- [ ] Talk about FHS / LSB
- [ ] HTTP Client
	- [ ] reqwest:
		- [ ] Pro: rusttls for no dep on openssl