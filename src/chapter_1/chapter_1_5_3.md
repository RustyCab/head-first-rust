# 安装过程：Windows, macOS, Linux

### Windows

1. **运行安装程序**：找到你下载的 `rustup-init.exe` 文件，然后双击运行。如果看到 Windows 的安全警告，点击 "运行" 继续。

2. **安装 Rust**：在弹出的命令行窗口中，会出现一些关于 Rust 安装的提示，按回车键接受默认设置即可。安装过程可能需要几分钟的时间。

3. **验证安装**：当安装完成后，关闭命令行窗口，然后打开一个新的命令行窗口（或 PowerShell 窗口），输入 `rustc --version`，如果看到 Rust 的版本信息，那么说明你已经成功安装了 Rust。

### macOS 和 Linux

1. **打开终端**：在 macOS 中，你可以通过 Spotlight 搜索 "Terminal" 打开终端；在 Linux 中，你可以通过按下 `Ctrl+Alt+T` 打开终端。

2. **运行安装脚本**：在终端中，输入以下命令来运行你下载的 `rustup-init.sh` 文件：

   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

   安装脚本会自动下载并安装最新的 Rust 稳定版，以及其相关的工具，如 `cargo`（Rust 的包管理器和构建工具）。

3. **验证安装**：当安装完成后，关闭终端窗口，然后打开一个新的终端窗口，输入 `rustc --version`，如果看到 Rust 的版本信息，那么说明你已经成功安装了 Rust。

请注意，以上步骤可能会因你的网络环境、操作系统版本或 Rust 官网的更新而略有不同。如果你在安装过程中遇到问题，你可以访问 Rust 官网的 FAQ 页面或者 Rust 社区寻求帮助。
