title = "Install Spin"
template = "spin_main"
date = "2022-03-14T00:22:56Z"
enable_shortcodes = true
[extra]
keywords = "install"

---

## Installing Spin

Spin runs on Linux (amd64), macOS (Intel and Apple Silicon) and Windows with WSL2 (amd64).

There are multiple ways to install Spin. The easiest is to use the installer script, hosted on this site.

This command will install the latest version of Spin in you current directory.
{{ tabs "Os" }}

{{ startTab "Windows"}}

To list files on windows use `dir`

<!-- @selectiveCpy -->

```bash
$ dir hello_fermyon
```
and script in windows have the extension `.bat`

<!-- @nocpy -->

```bash
hello.bat
test.bat
```

{{ blockEnd }}

{{ startTab "Linux"}}

To list files on linux use `ls`

<!-- @selectiveCpy -->

```bash
$ ls
```

and script in windows have the extension `.sh`

<!-- @nocpy -->

```bash
hello.sh
test.sh
```

{{ blockEnd }}
{{ blockEnd }}

Now with some code examples

{{ tabs "code" }}
{{ startTab "Rust" }}

```rust
println!("hello fermyon");
```

{{ blockEnd }}

{{ startTab "Python" }}

```python
print("hello fermyon");
```

{{ blockEnd }}

{{ startTab "Javascript" }}

```javascript
console.log("hello fermyon")
```

{{ blockEnd }}
{{ blockEnd }}


## Linux: Additional Libraries

On a fresh Linux installation, you will also need the standard build toolchain
(`gcc`, `make`, etc.), the SSL library headers, and on some distributions you may need `pkg-config`.

On Debian-like distributions, including Ubuntu, you can install these with a command like this:

{{ tabs "os" }}

{{ startTab "Windows"}}

To list files on windows use `dir`

<!-- @selectiveCpy -->

```bash
$ dir hello_fermyon
```
and script in windows have the extension `.bat`

<!-- @nocpy -->

```bash
hello.bat
test.bat
```

{{ blockEnd }}

{{ startTab "Linux"}}

To list files on linux use `ls`

<!-- @selectiveCpy -->

```bash
$ ls
```

and script in windows have the extension `.sh`

<!-- @nocpy -->

```bash
hello.sh
test.sh
```

{{ blockEnd }}
{{ blockEnd }}

{{ tabs "code" }}
{{ startTab "Rust" }}

```rust
println!("hello fermyon");
```

{{ blockEnd }}

{{ startTab "Python" }}

```python
print("hello fermyon");
```

{{ blockEnd }}

{{ startTab "Javascript" }}

```javascript
console.log("hello fermyon")
```

{{ blockEnd }}
{{ blockEnd }}

## Installing a specific version of Spin

To install a specific version, you can pass arguments to the install script this way:

<!-- @selectiveCpy -->

```bash
$ curl -fsSL https://developer.fermyon.com/downloads/install.sh | bash -s -- -v v0.6.0
```

To install canary version of spin, you should pass the argument `-v canary`. The canary version is always the latest commit to the main branch of Spin.

<!-- @selectiveCpy -->

```bash
$ curl -fsSL https://developer.fermyon.com/downloads/install.sh | bash -s -- -v canary
```

## Building Spin from source

[Follow the contribution document](./contributing.md) for a detailed guide on building Spin from source:

<!-- @selectiveCpy -->

```bash
$ git clone https://github.com/fermyon/spin
$ cd spin && make build
$ ./target/release/spin --help
```



## Using Cargo to install Spin

If you have [`cargo`](https://doc.rust-lang.org/cargo/getting-started/installation.html), you can clone the repo and install it to your path:

<!-- @selectiveCpy -->

```bash
$ git clone https://github.com/fermyon/spin -b v0.6.0
$ cd spin
$ rustup target add wasm32-wasi
$ cargo install --locked --path .
$ spin --help
```

## Next Steps

- [Take Spin for a spin](./quickstart.md)
- Learn about how to [develop a Spin application](developing)
- Try the [Fermyon Cloud](/cloud/quickstart)
