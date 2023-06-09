# 第一章：Rust 101

## 1. Rust简介


**欢迎来到Rust的世界！**

想象一下，你是一个宇航员，准备驾驶一艘太空船前往未知的星球。这艘太空船需要精准地工作，不能有任何错误，因为那可能会导致任务失败，甚至危及你的生命。编程就像驾驶这艘太空船，而Rust就像是你的太空船，它让你有信心可以安全、有效地抵达目的地。

Rust是一种系统编程语言，旨在提供内存安全，没有数据竞争，以及高性能。它的语法和特性使得你可以写出既安全又快速的代码，就像一个经验丰富的宇航员控制着太空船。

![Rust Logo](https://www.rust-lang.org/static/images/rust-logo-blk.svg)

**Rust的优点**

- **内存安全**：Rust的所有权系统和借用检查器确保了内存安全，不必担心像空指针解引用或者数据竞争等问题，让你的太空船不会在半路爆炸。

- **零成本抽象**：在Rust中，你可以使用高级抽象，而不会牺牲性能。你的太空船可以使用最先进的导航系统，而不会减慢速度。

- **并发无忧**：Rust的语言特性让并发编程变得更加简单、安全。就像你可以信任你的太空船会正确处理所有并发的任务，不会让任何一个重要的系统出现问题。

- **C-Linkable**：Rust可以轻松与C和其他语言进行交互，使其非常适合系统编程。你的太空船可以与其他船队进行无缝通信。

现在，你可能已经迫不及待想要开始你的Rust之旅了。放心，我们将一步步带你了解Rust，让你能够自信地驾驶你的"太空船"前往未知的"星球"。让我们开始吧！

## 2. 安装和设置Rust环境


**第一步：下载和安装Rust**

在你开始编写Rust程序之前，你需要在你的计算机上安装Rust编译器。幸运的是，Rust提供了一个非常方便的脚本`rustup`，这个脚本会帮你处理所有的安装细节。你只需要打开终端，然后输入以下命令：

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

然后按照提示进行操作。默认选项通常是最好的选择，除非你有特殊的需求。

安装完成后，关闭并重新打开你的终端，然后输入：

```bash
rustc --version
```

如果你看到了类似于`rustc 1.52.1 (9bc8c42bb 2021-05-09)`的输出，恭喜你，Rust已经成功安装了！

**第二步：了解Cargo**

Cargo是Rust的构建系统和包管理器。安装Rust时，Cargo也会被自动安装。你可以通过输入以下命令来检查Cargo是否已经被安装：

```bash
cargo --version
```

如果你看到了类似于`cargo 1.52.0 (69767412a 2021-04-21)`的输出，那么Cargo已经准备就绪。

Cargo有许多强大的功能。它可以帮助你创建、构建、测试和分享你的Rust程序。你会在接下来的章节中更深入地了解Cargo。

**第三步：创建你的第一个Rust程序**

让我们使用Cargo来创建你的第一个Rust程序。在终端中，导航到你想要创建项目的目录，然后输入：

```bash
cargo new hello_rust
```

这个命令会创建一个名为`hello_rust`的新目录，并在其中初始化一个新的Rust项目。现在，让我们导航到这个新的目录：

```bash
cd hello_rust
```

在`hello_rust`目录中，你会发现一个`src`目录和一个名为`Cargo.toml`的文件。`src`目录包含你的源代码，而`Cargo.toml`则是Cargo的配置文件。

让我们看看`src/main.rs`文件，这是你的主程序文件。它应该看起来像这样：

```rust
fn main() {
    println!("Hello, world!");
}
```

这就是你的第一个Rust程序。要运行它，你只需要在终端中输入：

```bash
cargo run
```

你应该会看到`Hello, world!`被打印在终端中。恭喜你，你已经成功编写并运行了

你的第一个Rust程序！

现在你已经准备好开始你的Rust编程之旅了。记住，学习是一个过程，不要急于求成。你已经迈出了第一步，只需要继续前进，你一定能够掌握Rust。祝你学习愉快！


## 3. Hello, Rust! 第一个Rust程序

**欢迎来到你的第一个Rust程序**

当你成功安装和设置了Rust环境后，最好的开始方式就是编写和运行一个简单的程序。在编程世界中，这个传统通常是打印"Hello, World!"。

让我们看看如何在Rust中完成这个任务。

首先，你需要创建一个新的Rust文件。让我们将它命名为`main.rs`。这个`main`表示这是我们程序的主入口点，`.rs`扩展名表示这是一个Rust文件。

在你的`main.rs`文件中，写入以下代码：

```rust
fn main() {
    println!("Hello, Rust!");
}
```

现在，让我们一步步分解这段代码：

- `fn main() { ... }`: 这是Rust程序的主函数。当你的程序开始运行时，`main`函数是第一个被调用的。`fn`关键字用于声明一个新的函数，`main`是我们的函数名，`()`表示这个函数不接受任何参数，`{}`中间是函数的主体。

- `println!("Hello, Rust!");`: 这是一个宏调用，用于在控制台输出文本。`println!`是Rust的内置打印行宏，它会将传入的字符串参数打印到控制台，并在末尾添加一个新行。注意`println!`后面的`!`，它表明这是一个宏而不是一个普通的函数。`"Hello, Rust!"`是一个字符串字面量，我们将它传递给`println!`宏来打印。

要运行你的Rust程序，打开终端，导航到`main.rs`文件所在的目录，然后输入`cargo run`命令。你应该会看到"Hello, Rust!"被打印在终端中。

恭喜你，你已经编写并运行了你的第一个Rust程序！

在接下来的章节中，我们将更深入地学习Rust的语法和特性。记住，编程就像建筑一座大楼，你需要一块块砖头（或者一行行代码）来逐步构建。只要你持之以恒，你一定可以成为一个优秀的Rust开发者！祝你好运！
