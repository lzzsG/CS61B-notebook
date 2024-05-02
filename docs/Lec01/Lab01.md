---
layout: page
title: Lab 1 IntelliJ, Java, git
permalink: /Lab01/
nav_order: 2
parent: L01 Intro, Hello World Java


---

# Lab 1: IntelliJ, Java, git

---

## Before You Begin在你开始之前

- Before beginning this lab, complete [lab1setup](https://sp21.datastructur.es/materials/lab/lab1setup/lab1setup) to install software required for 61B. If you get stuck at any point, feel free to post on Ed or attend lab, or come to Office Hours.在开始本实验之前，请完成 lab1setup 以安装 61B 所需的软件。如果您在任何时候遇到困难，请随时在 Ed 上发帖或参加实验室，或者参加办公时间。
- Be aware that there are a large number of setup steps this first week. **Don’t be discouraged**, and make sure to ask for help if you’re stuck!请注意，第一周有大量设置步骤。不要灰心，如果遇到困难，请务必寻求帮助！
- Warning: This lab runs a little long, and it’s normal if you do not finish during your lab period, especially if you end up having a tricky setup issue that requires a lot of assistance.警告：本实验运行时间有点长，如果您在实验期间没有完成，这是正常的，特别是如果您最终遇到需要大量帮助的棘手设置问题。
- It’s OK to talk to other students while you work on this lab (or any other), but you should ultimately do all the typing/programming/entering-of-commands yourself. There’s a lot of important setup information in this lab that you need to have done independently of anyone else.当你在这个实验室（或任何其他实验室）工作时，可以与其他学生交谈，但你最终应该自己完成所有的打字/编程/输入命令。本实验中有很多重要的设置信息，您需要独立于其他人完成。

## GitHub and BeaconGitHub 和信标

Instead of bCourses, CS61B uses an in-house system for centralizing your grades and student information called Beacon.CS61B 使用名为 Beacon 的内部系统来集中您的成绩和学生信息，而不是 bCourses。

In this section, we’ll set up your Beacon account as well as your CS 61B GitHub repository (“repo”), which you will need to submit all coding assignments.在本节中，我们将设置您的 Beacon 帐户以及 CS 61B GitHub 存储库（“repo”），您将需要使用它来提交所有编码作业。

1. Create an account at [GitHub.com](https://github.com/). If you already have an account, you do not need to create a new one.在 GitHub.com 创建一个帐户。如果您已有帐户，则无需创建新帐户。
2. Go to [the Beacon website](https://sp21.beacon.datastructur.es/register/) and you’ll be guided through a few steps to complete your GitHub repository registration. Please follow them carefully! You must be logged in to your Berkeley account to complete the Google Form quiz. If any errors occur while you’re working through the steps, please let your TA know immediately.访问 Beacon 网站，系统将引导您完成几个步骤来完成 GitHub 存储库注册。请仔细关注他们！您必须登录您的伯克利帐户才能完成 Google 表单测验。如果您在执行这些步骤时出现任何错误，请立即告知您的助教。
3. After completing all of the steps, you should receive an email inviting you to collaborate on your course GitHub repository, accept the email invitation from **both** emails and you should be good to go. This email will be sent to the **email that you used to create your GitHub account, which may not necessarily be your Berkeley email**. Hooray! **Don’t follow the instructions that GitHub says you might want to do** – instead, follow the instructions given later in this lab.完成所有步骤后，您应该会收到一封电子邮件，邀请您在课程 GitHub 存储库上进行协作，接受两封电子邮件中的电子邮件邀请，然后就可以开始了。此电子邮件将发送到您用于创建 GitHub 帐户的电子邮件，该电子邮件不一定是您的伯克利电子邮件。万岁！不要按照 GitHub 所说的您可能想要执行的说明进行操作，而是按照本实验后面给出的说明进行操作。

### More details about your repository有关您的存储库的更多详细信息

Your repository will have a name containing a number that is unique to you! For instance, if your repo is called “sp21-s42”, you’ll be able to visit your private repository at https://github.com/Berkeley-CS61B-Student/sp21-s42 (when logged into GitHub) If your repo number is not “42” this link will not work for you. Replace “42” with your own to see your repo on Github.您的存储库的名称将包含您唯一的数字！例如，如果您的存储库名为“sp21-s42”，您将能够访问您的私有存储库：https://github.com/Berkeley-CS61B-Student/sp21-s42（登录 GitHub 后）如果您的仓库编号不是“42”，此链接对您不起作用。将“42”替换为您自己的，即可在 Github 上查看您的存储库。

Additionally, the instructors, TAs, and tutors will be able to view your repository. This means you can (and should!) link to your code when asking private debugging questions on Ed. No other students will be able to view your repository. As a reminder, you may not post code from this course publicly, even after completing the course. Doing so is a violation of our course policies and you might be subject to disciplinary action.此外，讲师、助教和导师将能够查看您的存储库。这意味着您可以（并且应该！）在 Ed 上询问私人调试问题时链接到您的代码。其他学生将无法查看您的存储库。提醒一下，即使在完成课程之后，您也不得公开发布本课程的代码。这样做违反了我们的课程政策，您可能会受到纪律处分。

If you’re working with a lab partner, you’ll also receive a separate shared repository that you should use for labs. More details are provided on our Parterships Guide, which you can find on our Course Info page.如果您与实验室合作伙伴合作，您还将收到一个单独的共享存储库，供您用于实验室。我们的合作伙伴指南提供了更多详细信息，您可以在我们的课程信息页面上找到该指南。

Additionally, after registering with Beacon, you will be invited to collaborate on another repo of the form “snaps-sp21-sXXX” - don’t worry about what this repo is for now, just accept the invitation so you have access to it. We will have more information about this repo in a later section of this lab!此外，在 Beacon 注册后，您将被邀请合作开发另一个“snaps-sp21-sXXX”形式的存储库 - 现在不用担心这个存储库是什么，只需接受邀请即可访问它。我们将在本实验的后面部分提供有关此存储库的更多信息！

## A. Getting the Starter FilesA. 获取入门文件

For most of the assignments in this class (including this lab), we’ll provide a set of starter files.对于本课程中的大多数作业（包括本实验），我们将提供一组入门文件。

To get the starter files, we’ll be using the git version control system, which you’ll learn more about later in this lab and throughout the course. For now, let’s simply use git to get the files for this lab.为了获取入门文件，我们将使用 git 版本控制系统，您将在本实验室后面和整个课程中了解更多有关该系统的信息。现在，我们简单地使用 git 来获取本实验的文件。

If you need help with creating directories, creating files, changing directories, etc., see section C of [lab1setup](https://sp21.datastructur.es/materials/lab/lab1setup/lab1setup.html).如果您在创建目录、创建文件、更改目录等方面需要帮助，请参阅 lab1setup 的 C 部分。

1. First, tell Git your name and email address so that your commits are correctly attributed to you. Run the following commands:首先，告诉 Git 您的姓名和电子邮件地址，以便您的提交正确归属于您。运行以下命令：

   Replace “Your Name” with your name, and “you@berkeley.edu” with your email address. You should use the email address that you used to sign up for GitHub. If that’s not your “@berkeley.edu” email address, that’s okay.将“您的姓名”替换为您的姓名，将“you@berkeley.edu”替换为您的电子邮件地址。您应该使用注册 GitHub 时使用的电子邮件地址。如果这不是您的“@berkeley.edu”电子邮件地址，也没关系。

   ```bash
    $ git config --global user.email "you@berkeley.edu"
    $ git config --global user.name "Your Name"
   ```

2. Clone your [Berkeley-CS61B-Student organization](https://github.com/Berkeley-CS61B-Student) repository.克隆您的 Berkeley-CS61B-Student 组织存储库。

   - Navigate to the spot in your folders on your computer where you’d like to start your repository. In the example below, I’m assuming you want all your stuff in a folder named cs61b, but you can pick a different name if you’d like.

     导航到计算机上文件夹中您想要启动存储库的位置。在下面的示例中，我假设您希望将所有内容放在名为 cs61b 的文件夹中，但如果您愿意，可以选择其他名称。

     ```bash
      $ cd cs61b
     ```

   - Enter the following command to clone your GitHub repo. Make sure to replace the

      

     ```plaintext
     s**
     ```

      

     with the class id you were given when you registered for your repo.

     输入以下命令来克隆您的 GitHub 存储库。确保将 s** 替换为您注册存储库时获得的类 ID。

     ```bash
      $ git clone https://github.com/Berkeley-CS61B-Student/sp21-s**.git
     ```

     If you’d like to use SSH instead of HTTPS (and [set up your own SSH key](https://help.github.com/articles/generating-ssh-keys/)), feel free to also do that instead. If you don’t know what any of this means, just use the command above. The advantage of SSH is that you won’t have to type in your GitHub password every time you use your repository.如果您想使用 SSH 而不是 HTTPS（并设置您自己的 SSH 密钥），也可以这样做。如果您不知道这意味着什么，只需使用上面的命令即可。 SSH 的优点是您不必每次使用存储库时都输入 GitHub 密码。

   - Move into your newly created repo! (Make sure you do this part, or the rest of the steps below will not work correctly.)

     进入您新创建的存储库！ （请确保执行此部分，否则以下其余步骤将无法正常工作。）

     ```bash
      $ cd sp21-s**
     ```

3. Add the

    

   ```plaintext
   skeleton
   ```

    

   remote repository. You will “pull” code from this remote repository to get starter code for assignments. Make sure that you are within the newly created repository folder before you continue with these commands.

   添加骨架远程存储库。您将从该远程存储库“拉取”代码以获取作业的起始代码。在继续执行这些命令之前，请确保您位于新创建的存储库文件夹中。

   - Enter the following command to add the

      

     ```plaintext
     skeleton
     ```

      

     remote.

     输入以下命令以添加骨架遥控器。

     ```bash
      $ git remote add skeleton https://github.com/Berkeley-CS61B/skeleton-sp21.git
     ```

   - Listing the remotes should now show both the

      

     ```plaintext
     origin
     ```

      

     and

      

     ```plaintext
     skeleton
     ```

      

     remotes.

     列出遥控器现在应该显示原始遥控器和骨架遥控器。

     ```bash
      $ git remote -v
     ```

   - If you get an error that says “Not a git repository”, make sure you’re in the `sp21-s**` directory.如果您收到“不是 git 存储库”的错误，请确保您位于 sp21-s** 目录中。

4. You must now “pull” from the

    

   ```plaintext
   skeleton
   ```

    

   remote in order to get the starter code for Lab 1. You will also do this when new projects and assignments are released. To do this, use the spookiest command in the whole git toolbox:

   现在，您必须从骨架遥控器“拉取”以获得实验 1 的起始代码。当新项目和作业发布时，您也将执行此操作。为此，请使用整个 git 工具箱中最诡异的命令：

   ```bash
    $ git pull skeleton master
   ```

   What this does is grab all remote files from the repo named `skeleton` (which is located at `https://github.com/Berkeley-CS61B/skeleton-sp21.git`) and copies them into your current folder.其作用是从名为 sculpture 的存储库（位于 https://github.com/Berkeley-CS61B/sculpture-sp21.git）中获取所有远程文件，并将它们复制到当前文件夹中。

   If you get an error similar to “fatal: refusing to merge unrelated histories”, you probably ran GitHub’s suggested commands when you created your repository. To fix this, you can instead run:如果您收到类似于“致命：拒绝合并不相关历史记录”的错误，则您可能在创建存储库时运行了 GitHub 建议的命令。要解决此问题，您可以运行：

   ```bash
    $ git pull --rebase --allow-unrelated-histories skeleton master
   ```

   this time only.仅限这一次。

5. If you list the files in your current directory, you’ll see that there is now a folder named `lab1` Look in the `lab1` folder and you’ll see files called `HelloWorld.java`, `HelloNumbers.java`, `Collatz.java`, and others, that you’ll work with in later parts of this lab.如果列出当前目录中的文件，您将看到现在有一个名为 lab1 的文件夹。在 lab1 文件夹中查看，您将看到名为 HelloWorld.java、HelloNumbers.java、Collatz.java 等的文件，这些文件您将在本实验的后续部分中使用。

## B. Running Code in IntelliJB. 在 IntelliJ 中运行代码

IntelliJ is an IDE (Integrated Development Environment). It includes a text editor as well as a whole lot of extra features to make writing code easier. Let’s try it out first on our lab1 folder.IntelliJ 是一个 IDE（集成开发环境）。它包括一个文本编辑器以及许多额外的功能，使编写代码变得更容易。我们先在 lab1 文件夹中尝试一下。

1. Upon opening IntelliJ, click on the “Open” option.打开 IntelliJ 后，单击“打开”选项。![IntelliJ Start Menu]({{ site.baseurl }}/docs/Lec01/assets/intellij_start_menu-1714665958302-33.png)
2. Find and choose your lab1 directory, then press the OK button. Once you’ve pressed finish, you should see something really similar to the following image. You may need to click the little triangle next to `lab1` in the top left to get the source files (`HelloWorld`, `HelloNumbers`, `Collatz`, `GetEnvironmentVariables`, and `CheckLabConfig`) to show up. If you don’t see the sidebar, go to **View → Tool Windows → Project**, or select **“Project”** on the left toolbar.查找并选择您的 lab1 目录，然后按“确定”按钮。按下完成后，您应该会看到与下图非常相似的内容。您可能需要单击左上角 lab1 旁边的小三角形才能显示源文件（HelloWorld、HelloNumbers、Collatz、GetEnvironmentVariables 和 CheckLabConfig）。如果您没有看到侧边栏，请转到“视图”→“工具窗口”→“项目”，或选择左侧工具栏上的“项目”。![IntelliJ with lab 1 open]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1-1714665958302-35.png)

Note: The first time you start up IntelliJ it might take some time indexing files. This may take a few minutes. There should be a little progress bar in the bottom right. Some steps might not work until this is done.注意：第一次启动 IntelliJ 时，索引文件可能需要一些时间。这可能需要几分钟的时间。右下角应该有一个小进度条。完成此操作之前，某些步骤可能不起作用。

1. Double click on HelloNumbers and you’ll see your HelloNumbers code appear. Your color scheme won’t look like what is shown in the picture below (which is the official Josh Hug approved color scheme, called Sunburst). If you think you’d like to use Sunburst instead, see the very end of this lab for an optional setup. There should be no errors (code highlighted in red). If you see any errors, please post to Ed or ask your lab TA.双击 HelloNumbers，您将看到您的 HelloNumbers 代码出现。您的配色方案不会如下图所示（这是 Josh Hug 官方批准的配色方案，称为 Sunburst）。如果您想改用 Sunburst，请参阅本实验的最后部分以获取可选设置。不应有错误（代码以红色突出显示）。如果您发现任何错误，请发帖给 Ed 或询问您的实验室助教。![IntelliJ with HelloNumbers open]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1_HelloNumbers_open-1714665958302-37-1714665958303-38.png)
2. Next, let’s run your HelloNumbers. To do this, click “Run”, then click the “Run…” option.接下来，让我们运行您的 HelloNumbers。为此，请单击“运行”，然后单击“运行...”选项。![Preparing to run HelloNumbers]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1_HelloNumbers_run_run-1714665958303-39.png)
3. This will bring up two choices, one called “Edit Configuration”, and one called “HelloNumbers”. You may see other options for files we will interact with later this lab. IntelliJ supports all sorts of complicated configuration options for running Java programs, but we’re happy with the default here, so let’s just click on the one that says “HelloNumbers”.这将出现两个选择，一种称为“编辑配置”，另一种称为“HelloNumbers”。您可能会看到我们稍后将在本实验中与之交互的文件的其他选项。 IntelliJ 支持运行 Java 程序的各种复杂配置选项，但我们对此处的默认设置感到满意，所以我们只需单击显示“HelloNumbers”的选项即可。![Picking a run option]({{ site.baseurl }}/docs/Lec01/assets/main_screen_when_done_lab1_HelloNumbers_run_run_after_click-1714665958303-41.png)

Look at the output the program generated! You should see some nice numbers printed out! Hello Numbers!看看程序生成的输出！您应该会看到打印出一些不错的数字！你好数字！

## C. Setting up SnapsC. 设置快照

You have two course repositories, one standard repository (e.g. sp21-s33) and one Snaps repository (snaps-sp21-s33). Commits to your standard repository are made manually. Commits to the snaps repository are made automatically.您有两个课程存储库，一个标准存储库（例如 sp21-s33）和一个 Snaps 存储库（snaps-sp21-s33）。对标准存储库的提交是手动进行的。对快照存储库的提交是自动进行的。

The Snaps repository will act as a safe backup of your work in case you forget to actually make manual commits with git. You’ll push your Snaps repository after every project, which will allow us to release stats like the average time it took for students to complete each project (or each part of each project). It will also allow us to identify parts of projects that are much more confusing or time consuming that we anticipated. And it will also allow us to understand if the workload we’ve assigned is too high, so that we can tune down the course difficulty if we’ve overburdened you. If you are strongly opposed to pushing your Snaps repository, please contact your mentor GSI at that time. There will be more information about mentor GSIs during the second week of classSnaps 存储库将充当您工作的安全备份，以防您忘记使用 git 进行手动提交。您将在每个项目之后推送您的 Snap 存储库，这将使我们能够发布统计数据，例如学生完成每个项目（或每个项目的每个部分）所需的平均时间。它还将使我们能够识别项目中比我们预期更混乱或更耗时的部分。它还可以让我们了解我们分配的工作量是否太高，以便在您负担过重时可以降低课程难度。如果您强烈反对推送您的 Snap 存储库，请当时联系您的导师 GSI。课程第二周将提供有关导师 GSI 的更多信息

We don’t want you to feel like we’re looking over your shoulder! Thus, we will not be manually analyzing Snaps repositories, nor will we use any of the Snaps repository information for plagiarism detection. That is, all analysis will be conducted via bulk analytical tools that are unaware of your identity, and nothing in your Snaps repository will be used against you in any way.我们不希望您觉得我们在监视您！因此，我们不会手动分析 Snaps 存储库，也不会使用任何 Snaps 存储库信息进行抄袭检测。也就是说，所有分析都将通过批量分析工具进行，这些工具不知道您的身份，并且您的 Snap 存储库中的任何内容都不会以任何方式用于对付您。

At the very end of the semester, you will also have the opportunity to opt-in to a research project. Details will be provided at that time.在学期结束时，您还将有机会选择参加研究项目。届时将提供详细信息。

In this section of lab you will set up your computer to allow the creation of the Snaps backups.在本实验部分中，您将设置计算机以允许创建 Snap 备份。

### Getting the Snaps Repo获取 Snap 存储库

You should have gotten and accepted an invitation to collaborate on a `snaps-sp21-s***` repo. If you have not accepted it, please do not proceed until you do. If you can’t find the invitation in your email inbox (remember, the email account attached to your GitHub account, which may not necessarily be your Berkeley email), please post on Ed or come to lab or Office Hours, so we can help you.您应该已经收到并接受了在 snaps-sp21-s*** 存储库上进行协作的邀请。如果您尚未接受，请在接受之前不要继续。如果您在电子邮件收件箱中找不到邀请（请记住，附加到您的 GitHub 帐户的电子邮件帐户，不一定是您的伯克利电子邮件），请在 Ed 上发布或来到实验室或办公时间，以便我们提供帮助你。

First, we will clone the snaps repo to your computer. In your terminal (Git Bash on Windows), navigate to your home directory: `cd ~`. Then, run the following command, replacing *** with your repo number:首先，我们将快照存储库克隆到您的计算机。在您的终端（Windows 上的 Git Bash）中，导航到您的主目录：cd ~。然后，运行以下命令，将 *** 替换为您的存储库编号：

```bash
git clone https://github.com/Berkeley-CS61B-Student/snaps-sp21-s***
```

If you run `ls`, you should now see the `snaps-sp21-s***` folder.如果运行 ls，您现在应该会看到 snaps-sp21-s*** 文件夹。

**IMPORTANT:** Never complete assignments in this folder. Gradescope tests will always fail if you submit code from the snaps folder. You should only interact with your sp21-s*** folder.重要提示：切勿完成此文件夹中的作业。如果您从 snaps 文件夹提交代码，Gradescope 测试将始终失败。您应该只与 sp21-s*** 文件夹交互。

### Setting Up Environment Variables设置环境变量

Next you’ll need to set up some environment variables. The precise steps to take depend on your operating system.接下来您需要设置一些环境变量。采取的具体步骤取决于您的操作系统。

- [Windows instructionsWindows 说明](https://sp21.datastructur.es/materials/lab/lab1/lab1SnapsSetupWindows.html)
- [macOS and Linux instructionsmacOS 和 Linux 说明](https://sp21.datastructur.es/materials/lab/lab1/lab1SnapsSetupMacAndLinux.html)

### Installing the Snaps Plugin安装 Snap 插件

### Mac OS and LinuxMac 操作系统和 Linux

1. After setting up the environment variables above, restart IntelliJ, and all terminal windows (close them and open a new one), so the variables can take effect.设置完上面的环境变量后，重新启动IntelliJ和所有终端窗口（关闭它们并打开一个新窗口），这样变量才能生效。
2. Go to the IntelliJ welcome window (you may have to click “File → Close Project” to get back to the welcome window)进入 IntelliJ 欢迎窗口（您可能需要单击“文件 → 关闭项目”才能返回欢迎窗口）
3. Choose “Plugins” (left panel) → “Marketplace” (top middle) → search “CS 61B Snaps”, and install.选择“插件”（左面板）→“市场”（顶部中间）→搜索“CS 61B Snaps”，然后安装。
4. IntelliJ may ask you to restart the IDE (a green “Restart IDEA” button will appear). If it does, restart it.IntelliJ 可能会要求您重新启动 IDE（将出现绿色的“重新启动 IDEA”按钮）。如果是这样，请重新启动它。
5. Do not ignore the next step.不要忽略下一步。
6. **Quit intelliJ** (regardless of whether it restarted or not in step 4). Yes, even though you may have just restarted it, quit it completely again.退出 intelliJ（无论步骤 4 中是否重新启动）。是的，即使您可能刚刚重新启动它，也要再次完全退出它。
7. Open a terminal window, and launch intelliJ by running `idea`. Do not run IntelliJ using the OS Gui (e.g. Finder in Mac OS).打开终端窗口，然后通过运行 idea 启动 intelliJ。不要使用 OS Gui（例如 Mac OS 中的 Finder）运行 IntelliJ。
8. Continue to the next section to test your environment variables.继续下一部分来测试您的环境变量。

### Windows视窗

1. After setting up the environment variables above, restart IntelliJ, and all terminal windows (close them and open a new one), so the variables can take effect.设置完上面的环境变量后，重新启动IntelliJ和所有终端窗口（关闭它们并打开一个新窗口），这样变量才能生效。
2. Go to the IntelliJ welcome window (you may have to click “File → Close Project” to get back to the welcome window)进入 IntelliJ 欢迎窗口（您可能需要单击“文件 → 关闭项目”才能返回欢迎窗口）
3. Choose “Plugins” (left panel) → “Marketplace” (top middle) → search “CS 61B Snaps”, and install.选择“插件”（左面板）→“市场”（顶部中间）→搜索“CS 61B Snaps”，然后安装。
4. IntelliJ may ask you to restart the IDE (a green “Restart IDEA” button will appear). If it does, restart it.IntelliJ 可能会要求您重新启动 IDE（将出现绿色的“重新启动 IDEA”按钮）。如果是这样，请重新启动它。
5. Do not ignore the next step.不要忽略下一步。
6. **Restart IntelliJ again**. Yes, even though you may have just restarted it, quit it completely and open it again.再次重新启动 IntelliJ。是的，即使您可能刚刚重新启动它，也请完全退出并再次打开它。

### Test Your Environment Variables测试您的环境变量

After reopening IntelliJ, make sure the lab1 folder is open in IntelliJ. Verify that you set the environment variables correctly by opening `CheckLabConfig`. Then click Run and go down to the option that says “Run…”.重新打开 IntelliJ 后，确保 lab1 文件夹在 IntelliJ 中打开。通过打开 CheckLabConfig 验证您设置的环境变量是否正确。然后单击“运行”并转到“运行...”选项。

![about to run check lab config]({{ site.baseurl }}/docs/Lec01/assets/windows_about_to_run_checklabconfig-1714665958303-43.png)

Now click on the option that contains `CheckLabConfig`:现在单击包含 CheckLabConfig 的选项：

![the check lab config option]({{ site.baseurl }}/docs/Lec01/assets/windows_check_lab_config_option-1714665958303-45.png)

This should run the main method of our `CheckLabConfig` class. If everything is working, you should see a message confirming that you are done with lab 1 set up!这应该运行我们的 CheckLabConfig 类的 main 方法。如果一切正常，您应该会看到一条消息，确认您已完成实验 1 设置！

## D. Programming ExerciseD. 编程练习

Open the file called `Collatz.java`. Try running it and you’ll see the number 5 get printed.打开名为 Collatz.java 的文件。尝试运行它，您会看到打印出数字 5。

This program is supposed to print the [Collatz sequence](https://en.wikipedia.org/wiki/Collatz_conjecture) starting from a given number. The Collatz sequence is defined as follows:该程序应该打印从给定数字开始的 Collatz 序列。 Collatz 序列定义如下：

If n is even, the next number is n/2. If n is odd, the next number is 3n + 1. If n is 1, the sequence is over.如果 n 是偶数，则下一个数字是 n/2。如果 n 是奇数，则下一个数字是 3n + 1。如果 n 是 1，则序列结束。

For example, suppose we start with 5. Since 5 is odd, the next number is 3x5 + 1 = 16. Since 16 is even, the next number is 8. Since 8 is even, the next number is 4. Since 4 is even the next number is 2. Since 2 is even, the next number is 1. At that point we’re done. The sequence was 5, 16, 8, 4, 2, 1.例如，假设我们从 5 开始。由于 5 是奇数，所以下一个数字是 3x5 + 1 = 16。由于 16 是偶数，所以下一个数字是 8。由于 8 是偶数，所以下一个数字是 4。由于 4 是偶数下一个数字是 2。由于 2 是偶数，所以下一个数字是 1。此时我们就完成了。顺序是 5、16、8、4、2、1。

Your first task is to write a method as follows: `public static int nextNumber(int n)` that returns the next number. For example `nextNumber(5)` should return 16. This method will be tested by the Gradescope autograder. Make sure to provide a description of the method as a comment. Your description should be contained by `/**` and `*/`. Comments contained by `/**` and `*/` are also called “Javadoc comments” or just “Javadocs”. These comments can span multiple lines if they need the extra space, e.g. the `nextNumber` Javadocs.您的第一个任务是编写一个方法，如下所示： public static int nextNumber(int n) 返回下一个数字。例如，nextNumber(5) 应返回 16。此方法将由 Gradescope 自动评分器进行测试。确保提供该方法的描述作为注释。您的描述应包含在 /** 和 */ 中。 /** 和 */ 包含的注释也称为“Javadoc 注释”或简称为“Javadocs”。如果这些注释需要额外的空间，则可以跨越多行，例如nextNumber Javadocs。

Javadocs may contain optional tags, e.g. `@param`. We do not require you to use any tags like this in 61B except the `@source` tag. Use the `@source` tag any time you receive significant help on a project. The `@source` tag is not required for HW or lab, though we recommend it anyway, since it’s a good scholarly and professional habit to cite your sources.Javadoc 可能包含可选标签，例如@参数。除了 @source 标签之外，我们不要求您在 61B 中使用任何类似的标签。每当您在项目上获得重要帮助时，请使用@source 标签。硬件或实验室不需要 @source 标签，但我们还是推荐它，因为引用来源是一个很好的学术和专业习惯。

Some Java tips:一些 Java 技巧：

- The `%` operator implements remainder. For example, the value of `x % 4` will be `0`, `1`, `2`, or `3`.% 运算符实现余数。例如，x % 4 的值为 0、1、2 或 3。
- The `==` operator compares two values for inequality. The code fragment `if (n % 4 == 1)` reads as “if the remainder when dividing n by 4 is equal to 1.”== 运算符比较两个值是否不相等。代码片段 if (n % 4 == 1) 读作“如果 n 除以 4 的余数等于 1”。

After writing `nextNumber`, fill in the `main` method so that it prints out the Collatz sequence starting from `n = 5`. For example, if `n = 5`, your program should print `5 16 8 4 2 1`. It’s fine if there’s an extra space after the 1.写完nextNumber后，填写main方法，使其打印出从n = 5开始的Collatz序列。例如，如果n = 5，你的程序应该打印5 16 8 4 2 1。如果后面有一个额外的空格就可以了1.

Fun fact: For all numbers, the Collatz sequence appears to terminate at 1. So far, however, nobody has been able to prove that this is true for all possible starting values, but all values up to approximately 2^68 have been checked. As noted in the wikipedia article, mathematician Jeffrey Lagarias noted that the Collatz conjecture “is an extraordinarily difficult problem, completely out of reach of present day mathematics.”有趣的事实：对于所有数字，Collatz 序列似乎都终止于 1。然而，到目前为止，没有人能够证明这对于所有可能的起始值都是正确的，但已检查了大约 2^68 以内的所有值。正如维基百科文章中所述，数学家杰弗里·拉加里亚斯指出，科拉茨猜想“是一个极其困难的问题，完全超出了当今数学的范围”。

## E. Pushing Your Work to GitHubE. 将您的工作推送到 GitHub

We’ll use the Git tool in this class to store a copy of your work in what is known as a “repository”. As we’ll see in a later lab, you’ll also be able to retrieve old versions of your work from your repository using Git. In fact, Git is the most popular code version control software used in the real world, and if you go into software engineering, it is almost guaranteed you’ll use this tool every day.我们将在本课程中使用 Git 工具将您的工作副本存储在所谓的“存储库”中。正如我们将在后面的实验中看到的，您还可以使用 Git 从存储库中检索旧版本的工作。事实上，Git 是现实世界中最流行的代码版本控制软件，如果你从事软件工程，几乎可以保证你每天都会使用这个工具。

The private company GitHub has servers that are able to store git repositories, and their website github.com provides a convenient web interface to view repositories.私营公司 GitHub 拥有能够存储 git 存储库的服务器，并且他们的网站 github.com 提供了方便的 Web 界面来查看存储库。

In this section, we’ll see how to “push” your repository to GitHub.在本节中，我们将了解如何将存储库“推送”到 GitHub。

First start by going to the GitHub URL corresponding to your repository. For example, if your repository number is 343, you’d go to https://github.com/Berkeley-CS61B-Student/sp21-s343. Go to the URL corresponding to your repository. You’ll see there’s nothing there. If you try other repository numbers, you’ll see that you do not have access. That is, only you (and the course staff) can view your respository.首先转到与您的存储库对应的 GitHub URL。例如，如果您的存储库编号是 343，您可以访问 https://github.com/Berkeley-CS61B-Student/sp21-s343。转到与您的存储库对应的 URL。你会发现那里什么也没有。如果您尝试其他存储库编号，您会发现您没有访问权限。也就是说，只有您（和课程工作人员）可以查看您的存储库。

To push your code, we’ll be using the following three commands: `add`, `push`, and `commit`. Don’t worry about the details yet, and simply follow the steps below:为了推送代码，我们将使用以下三个命令：add、push 和 commit。不要担心细节，只需按照以下步骤操作即可：

1. Open a terminal window and navigate to the folder containing your `sp21-s***` repository, **NOT** your `snaps-sp21-s***` repo. If you type the “ls” command, you should see your lab1 folder sitting there.打开终端窗口并导航到包含 sp21-s*** 存储库的文件夹，而不是 snaps-sp21-s*** 存储库。如果您键入“ls”命令，您应该会看到 lab1 文件夹就在那里。

2. Enter the following command to confirm that you’re in the right directory.

   输入以下命令以确认您位于正确的目录中。

   ```bash
    $ git status
   ```

   If everything is working correctly you should see something like:如果一切正常，您应该看到类似以下内容：

   ```bash
    On branch master
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
        modified:   lab1/Collatz.java
   ```

   What Git is telling you is that you’ve changed something about your lab1/Collatz.java folder that GitHub has not recorded. **Make sure that it says lab1/Collatz.java, not just Collatz.java**. If it says just Collatz.java, you should use `cd..` to go up one directory.Git 告诉您的是您已经更改了 lab1/Collatz.java 文件夹中的某些内容，但 GitHub 尚未记录。确保它显示的是 lab1/Collatz.java，而不仅仅是 Collatz.java。如果它只显示 Collatz.java，则应使用 cd.. 上一级目录。

3. Enter the command

   输入命令

   ```bash
    $ git add lab1/*
   ```

4. Enter the following command to confirm that add worked properly.

   输入以下命令以确认添加工作正常。

   ```bash
    $ git status
   ```

   If everything is working correctly, you should see something like:如果一切正常，您应该看到类似以下内容：

   ```bash
    On branch master
    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
            modified:   lab1/Collatz.java
   ```

   Now Git is telling you that it is acknowledging that you want to record the changes you made to Collatz.java.现在，Git 告诉您，它确认您想要记录对 Collatz.java 所做的更改。

5. Enter the command

   输入命令

   ```bash
    $ git commit -m "done with Collatz"
   ```

   When you do this, Git will make a recording of the changes you made to Collatz.java. It will also record the message “done with Collatz” along with the recording. These messages can be helpful if you’re looking to find a specific change at some point in the past. We’ll discuss further in a later lab. It will also print some output the terminal, and you’ll see something like below, though the number of insertions and deletions may be different.当您执行此操作时，Git 将记录您对 Collatz.java 所做的更改。它还会在录音中记录“与 Collatz 完成”的消息。如果您想查找过去某个时刻的特定更改，这些消息可能会很有帮助。我们将在稍后的实验中进一步讨论。它还会在终端上打印一些输出，您将看到如下所示的内容，尽管插入和删除的数量可能不同。

   ```bash
    [master e2c138b] done with Collatz
    1 file changed, 15 insertions(+), 1 deletion(-)
   ```

6. As before, enter the git status command.

   和以前一样，输入 git status 命令。

   ```bash
    $ git status
   ```

   If commit worked correctly, you should see something like:如果提交工作正常，您应该看到类似以下内容：

   ```bash
    On branch master
    nothing to commit, working tree clean
   ```

   The fact that the “working tree” is “clean” means that all of your work is backed up.“工作树”是“干净的”这一事实意味着您的所有工作都已备份。

7. Refresh the URL for your repo on GitHub.com. You’ll see that your changes STILL aren’t showing up. This is because we have one last step.在 GitHub.com 上刷新您的存储库的 URL。您会发现您的更改仍未显示。这是因为我们还有最后一步。

8. Enter the command:

   输入命令：

   ```bash
    $ git push origin master
   ```

9. Refresh the URL for your repo on GitHub.com. You should see that your changes to Collatz.java are now visible, along with the message you entered.在 GitHub.com 上刷新您的存储库的 URL。您应该看到对 Collatz.java 的更改以及您输入的消息现在可见。

Note that normally you won’t enter `git status` after every single command. We were only doing this to make sure that you entered the commands correctly. The three commands that we entered that were actually necessary to get your code on GitHub are summarized below:请注意，通常您不会在每个命令后输入 git status。我们这样做只是为了确保您正确输入命令。我们输入的三个命令对于在 GitHub 上获取代码实际上是必需的，总结如下：

```bash
git add lab1/*
git commit -m "done with Collatz"
git push origin master
```

A lot of questions probably come to mind:脑海中可能会浮现出很多问题：

- Why is it useful to have to manually track my changes rather than just using a tool like Dropbox that automatically makes backups?为什么手动跟踪我的更改比仅使用 Dropbox 这样自动进行备份的工具更有用？
- What do these individual commands do? If commit made a recording of my work, but it wasn’t visible until I entered push, then where was the backup made?这些单独的命令有什么作用？如果commit记录了我的工作，但是直到我进入push后才可见，那么备份在哪里呢？
- Why does it take 3 commands instead of just one? Why not just a single command like ‘git upload -m “done with Collatz”’ or whatever?为什么需要 3 个命令而不是 1 个？为什么不只是像“git upload -m”done with Collatz”这样的单个命令？

Let’s address them in turn:让我们依次解决它们：

**Q: Why wouldn’t people just use Dropbox (or similar)?** Dropbox is backing up everything at sporadic intervals. When writing programs, we often want to make backups at specific times and only of specific files. For example, when you finally get a program working, you might want to back it up at that point so you can come back to it if you break it later. Also the ability to add a message makes it easy to organize the backups so you can find the ones you want.问：为什么人们不直接使用 Dropbox（或类似的）？ Dropbox 会不定期地备份所有内容。在编写程序时，我们经常希望在特定时间仅备份特定文件。例如，当您最终让一个程序运行时，您可能希望在此时备份它，以便以后在破坏它时可以返回到它。此外，添加消息的功能使您可以轻松组织备份，以便您找到所需的备份。

**What does add do?** Add marks a file (or set of files) as something you want to backup.添加有什么作用？添加将一个文件（或一组文件）标记为您要备份的内容。

**What does commit do?** Commit creates a backup with the given message.提交有什么作用？提交使用给定消息创建备份。

**If commit makes a backup but not to GitHub, where did it back up my files?** On your own computer!如果 commit 进行了备份但没有备份到 GitHub，那么它在哪里备份了我的文件？在您自己的计算机上！

**What good is a backup on your own computer?** If you want to go back to an old version, you can do that using git using other commands. By storing the backup locally, restoring old backups is very fast and doesn’t require an internet connection.在自己的计算机上进行备份有什么好处？如果您想返回到旧版本，可以使用 git 使用其他命令来执行此操作。通过在本地存储备份，恢复旧备份的速度非常快，并且不需要互联网连接。

**What if my computer dies, isn’t the backup made by commit lost?** Yes. That’s why there’s a push command.如果我的电脑死机了，commit做的备份不是就丢失了吗？是的。这就是为什么有一个push命令。

**Why not do add, commit, and push in one command?** Sometimes you only want to add a small number of files, so you might call add on only those files before finally doing a commit. And sometimes you want to make commits but don’t want to push, for example because you don’t have internet access or because you’re working on code that is too sensitive to be placed on any internet site.为什么不在一个命令中完成添加、提交和推送呢？有时您只想添加少量文件，因此您可以在最终提交之前仅对这些文件调用 add 。有时您想要提交但不想推送，例如因为您无法访问互联网，或者因为您正在处理的代码过于敏感而无法放置在任何互联网站点上。

**How do I see the history of old backups and how do I restore them?** If you want to see old commits, you can use `git log`, and you can use `git checkout` to restore old copies of your code. We’ll cover these later. Alternately you can also use the web interface at GitHub.com to explore and even download old copies.如何查看旧备份的历史记录以及如何恢复它们？如果您想查看旧的提交，可以使用 git log，并且可以使用 git checkout 来恢复代码的旧副本。我们稍后会介绍这些。或者，您也可以使用 GitHub.com 上的 Web 界面来探索甚至下载旧副本。

We will come to understand git better throughout the semester.通过整个学期我们将更好地理解 git。

Bonus: As an analogy for those of you have seen the 1984 film Ghostbusters (which I watched literally every day as a small kid), the `add` command is somewhat like using your proton accelerator on a ghost (or ghosts), the `commit` command is a somewhat like pulling the ghost (or ghosts) into the trap, and the `push` command is somewhat like unloading the trap into the Containment Unit.额外奖励：对于那些看过 1984 年电影《捉鬼敢死队》（我小时候几乎每天都看）的人来说，add 命令有点像在一个（或多个）鬼魂上使用质子加速器，commit 命令是a 有点像将幽灵（或多个幽灵）拉入陷阱，而推送命令有点像将陷阱卸载到收容单元中。

## F. Submitting Lab 1F. 提交实验 1

The last step is to submit your work with Gradescope. Gradescope is the site that you’ll use to submit homework, lab, and project assignments. To sign up for Gradescope (if you haven’t already), head to [gradescope.com](http://gradescope.com/) and click on the white “Sign up for free” button in the middle. You should use your Berkeley email. You should have already been enrolled in our Gradescope page with your Berkeley email. If you have not been added to Gradescope yet, you can refer to our welcome post on Ed for an enrollment code.最后一步是使用 Gradescope 提交您的作业。 Gradescope 是您用来提交作业、实验和项目作业的网站。要注册 Gradescope（如果您还没有注册），请访问gradescope.com，然后单击中间的白色“免费注册”按钮。您应该使用您的伯克利电子邮件。您应该已经使用伯克利电子邮件注册了我们的 Gradescope 页面。如果您尚未添加到 Gradescope，您可以参阅我们在 Ed 上的欢迎帖子以获取注册代码。

Once you’re enrolled in the class on Gradescope, click on “Lab 1: Welcome to Java” to submit your code.在 Gradescope 上注册课程后，单击“实验 1：欢迎使用 Java”提交您的代码。

After clicking this button, you’ll be taken to a screen where you select your repository and branch (shown below). The first time you do this, you’ll have to link your GitHub account to Gradescope (similar to what you did on the registration website). Click the “Connect to GitHub” button and follow the instructions.单击此按钮后，您将进入一个屏幕，您可以在其中选择存储库和分支（如下所示）。第一次执行此操作时，您必须将 GitHub 帐户链接到 Gradescope（类似于您在注册网站上所做的操作）。单击“连接到 GitHub”按钮并按照说明进行操作。

Now select your repository and branch. If your repository is “sp21-s57”, you’ll select “sp21-s57” in the top box, and in the bottom box you’ll pick “master”.现在选择您的存储库和分支。如果您的存储库是“sp21-s57”，您将在顶部框中选择“sp21-s57”，并在底部框中选择“master”。

Later, you can create your own “branches” (as described in a later optional part of a 61Blab) if you want those graded instead, though that won’t be required in 61B.稍后，如果您希望对这些分支进行评分，则可以创建自己的“分支”（如 61Blab 的后续可选部分中所述），尽管 61B 中不需要这样做。

![Github Repo and Branch Selection]({{ site.baseurl }}/docs/Lec01/assets/github_repo_and_branch_selection-1714665958303-47.png)

Now press “Upload” to submit!现在按“上传”提交！

Please report any issues you may have to Ed. Entire error messages and/or screenshots are welcome.请向 Ed 报告您可能遇到的任何问题。欢迎提供完整的错误消息和/或屏幕截图。

***Important:\*** *We HIGHLY encourage you to make frequent commits!* **Lack of proper version control will not be considered an excuse for lost work, particularly after the first few weeks.**重要提示：我们强烈鼓励您经常做出承诺！缺乏适当的版本控制不会被视为丢失工作的借口，特别是在最初几周之后。

## G. Verifying Snaps InstallationG. 验证 Snap 安装

In your terminal, run the following commands, one by one:在终端中，一一运行以下命令：

```bash
cd $SNAPS_DIR
git push
```

Now, in Gradescope, you will see that Lab 1 has another grader called “Lab 1A: Snaps Checkoff”. Click on this button, and choose “Github” under “Submission Method”.现在，在 Gradescope 中，您将看到 Lab 1 有另一个评分器，名为“Lab 1A：Snaps Checkoff”。单击此按钮，然后在“提交方式”下选择“Github”。

This time, choose your `snaps-sp21-s***` repo and **NOT** your `sp21-s***` repo, and hit “Submit”.这次，选择您的 snaps-sp21-s*** 存储库，而不是 sp21-s*** 存储库，然后点击“提交”。

If you pass these grader tests, you have set up your computer correctly. Yay! If you didn’t pass this grader, try to repeat the steps in part C of this lab and/or this section more carefully, or **come to Office Hours**. Passing this grader is required for getting full credit on Lab 1.如果您通过了这些评分者测试，则您已正确设置计算机。耶！如果您没有通过此评分，请尝试更仔细地重复本实验 C 部分和/或本节中的步骤，或者参加办公时间。要获得实验 1 的满分，必须通过此评分。

Note that this is one of the few times you will make a submission using your Snaps repo, and we will always explicitely tell you to do so when necessary. Otherwise, always work on and submit assignments from your `sp21-s***` repo.请注意，这是您使用 Snaps 存储库进行提交的少数几次之一，我们将始终明确告诉您在必要时这样做。否则，请始终从 sp21-s*** 存储库中处理并提交作业。

## Recap回顾

1. The IntelliJ IDE is what we’ll be using to run Java code this semester.本学期我们将使用 IntelliJ IDE 来运行 Java 代码。
2. Git is a version control system that tracks the history of a set of files in the form of commits.Git 是一个版本控制系统，它以提交的形式跟踪一组文件的历史记录。
3. Commit often and use informative commit messages.经常提交并使用信息丰富的提交消息。
4. Pull from the `skeleton` remote repository to get or update starter code for assignments.从骨架远程存储库中提取以获取或更新作业的起始代码。
5. Use Gradescope to submit homework, labs, and projects.使用 Gradescope 提交作业、实验和项目。

## Josh Hug’s Color Scheme (Optional)Josh Hug 的配色方案（可选）

I’m not a big fan of the default IntelliJ colors, so I made my own color scheme, which is a very close imitation of the extremely good Sunburst theme for Sublime. To use my theme, download [hug_sunburst](https://sp21.datastructur.es/materials/lab/lab1/hug_sunburst.jar), and import it using the “File→Manage IDE Settings→Import Settings” option in IntelliJ. You might end up with large text, which I use for recording videos. To adjust the size of the font in Intellij to your liking, see [this link](https://www.jetbrains.com/help/idea/configuring-colors-and-fonts.html).我不太喜欢默认的 IntelliJ 颜色，所以我制作了自己的配色方案，这是对 Sublime 非常好的 Sunburst 主题的非常接近的模仿。要使用我的主题，请下载 Hug_sunburst，然后使用 IntelliJ 中的“文件→管理 IDE 设置→导入设置”选项导入它。您最终可能会得到大文本，我用它来录制视频。要根据您的喜好调整 Intellij 中的字体大小，请参阅此链接。