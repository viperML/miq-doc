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

- [ ] Talk about FHS / LSB