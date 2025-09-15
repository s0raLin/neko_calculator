# 喵喵计算器 - Tauri 版

一个基于 Tauri+HTML/CSS/JavaScript 的跨平台桌面计算器应用。  
轻量、安全、可在 **Windows / Linux / macOS** 上运行。

## 📂 项目结构
```bash
.
├── dist/                # 前端代码 (HTML/CSS/JS)
├── src-tauri/          # Tauri 配置和 Rust 后端
│   ├── Cargo.toml      # Rust 配置
│   ├── tauri.conf.json # Tauri 应用配置
└── README.md

```

---
## ✨ 功能

- 基本加减乘除计算
    
- 百分比运算
    
- 支持括号运算
    
- 美观可爱的 UI（喵喵风格）
    
- 跨平台支持
    
## 演示
![演示](./neko.webm)


---
## 📦 环境要求

在编译和运行本项目之前，请先准备以下环境：

- Rust（稳定版，建议使用 `rustup` 安装）
- Tauri CLI:
```bash
cargo install tauri-cli
```
### 各平台依赖

#### 🪟 Windows

- 需要 `Visual Studio Build Tools`
- 确保已安装 C++ 构建工具和 `Windows SDK`
#### 🐧Linux

- 安装依赖（以 Arch 为例）可自行查看[官网](https://tauri.app/zh-cn/start/prerequisites/)：
``` bash
sudo pacman -Syu
sudo pacman -S --needed \
  webkit2gtk-4.1 \
  base-devel \
  curl \
  wget \
  file \
  openssl \
  appmenu-gtk-module \
  libappindicator-gtk3 \
  librsvg \
  xdotool
```

#### 🍎 macOS

- 确保安装了 `Xcode`或 `Xcode Command Line Tools`

---
## 📦 构建打包


克隆项目并进入目录：
```bash
https://github.com/s0raLin/neko_calculator.git
cd neko_calculator
```
构建可执行文件（桌面应用）：
```bash
cargo tauri build
```
编译完成后，在以下目录找到应用安装包：
- Windows: `src-tauri/target/release/bundle/msi/`
- Linux: `src-tauri/target/release/bundle/deb/` 或 `AppImage`
- macOS: `src-tauri/target/release/bundle/dmg/`
