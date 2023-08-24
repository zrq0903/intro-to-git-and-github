## Exercises

### Introduction to Git and GitHub

Version control, Git, and GitHub are, each on their own, larger topics than we can handle in this class, but they are each such essential tools that you must learn how to use them. When it comes to programming, the first two, and to a lesser degree the third, are vital for handling any non-trivial project safely and efficiently. Beyond programming, any kind of project where you need to work structured and disciplined with data and processes that can vary over time will benefit greatly from these tools or tools like them.

This exercise will show you have to get started and how we will use the tools in this class. If you are interested in learning a little more, you can download an (admittedly slightly dated) book T. Mailund wrote on the topic here: [The Beginner's Guide to Git and GitHub](https://www.dropbox.com/s/1d086uef0fpehbj/Git-and-GitHub.pdf?dl=0).

#### Getting assignment repositories

In version control systems, "repositories" essentially refer to directories with something like "track changes" enabled. Different systems differ on how this is implemented, but it reasonably accurately describes how the Git system works. If you have a Git repository, you have a directory (including its subdirectories) where you can make changes. Git will track them, such that you can go back and see what the project looked like in the past, compare the transitions between different versions, revert to older versions if you need to, and much more.

Also, the standard for version control systems, at least for the last 20-30 years, is that they have a distributed nature, where versions of your project can live in the cloud and be accessed by multiple collaborators. Each collaborator has his or her own local repository, where they can make changes that are not visible to others. These local repositories know about one or more repositories that sit in the cloud, where they can push local changes to make them visible to the world, or from where they can pull down changes others have made.

GitHub handles this cloud-like behaviour for us, storing a repository in the cloud and connecting our local repositories to it, so it is not something we need to worry about in day-to-day life. We can just work in our repository, push changes when we want to, and pull down our collaborators' changes when they have made them.

To use GitHub, you need an account there. It is free; you just need to sign up, so if you haven't got an account already, go to [https://github.com](https://github.com) and follow the instructions for signing up.

We need to get a repository to work with for the next step. In this class each assignment has a matching repository that you can use as template for completing the assignment.

The one available for this exercise is this: [Introduction to Git and GitHub](https://github.com/birc-ctib/intro-to-git-and-github). Click it, and then read on for further instructions.

If you are on GitHub, following the link you got, there is the name of the repositiory at the top, below that there is a tool-bar (Code, Issues, Pull requests, Actions, ...), and below that four buttons. Clicking on the blue "Use this template" button is one way of creating your own repository from the template.

![](img/get_repository.png)

There are three ways you can download the repository: you can "clone" it, open it with GitHub Desktop, or download a zip file. The last option is the simplest because you will only get a copy of the code, but if you want a repository you can work with, you need to use one of the other two options. We can choose the first option if the command-line git tools are installed. Then you copy the URL, and in your terminal, you write

```bash
> git clone https://github.com/[REPO-NAME]
```

The second option lets you open and manage the repository with a GUI tool, [GitHub Desktop](https://desktop.github.com). If you are not familiar with working on the command line, this is a good choice, and it is an excellent tool for the kind of work we will be doing.

In any case, whether you got the code using VS Code, GitHub Desktop, or you cloned the repository using the command line, you should now have a copy of the repository on your own machine.

Continue this exercise on the repository you just created. There is more to cover, but you will see the instructions there, and it is in that repository you can try out working with Git and GitHub.

### Introducing the command line

When you are familiar with Git and GitHub, you [should also familiarise yourself with the UNIX command line][command-line-ex].


[command-line-ex]: https://github.com/birc-ctib/command-lines-and-pipes


