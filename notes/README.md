
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
	- [x] gnu libc?
- [ ] Bootstrap environment tools
	- [ ] `binutils` for:
		- `ar`
		- `readelf`
	- [ ] `posix shell` for `configure`
	- [ ] `coreutils` ?
	- [ ] `tar` ? - Handle in myq ?
- [ ] Library RUN_PATH
	- `readelf -d`
	- patchelf