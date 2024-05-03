---
layout: page
title: Lab 0 Setup, Setting Up Your Computer
permalink: /Lab00/
nav_order: 2
parent: L01 Intro, Hello World Java

---

# 实验0 设置：设置您的计算机

---

我们鼓励您在开始Lab 1 之前尽可能多地完成此设置。如果您遇到困难，请前往办公时间或实验室寻求帮助。

## A. 安装文本编辑器（可选）

如果您还没有首选的文本编辑器，我们推荐安装一个。

目前最受欢迎的三种 GUI 文本编辑器似乎是：

1. Sublime Text（免费，但会不断提醒您付费）：<https://www.sublimetext.com/>
2. Atom（免费）：<https://atom.io/>
3. Visual Studio Code（免费）：<https://code.visualstudio.com/>

请查看[此文本编辑器评测](https://www.techradar.com/best/best-text-editors)以更深入了解这些及其他文本编辑器。

选择哪个并不十分重要，因为我们在课程中只会偶尔使用文本编辑器。大多数时间我们将使用称为 IDE 的其他东西。

您不必选择上述三个选项中的一个。您可以完全使用不同的文本编辑器（内置文本编辑器、vim、emacs 等）。

## B. 配置您的计算机

根据您的操作系统，我们需要做一些设置以为 61B 课程配置您的计算机。

具体步骤取决于您的操作系统。

- [Windows 指南](https://sp21.datastructur.es/materials/lab/lab1setup/windows.html) [[视频演示](https://youtu.be/xEO4SOjmUOw)]
- [macOS 指南](https://sp21.datastructur.es/materials/lab/lab1setup/mac.html)
- [Linux 指南](https://sp21.datastructur.es/materials/lab/lab1setup/linux.html)

只有在您已完成上述针对您操作系统的指南后，才继续下一部分。在 Windows 上的高级用户也可以使用新的 Bash for Windows 功能，但我们不会提供官方指导。请注意，如果您使用 Bash for Windows，您需要安装两次 Java（一次在 Bash for Windows 中，一次在 Windows 本身中，按照上述指南操作）。

## C. 学习使用终端（可选）

如果您已经知道如何打开和使用终端，请跳过此部分。

终端是一个应用程序，允许您运行各种程序以及在您的计算机中操作文件。它是一个强大但也危险的工具，因此在使用一些命令时请小心。在类 Unix 操作系统上，终端应用程序将为您提供所需的一切。例如，在 macOS 上，您可以使用 Spotlight 搜索终端应用程序。

以下是一些您可能在本课程中发现有用的重要命令：

- `cd
  `: 更改您的工作目录

  ```bash
    cd hw
  ```

  此命令将把您的目录更改为 `hw`。

- `pwd
  `: 当前工作目录

  ```bash
    pwd
  ```

  如果您不确定自己在哪里，此命令会告诉您当前目录的完整绝对路径。

- `.
  `: 代表您当前的目录

  ```bash
    cd .
  ```

  此命令将把您的目录更改为当前目录（即什么也不做）。

- `..
  `: 代表您当前目录的上一级目录

  ```bash
    cd ..
  ```

  此命令将把您的目录更改为其父目录。如果您在 /workspace/day1/ 中，该命令会将您放在 /workspace/。

- `ls
  `: 列出目录中的文件/文件夹

  ```bash
    ls
  ```

  此命令将列出您当前目录中的所有文件和文件夹。

  ```bash
    ls -l
  ```

  此命令将列出您当前目录中的所有文件和文件夹，并带有时间戳和文件权限。这可以帮助您双重检查您的文件是否正确更新或更改文件的读写执行权限。

- `mkdir
  `: 创建一个目录

  ```bash
    mkdir dirname
  ```

  此命令将在当前目录中创建一个名为 `dirname` 的目录。

- `rm
  `: 删除一个文件

  ```bash
    rm file1
  ```

  此命令将从当前目录中删除 `file1`。如果 `file1` 不存在，则不会起作用。

  ```bash
    rm -r dir1
  ```

  此命令将递归删除 `dir1` 目录。换句话说，它将删除 `dir1` 内的所有文件和目录，以及 `dir1` 本身。请小心使用此命令！

- `cp
  `: 复制一个文件

  ```bash
    cp lab1/original lab2/duplicate
  ```

  此命令将复制 `lab1` 目录中的 `original` 文件，并在 `lab2` 目录中创建一个 `duplicate` 文件。

- `mv
  `: 移动或重命名一个文件

  ```bash
    mv lab1/original lab2/original
  ```

  此命令将 `original` 从 `lab1` 移动到 `lab2`。与 `cp` 不同，`mv` 不会在 `lab1` 目录中保留原文件。

  ```bash
    mv lab1/original lab1/newname
  ```

  此命令不会移动文件，而是将其从 `original` 重命名为 `newname`。

当在命令行上导航时，还有一些其他有用的技巧：

- 您的 shell 可以通过 *tab 补全* 为您完成文件名和目录名。当您有一个不完整的名称（对于已经存在的东西）时，尝试按 `tab` 键进行自动完成或显示可能的名称列表。
- 如果您想重新键入最近使用过的指令，请按键盘上的 `up` 键，直到看到正确的指令。如果您在执行重复指令时，这可以节省键入时间。

## D. 测试您在步骤 B 中的设置

让我们确保一切正常运行。

1. 首先打开您的终端。检查 git 是否为已识别命令，通过键入以下命令：

   ```bash
    git --version
   ```

   应该打印出 git 的版本号。如果您看到“git: command not found”或类似的，尝试打开一个新的终端窗口，重启您的计算机，或重新安装 Git。

2. 其次，让我们检查 `javac` 和 `java` 是否工作。`javac` 和 `java` 允许 *命令行编译*，换句话说，就是能够直接从命令行运行 Java 程序。在实践中，大多数开发人员通过像 IntelliJ 这样的 IDE 运行 Java 程序，因此除了测试您的设置外，我们本学期不会太多使用命令行编译。首先，在您的终端运行以下命令：

   ```bash
    mkdir ~/temp
    cd ~/temp
   ```

   1. 然后，在此目录中打开您操作系统的文件资源管理器。您可以通过命令行做到这一点：

      - Mac：`open .`
      - Windows：`explorer .`
      - Ubuntu：`gnome-open .`
      - Linux Mint：`xdg-open .` 或 `mate .`

   2. 在这个新打开的目录中，创建

一个名为 `HelloWorld.java` 的文件，其内容如下：

```java
 public class HelloWorld {
     public static void main(String[] args) {
         System.out.println("Hello world!");
     }
 }
```

   3. 在您的终端中输入 `ls`（列出此目录中的文件/文件夹）。您应该看到列出的 `HelloWorld.java`。

   4. 运行 `javac HelloWorld.java`。如果这产生了任何输出，则您的设置可能有问题。尝试打开一个新的终端窗口或重启您的计算机。如果仍然不起作用，请查看针对您操作系统的指南下的故障排除部分。

   5. 键入 `ls`，您应该看到 `HelloWorld.java` 和新创建的 `HelloWorld.class`（`javac` 命令创建了这个文件）。

   6. 运行 `java HelloWorld`。它应该为您打印出“Hello world!”。如果没有，您的设置出了问题！

   7. 您完成了！您也可以随意删除“temp”文件夹及其内容。

   下面的截图显示了我们希望在执行步骤 4-7 时看到的情况。如果您看到类似于此的情况，您的 Java 设置已完成。![hello_world]({{ site.baseurl }}/docs/Lec01/assets/hello_world.png)

## E. 安装 IntelliJ

1. 从 [JetBrains](https://www.jetbrains.com/idea/download/) 网站下载 IntelliJ Community Edition。
2. 选择适合您的操作系统的版本后，点击下载并等待几分钟直到文件下载完成。
3. 运行安装程序。如果您已经安装了旧版本的 IntelliJ，您应该在此时卸载它并用这个新版本替换。您可以使用所有默认的安装选项，但有一个例外，如果**您使用 Windows**，请确保勾选“将启动器目录添加到 PATH”。如果您不小心错过了，最简单的解决方案是卸载 IntelliJ，并再次运行安装程序，确保这次勾选该选项。**下面的图片只适用于 Windows。**

![Path]({{ site.baseurl }}/docs/Lec01/assets/path.png)

## F. 安装 IntelliJ CS 61B 插件

启动 IntelliJ 后开始设置过程。然后按照以下步骤操作。

**在继续之前，请确保您运行的是 2020.3.1 版或更高版本的 IntelliJ。** 旧版本可能也可以使用，但我们自己没有尝试过。

1. 在 *欢迎* 窗口中，点击左侧菜单上的 **“插件”** 按钮。![Configure Plugin]({{ site.baseurl }}/docs/Lec01/assets/plugin_setup1.png)
2. 在出现的窗口中，点击“市场”并在顶部的搜索栏中输入“CS 61B”。应该会出现 CS 61B 插件条目。如果您点击自动完成建议，可能会出现与下面显示的略有不同的窗口——这是可以的。
3. 点击绿色的 **安装** 按钮，等待插件下载并安装。![Search CS 61B]({{ site.baseurl }}/docs/Lec01/assets/plugin_setup2.png)
4. 现在，搜索“Java Visualizer”，并点击绿色的 **安装** 按钮以安装插件。![Search Java Visualizer]({{ site.baseurl }}/docs/Lec01/assets/plugin_setup3.png)
5. 如果出现，点击绿色的 **重新启动 IDE** 按钮以完成安装。如果您没有看到 **重新启动 IDE** 按钮，继续进行。

有关使用插件的更多信息，请阅读[插件指南](https://sp21.datastructur.es/materials/guides/plugin.html#using-the-plugins)。您现在不必马上阅读这个。

## G. 庆祝

哇！您终于完成了所有设置。您现在可以继续进行实验室 1 了。
