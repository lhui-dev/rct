# 🚀 rct — Rust 项目模板

<p align="center">
  <b>一个面向工程实践的 Rust 项目模板，内置现代开发最佳实践。</b>
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/rust-stable-orange" /></a>
  <a href="#"><img src="https://img.shields.io/badge/license-MIT-blue" /></a>
  <a href="#"><img src="https://img.shields.io/badge/build-passing-brightgreen" /></a>
  <a href="#"><img src="https://img.shields.io/badge/style-clippy%20%2B%20fmt-blue" /></a>
</p>

---

## 🌍 语言

* 中文 | [English](./README.en.md)

---

## ✨ 项目简介

**rct** 是一个开箱即用的 Rust 工程模板，帮助你从项目一开始就具备完善的工程化能力。

无需手动搭建工具链，rct 已内置完整开发流程，包括：

* 代码质量控制
* 依赖安全检查
* 版本管理与变更日志
* CI/CD 自动化支持

无需重复配置，专注业务开发。

---

## ⚡ 核心特性

### 🧱 项目初始化

* 基于 `cargo generate` 一键生成项目
* 支持模板变量替换，灵活定制项目结构

### 🔍 代码质量

* 集成 `cargo clippy` + `cargo fmt`
* `typos` 拼写检查

### 🔐 依赖安全

* 使用 `cargo-deny` 检查：

    * 许可证合规
    * 安全漏洞（advisories）
    * 重复依赖

### 📝 版本与日志管理

* 集成 `cargo-cliff`
* 支持 Conventional Commits
* 遵循语义化版本（SemVer）

### ⚙️ CI/CD 支持

* 预置 GitHub Actions 结构
* 可快速接入自动化构建 / 测试 / 发布

### 🌐 跨平台支持

* 支持 Windows / macOS / Linux

---

## 🚀 快速开始

### 1. 安装依赖

```bash
# 如果尚未安装 Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup update stable

# 项目生成工具
cargo install cargo-generate
pip install pre-commit

# 工程工具链
cargo install cargo-deny cargo-cliff typos-cli cargo-make cargo-nextest
```

---

### 2. 初始化项目

```bash
cargo generate --git https://github.com/lhui-dev/rct --name my-app
```

---

### 3. 项目初始化

```bash
cd my-app
pre-commit install
cargo build
```

---

### 4. 执行完整流程

```bash
cargo make do
```

一条命令完成：格式化 → 检查 → 测试 → 提交 → 生成 CHANGELOG

---

## 🧩 任务流水线（cargo-make）

内置基于 `cargo-make` 的自动化任务系统。

### 一键执行

```bash
cargo make do
```

### 执行流程

```
format → deny → typos → check → clippy → test → commit → cliff
```

### 单独执行任务

```bash
cargo make format
cargo make clippy
cargo make test
```

---

## 🛠 开发工作流

```bash
cargo build
cargo test
cargo fmt
cargo clippy -- -D warnings
```

---

## 📦 版本与日志

```bash
cargo version --bump 1.0.0
cargo cliff -o CHANGELOG.md --tag 1.0.0
```

---

## 🔍 依赖检查

```bash
cargo deny check
```

---

## 📁 项目结构

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

## ⚙️ 模板自定义

支持通过 `cargo-generate.toml` 定义模板变量，实现初始化时动态替换。

---

## 🤝 贡献

欢迎提交 Issue、PR 或建议，一起完善这个模板。

---

## 📄 许可证

MIT License

---

<p align="center">
  为 Rust 开发者打造 ❤️
</p>
