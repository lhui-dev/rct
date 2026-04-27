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

* `pre-commit` hooks
* `cargo clippy` + `cargo fmt`
* `typos` spell checking

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
pip install pre-commit

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
pre-commit install
cargo build
```

### 4. Run full pipeline

`cargo make do`

Run format → lint → test → commit → changelog in one command

---

## 🧩 Task Pipeline (cargo-make)

Built-in automation powered by cargo-make.

**Run everything**

```bash
cargo make do

```

**Pipeline:** format → deny → typos → check → clippy → test → commit → cliff

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
├── .pre-commit-config.yaml
├── README.en.md
├── README.md
└── LICENSE
```

---

## ⚙️ Customization

Supports `cargo-generate.toml` for template variables.

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
