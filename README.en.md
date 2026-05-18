# 🚀 rct — Rust Project Template

<p align="center">
  <b>A production-ready Rust project template with modern engineering best practices.</b>
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/rust-stable-orange" /></a>
  <a href="#"><img src="https://img.shields.io/badge/license-MIT-blue" /></a>
  <a href="#"><img src="https://img.shields.io/badge/build-passing-brightgreen" /></a>
  <a href="#"><img src="https://img.shields.io/badge/style-clippy%20%2B%20fmt-blue" /></a>
</p>

---

## 🌍 Language

* [中文版](./README.md) | English

---

## ✨ Overview

**rct** is a production-ready template designed to help you start Rust projects with solid engineering practices from
day one.

Instead of manually setting up tooling, rct provides a complete workflow covering:

* Code quality
* Dependency safety
* Versioning & changelog
* CI/CD workflows

No boilerplate setup. No repeated configuration. Just focus on building.

---

## ⚡ Features

### 🧱 Project Scaffolding

* One-command initialization via `cargo generate`
* Template variable system for customization

### 🔍 Code Quality

* `cargo clippy` + `cargo fmt`
* `typos` spell checking
* Includes baseline lint rules and a declared minimum Rust version

### 🔐 Dependency Safety

* `cargo-deny` for:

    * License compliance
    * Security advisories
    * Duplicate dependencies

### 📝 Versioning & Changelog

* `cargo-cliff` integration
* Conventional Commits support
* Semantic Versioning (SemVer)

### ⚙️ CI/CD Ready

* GitHub Actions ready structure
* Easy integration for build/test/release

### 🌐 Cross Platform

* Works on Windows / macOS / Linux

---

## 🚀 Quick Start

### 1. Install Requirements

```bash
# if you haven't install rust. run this command
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup update stable

# for generate
cargo install cargo-generate

# install dependencies
cargo install cargo-deny cargo-cliff typos-cli cargo-make cargo-nextest
```

---

### 2. Generate Project

```bash
cargo generate --git https://github.com/lhui-dev/rct --name my-app
```

---

### 3. Initialize

```bash
cd my-app
cargo build
```

### 4. Run validation pipeline

`cargo make do`

Run format → lint → test in one command

```bash
cargo make release
```

Run commit + changelog separately.

---

## 🧩 Task Pipeline (cargo-make)

Built-in automation powered by cargo-make.

**Run validation**

```bash
cargo make do

```

**Pipeline:** format → deny → typos → check → clippy → test

**Release:** commit → changelog

**Run individually**

```bash
cargo make format
cargo make clippy
cargo make test
```

## 🛠 Development Workflow

```bash
cargo build
cargo test
cargo fmt
cargo clippy -- -D warnings
```

---

## 📦 Versioning & Changelog

```bash
cargo version --bump 1.0.0
cargo cliff -o CHANGELOG.md --tag 1.0.0
```

---

## 🔍 Dependency Check

```bash
cargo deny check
```

---

## 📁 Project Structure

```
.
├── src/
├── .github/
├── Cargo.toml
├── deny.toml
├── cliff.toml
├── typos.toml
├── Makefile.toml
├── README.en.md
├── README.md
└── LICENSE
```

---

## ⚙️ Customization

Supports `cargo-generate.toml` for template variables such as `description`, `authors`, and `repository` in `Cargo.toml`.

After generating a project, update the repository URL in `cliff.toml` to match your own repository.

The template still keeps a fixed package name `rct` so the template repository itself remains buildable with `cargo check`. If you want the package name to be generated too, I can convert it into a pure template setup next.

---

## 🤝 Contributing

Contributions, issues and suggestions are welcome!

---

## 📄 License

MIT License

---

<p align="center">
  Made with ❤️ for Rust developers
</p>
