# 准备工作

如果您想玩一下 Go，您应该查看 Go Playground，它可以让您在线运行代码，而无需安装任何东西。这也是在 Go 的讨论论坛和 StackOverflow 等地方寻求帮助时共享 Go 代码的最常见方式。

安装 Go 非常简单。您可以从源代码安装它，但我建议您使用预编译的二进制文件之一。当您转到下载页面时，您将看到各种平台的安装程序。让我们避免这些并学习如何自己设置 Go。正如您将看到的，这并不难。

除了简单的示例之外，Go 设计为当您的代码位于工作区中时可以工作。工作空间是一个由 bin、pkg 和 src 子文件夹组成的文件夹。您可能会想强迫 Go 遵循您自己的风格 - 但不要这样做。

通常，我将项目放在 `~/code` 中。例如，`~/code/blog` 包含我的博客。对于 Go，我的工作空间是 `~/code/go`，我的 Go 支持的博客将位于 `~/code/go/src/blog`。

简而言之，在您希望放置项目的位置创建一个带有 src 子文件夹的 go 文件夹。

## OSX / Linux

下载适合您平台的 `tar.gz`。对于 OSX，您很可能对 `go#.#.#.darwin-amd64-osx10.8.tar.gz` 感兴趣，其中 `#.#.#` 是 Go 的最新版本。

通过 `tar -C /usr/local -xzf go#.#.#.darwin-amd64-osx10.8.tar.gz` 将文件解压到 `/usr/local`。

设置两个环境变量：

`GOPATH` 指向你的工作空间，对我来说，那就是 `$HOME/code/go`。
我们需要将 Go 的二进制文件附加到我们的 PATH 中。
您可以从 shell 进行设置：

```bash
echo 'export GOPATH=$HOME/code/go' >> $HOME/.profile
echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/code/go/bin' >> $HOME/.profile
```

您需要激活这些变量。您可以关闭并重新打开 shell，也可以运行 `source $HOME/.profile`。

输入 `go version`，您将有望获得类似于 `go version go1.3.3 darwin/amd64` 的输出。

## Windows

下载最新的 `zip` 文件。如果您使用的是 x64 系统，则需要 `go#.#.#.windows-amd64.zip`，其中 `#.#.#` 是 Go 的最新版本。

将其解压缩到您选择的位置。 `c:\Go` 是一个不错的选择。

设置两个环境变量：

GOPATH 指向您的工作空间。这可能类似于 `c:\users\goku\work\go`。
将 `c:\Go\bin` 添加到 PATH 环境变量。
可以通过系统控制面板的高级选项卡上的环境变量按钮设置环境变量。某些版本的 Windows 通过系统控制面板内的高级系统设置选项提供此控制面板。

打开命令提示符并输入 `go version`。您有望获得类似于 `go version go1.3.3 windows/amd64` 的输出。

## 链接

- [目录](directory.md)
- 上一章：[引言](introduction.md)
- 下一章：[第1章](1.0.md)
