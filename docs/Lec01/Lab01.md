---
layout: page
title: 💻Lab 1 Setup, Setting Up Your Computer
permalink: /Lab01/
nav_order: 1
parent: L01 Intro, Hello World Java

---

# 实验1 设置你的计算机

---

> 相关介绍：
>
> - https://zhuanlan.zhihu.com/p/434144861
> - [csdiy.wiki](https://csdiy.wiki/%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E4%B8%8E%E7%AE%97%E6%B3%95/CS61B/)



我们鼓励您在开始Lab 1 之前尽可能多地完成此设置。如果您遇到困难，请寻求帮助。

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

哇！您终于完成了所有设置。您现在可以继续进行实验 1 了。

---

# Lab 1: IntelliJ, Java, git

## 开始之前

- 在开始本实验之前，请完成 [lab1setup](https://sp21.datastructur.es/materials/lab/lab1setup/lab1setup) 以安装 61B 所需的软件。
- 注意，这第一周有大量的设置步骤。**不要气馁**，如果你卡住了，请务必寻求帮助！
- 警告：本实验稍微有点长，尤其是如果你遇到复杂的设置问题需要大量帮助时，很正常在实验课期间完不成。
- 在进行本实验（或其他实验）时，可以与其他学生讨论，但最终你应该独立完成所有的输入/编程/命令输入。这个实验中有很多重要的设置信息，需要你独立完成。

## A. 获取起始文件

对于本课程中的大多数作业（包括本实验），我们会提供一组起始文件。

要获取起始文件，我们将使用 git 版本控制系统，你将在本实验和整个课程中了解更多关于 git 的知识。现在，让我们简单地使用 git 获取本实验的文件。

如果你需要帮助创建目录、创建文件、改变目录等，请参阅 [lab1setup](https://sp21.datastructur.es/materials/lab/lab1setup/lab1setup.html) 的 C 部分。

1. 首先，告诉 Git 你的名字和电子邮件地址，以便正确归属你的提交。运行以下命令：

   将“Your Name”替换为你的名字，将“your@email.xx”替换为你的电子邮件地址。**你应该使用注册 GitHub 时使用的电子邮件地址**。

   ```bash
   $ git config --global user.email "your@email.xx"
   $ git config --global user.name "Your Name"
   ```

2. 骨架仓库[skeleton-sp21](https://github.com/Berkeley-CS61B/skeleton-sp21)**。

   - 创建**私人仓库**进行试验。

   

## B. 在 IntelliJ 中运行代码

IntelliJ 是一个集成开发环境（IDE）。它包括一个文本编辑器以及许多额外功能，使编写代码更加容易。让我们首先在 lab1 文件夹中试用它。

1. 打开 IntelliJ 后，点击“Open”选项。

   ![IntelliJ Start Menu]({{ site.baseurl }}/docs/Lec01/assets/intellij_start_menu-1878792.png)

2. 找到并选择你的 lab1 目录，然后按 OK 按钮。一旦按下完成，你应该会看到与下图非常相似的内容。你可能需要点击左上角的 `lab1` 旁的小三角形，以显示源文件（`HelloWorld`、`HelloNumbers`、`Collatz`、`GetEnvironmentVariables` 和 `CheckLabConfig`）。如果你没有看到侧边栏，请转到 **View → Tool Windows → Project**，或选择左侧工具栏上的 **“Project”**。

   ![IntelliJ with lab 1 open]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1-1878793.png)

   注意：第一次启动 IntelliJ 时，可能需要一些时间来索引文件。这可能需要几分钟。在右下角应该有一个进度条。在完成之前，某些步骤可能无法正常工作。

3. 双击 HelloNumbers，你会看到你的 HelloNumbers 代码出现。你的配色方案可能不会像下面图片中所示的那样（这是官方 Josh Hug 认可的配色方案，称为 Sunburst）。如果你想使用 Sunburst 配色方案，请参见本实验末尾的可选设置部分。应该没有错误（代码以红色突出显示）。如果看到任何错误，请在 Ed 上发帖或询问实验助教。

   ![IntelliJ with HelloNumbers open]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1_HelloNumbers_open-1878792.png)

4. 接下来，让我们运行你的 HelloNumbers。为此，点击“Run”，然后点击“Run…”选项。

   ![Preparing to run HelloNumbers]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1_HelloNumbers_run_run-1878792.png)

5. 这会显示两个选项，一个叫“Edit Configuration”，一个叫“HelloNumbers”。你可能会看到本实验稍后将与之交互的其他文件的选项。IntelliJ 支持各种复杂的配置选项来运行 Java 程序，但我们对默认配置感到满意，所以只需点击“HelloNumbers”。

   ![Picking a run option]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1_HelloNumbers_run_run_after_click-1878792.png)

   看看程序生成的输出！你应该看到一些漂亮的数字被打印出来！Hello Numbers！

## D. 编程练习

打开名为 `Collatz.java` 的文件。尝试运行它，你会看到数字 5 被打印出来。

这个程序应该从给定的数字开始打印 [Collatz 序列](https://en.wikipedia.org/wiki/Collatz_conjecture)。Collatz 序列定义如下：

如果 n 是偶数，下一数字是 n/2。如果 n 是奇数，下一数字是 3n + 1。如果 n 是 1，序列结束。

例如，假设我们从 5 开始。因为 5 是奇数，下一数字是 3x5 + 1 = 16。因为 16 是偶数，下一数字是 8。因为 8 是偶数，下一数字是 4。因为 4 是偶数，下一数字是 2。因为 2 是偶数，下一数字是 1。此时我们结束。序列是 5, 16, 8, 4, 2, 1。

你的第一个任务是编写一个方法

如下：`public static int nextNumber(int n)`，它返回下一个数字。例如，`nextNumber(5)` 应返回 16。这个方法将由 Gradescope 自动评分器测试。确保提供方法描述作为注释。你的描述应包含在 `/**` 和 `*/` 之间。这种注释也称为“Javadoc 注释”或简称“Javadocs”。如果需要更多空间，这些注释可以跨多行，例如 `nextNumber` 的 Javadocs。

Javadocs 可以包含可选标签，例如 `@param`。在 61B 中我们不要求你使用任何这样的标签，除了 `@source` 标签。当你在项目中获得重要帮助时使用 `@source` 标签。`@source` 标签不要求用于家庭作业或实验，但我们仍然建议使用，因为这是一个良好的学术和职业习惯，引用你的来源。

一些 Java 小贴士：

- `%` 运算符实现取余。例如，`x % 4` 的值将是 `0`、`1`、`2` 或 `3`。
- `==` 运算符比较两个值是否相等。代码片段 `if (n % 4 == 1)` 读作“如果 n 除以 4 的余数等于 1”。

编写 `nextNumber` 后，填写 `main` 方法，使其从 `n = 5` 开始打印出 Collatz 序列。例如，如果 `n = 5`，你的程序应打印 `5 16 8 4 2 1`。如果 1 后有一个额外的空格，也没关系。

有趣的事实：对于所有数字，Collatz 序列似乎都终止于 1。然而，到目前为止，还没有人能够证明这对于所有可能的起始值都是正确的，但已经检查了大约 2^68 的所有值。如维基百科文章中所述，数学家 Jeffrey Lagarias 指出 Collatz 猜想“是一个极其困难的问题，完全超出了当代数学的能力范围”。

## E. 将你的工作推送到 GitHub

在本课程中，我们将使用 Git 工具在所谓的“存储库”中存储你的工作副本。正如我们将在稍后的实验中看到的那样，你还可以使用 Git 从存储库中检索旧版本的工作。实际上，Git 是现实世界中最流行的代码版本控制软件，如果你进入软件工程领域，几乎可以肯定你每天都会使用这个工具。

私营公司 GitHub 具有能够存储 git 存储库的服务器，其网站 github.com 提供了方便的 Web 界面来查看存储库。

在本节中，我们将看到如何将你的存储库“推送”到 GitHub。

要推送代码，我们将使用以下三个命令：`add`、`commit` 和 `push`。不要担心细节，只需按照以下步骤操作：

1. 打开终端窗口并导航到包含你的存储库的文件夹。如果你输入 `ls` 命令，你应该会看到你的 lab1 文件夹在那里。

2. 输入以下命令以确认你在正确的目录中。

   ```
   $ git status
   ```

   如果一切正常，你应该看到类似这样的内容：

   ```bash
   On branch master
   Changes not staged for commit:
     (use "git add <file>..." to update what will be committed)
     (use "git restore <file>..." to discard changes in working directory)
       modified:   lab1/Collatz.java
   ```

   Git 告诉你的是，你已经更改了 lab1/Collatz.java 文件夹中的内容，但 GitHub 尚未记录。**确保它显示的是 lab1/Collatz.java，而不仅仅是 Collatz.java**。如果它仅显示 Collatz.java，你应该使用 `cd..` 返回上一级目录。

3. 输入命令

   ```bash
   $ git add lab1/*
   ```

4. 输入以下命令以确认添加是否正常工作。

   ```bash
   $ git status
   ```

   如果一切正常，你应该看到类似这样的内容：

   ```bash
   On branch master
   Changes to be committed:
     (use "git restore --staged <file>..." to unstage)
           modified:   lab1/Collatz.java
   ```

   现在 Git 告诉你，它已经确认你想记录对 Collatz.java 所做的更改。

5. 输入命令

   ```bash
   $ git commit -m "done with Collatz"
   ```

   当你这样做时，Git 将记录你对 Collatz.java 所做的更改。它还会记录消息“done with Collatz”以及录音。这些消息在你想在某个时间点找到特定更改时很有帮助。我们将在稍后的实验中进一步讨论。它还会在终端上打印一些输出，你会看到类似下面的内容，尽管插入和删除的数量可能不同。

   ```bash
   [master e2c138b] done with Collatz
   1 file changed, 15 insertions(+), 1 deletion(-)
   ```

6. 像之前一样，输入 `git status` 命令。

   ```bash
   $ git status
   ```

   如果提交成功，你应该看到类似这样的内容：

   ```bash
   On branch master
   nothing to commit, working tree clean
   ```

   “working tree” 是“clean” 意味着你的所有工作都已备份。

7. 刷新你在 GitHub.com 上的存储库 URL。你会看到你的更改仍然没有显示。这是因为我们还有最后一步。

8. 输入命令：

   ```bash
   $ git push origin master
   ```

9. 刷新你在 GitHub.com 上的存储库 URL。你应该看到对 Collatz.java 的更改现在可见，以及你输入的消息。

请注意，通常你不会在每个命令后输入 `git status`。我们这样做只是为了确保你正确地输入了命令。将代码上传到 GitHub 的三个必要命令总结如下：

```bash
git add lab1/*
git commit -m "done with Collatz"
git push origin master
```

可能会出现很多问题：

- 为什么手动跟踪更改而不是使用像 Dropbox 这样的工具来自动备份是有用的？
- 这些单个命令做什么？如果提交创建了我的工作的录音，但在我输入推送之前它不可见，那么备份在哪里？
- 为什么要使用 3 个命令而不是一个命令？为什么不只使用一个像‘git upload -m "done with Collatz"’的命令？

让我们依次解决它们：

**问：为什么人们不使用 Dropbox（或类似的工具）？** Dropbox 不定期备份所有内容。在编写程序时，我们通常希望在特定时间点备份特定文件。例如，当你最终让程序运行时，你可能希望在那时备份，以便如果你稍后破坏它，可以回到那时。此外，添加消息的功能使得组织备份变得容易，你可以找到所需的备份。

**添加命令做什么？** 添加将一个文件（或一组文件）标记为你想要备份的内容。

**提交命令做什么？** 提交创建带有给定消息的备份。

**如果提交创建了备份，但没有备份到 GitHub，那么我的文件备份在哪里？** 在你自己的电脑上！

**在自己的电脑上备份有什么好处？** 如果你想回到旧版本，你可以使用 git 的其他命令做到这一点。通过本地存储备份，恢复旧备份非常快，不需要互联网连接。

**如果我的电脑坏了，提交创建的备份是不是丢失了？** 是的。这就是为什么有一个推送命令。

**为什么不在一个命令中完成添加、提交和推送？** 有时你只想添加少量文件，因此你可能只对那些文件调用添加，然后最终进行提交。有时你想提交但不想推送，例如因为你没有互联网连接或因为你正在处理的代码过于敏感而不能放在任何互联网网站上。

**如何查看旧备份的历史记录并如何恢复它们？** 如果你想查看旧提交，可以使用 `git log`，并可以使用 `git checkout` 恢复旧版本的代码。我们将在后续实验中介绍。或者，你也可以使用 GitHub.com 的 Web 界面来探索甚至下载旧版本。

我们将在整个学期中更好地理解 git。

奖励：对于那些看过 1984 年电影《捉鬼敢死队》（我小时候每天都看）的同学来说，`add` 命令有点像用质子加速器对付鬼

魂，`commit` 命令有点像将鬼魂拉入陷阱，而 `push` 命令有点像将陷阱卸载到隔离单元。

## F. 提交实验 1

最后一步是用 Gradescope 提交你的工作。Gradescope 是你用来评测作业、实验和项目的站点。要注册 Gradescope（如果你还没有），请访问 [gradescope.com](http://gradescope.com/) 并点击中间的白色“Sign up for free”按钮。

UC Berkeley，**邀请码** **MB7ZPY** 

一旦你在 Gradescope 上注册了课程，点击“Lab 1: Welcome to Java”提交你的代码。

点击此按钮后，你将进入一个选择存储库和分支的屏幕（如下所示）。第一次这样做时，你可以将你的 GitHub 账户链接到 Gradescope（类似于你在注册网站上所做的）。点击“Connect to GitHub”按钮并按照说明进行操作。

现在选择你的存储库和分支。如果你的存储库是“sp21-s57”，你将在顶部框中选择“sp21-s57”，在底部框中选择“master”。

以后，如果你希望评分其他分支，可以创建自己的“分支”（在 61B 实验的后面部分描述），但在 61B 中不会要求这样做。

> 你也可以选择不连接GitHub，而使用文件上传测评。

![Github Repo and Branch Selection]({{ site.baseurl }}/docs/Lec01/assets/github_repo_and_branch_selection-1878792.png)

按“Upload”提交！

**重要提示：** 我们强烈鼓励你频繁提交！**缺乏适当的版本控制不会被视为丢失工作的借口，特别是在最初的几周之后。**

## 回顾

1. IntelliJ IDE 是我们本学期将用于运行 Java 代码的工具。
2. Git 是一种版本控制系统，以提交的形式跟踪文件集的历史。
3. 经常提交并使用有信息量的提交消息。
4. 使用 Gradescope 提交作业、实验和项目。

## Josh Hug 的配色方案（可选）

Josh Hug不太喜欢默认的 IntelliJ 颜色，所以做了自己的配色方案，这是一个非常接近 Sublime 的极好 Sunburst 主题的模仿。要使用此主题，下载 [hug_sunburst](https://sp21.datastructur.es/materials/lab/lab1/hug_sunburst.jar)，并使用 IntelliJ 中的“File→Manage IDE Settings→Import Settings”选项导入它。你可能会得到大字体，Josh Hug用它来录制视频。要根据需要调整 IntelliJ 中字体的大小，请参见 [此链接](https://www.jetbrains.com/help/idea/configuring-colors-and-fonts.html)。
