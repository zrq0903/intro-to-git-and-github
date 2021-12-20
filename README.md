# Introduction to Git and GitHub

Version control, Git, and GitHub are, each on their own, larger topics than we can handle in this class, but they are each such essential tools that you must learn how to use them. When it comes to programming, the first two, and to a lesser degree the third, are vital for handling any non-trivial project safely and efficiently. Beyond programming, any kind of project where you need to work structured and disciplined with data and processes that can vary over time, will benefit greatly from these tools, or tools like them.

This exercise will show you have to get started, and how we will use the tools in this class. If you are interested in learning a little more, you can download a (admittedly slightly dated) book I wrote on the topic here: [The Beginner's Guide to Git and GitHub](https://www.dropbox.com/s/1d086uef0fpehbj/Git-and-GitHub.pdf?dl=0).

## Getting assignment repositories

In version control systems, "repositories" essentially refer to directories with something like "track changes" enabled. Different systems differ on how this is implemented, but it is a fairly accurate description of how the Git system works. If you have a Git repository, you have a directory (including its subdirectories) where you can make changes, and Git will track them, such that you can go back and see what the project looked like in the past, compare the changes between different versions, revert to older versions if you need to, and much more.

Also common for version control systems, at least for the last 20-30 years, is that they have a distributed nature, where versions of your project can live in the cloud and be accessed by multiple collaborators. Each collaborator has his or her own local repository, where they can make changes that are not visible to others, and these local repositories know about one or more repositories that sit in the cloud, where they can push local changes to make the visible to the world, or from where they can pull down changes others have made.

GitHub handles this cloud-like behaviour for us, storing a repository in the cloud and connecting our local repositories to it, so it is not something we need to worry about day-to-day life. We can just work in our repository, push changes when we want to, and pull down our collaborators' changes when they have made them.

To use GitHub, you need an account there. It is free; you just need to sign up, so if you haven't got an account already, go to [https://github.com](https://github.com) and follow the instructions for signing up.

For the next step, we need to get a repository to work with.

In this class, I have set up a system that will create repositories for you. (It is not by any means hard to do it yourself--I suspect it will take less than five minutes to figure out how it is done--but the repositories I have set up include template code and various tools relevant to the class). Whenever I give you an exercise or project assignment on GitHub, you get a URL that you can click paste into your browser. You get those on the weekly exercise sheets.

The system I use for this is called GitHub Classrooms, and that is the interface you will be met with when you click on an assignment link. It isn't important to know how this works, just that it works a little different from what you would have to do to set up repositories on your own.

The first time you click on a link, you will be asked to identify yourself. I don't know what GitHub identifier you have, so you need to tell me who you are. Do not choose someone else at this point; I can change it, but I will be cross with you if you give me extra work.

![Identifying yourself from the roster](img/selecting-from-roster.png)

Once you have identified yourself, you can accept the assignment. There is only one button to press, so you can probably work out what you need to do.

![Accepting an assignment](img/accept-assignment.png)

You only need to identify yourself the first time; GitHub Classroom remembers which students have which GitHub identifiers (within a class).

For group assignments, you also need to create or join a team. If you are the first one to log in, you only have the option of creating a team

![Creating a team](img/create-team.png)

and you can give it any name you want, as long as it isn't taken.

![Naming a team](img/create-team-name.png)

If there are already teams when you log in, you can join an existing one or create a new one.

![Joining or creating a new time](img/join-team.png)

Unless you want to be unpopular, you should not join a team without discussing it with the other team members first.

After that, GitHub will start setting up your repository. It takes a little while, but usually less than a minute. You get a page that asks you to wait, so start aggressively reloading that page until something happens.

![Setting up the repo](img/setting-up-repo.png)

When the repository is configured, and you reload the page one file time, the page will look something like this:

![Repo done](img/repo-done.png)

If you click on the URL in blue, you go to your repository on GitHub

![Repo on GitHub](img/repo-on-github.png)

or if you click the Visual Studio Code icon, you can open the repository directly in Visual Studio Code (if you have it installed).

![Repo in VSCode](img/repo-in-vscode.png)

In the side-bar, it shows you information about a so-called pull request. Get away from there for now, I explain it in a little bit. Click on the files icon (top left corner) to see the files in the repository instead.

![Files in VSCode](img/files-in-vscode.png)

You are not really working on the cloud here, VS Code has downloaded the repository for you, and if you open a terminal you can see where the repository sits on your file system.

![Location of files in vscode](img/terminal-vscode.png)

If you are okay with that location, can leave the code there, and you are done with setting up the repo.

You can work directly with the repository in VS Code if you want, or you can download it from GitHub manually. It doesn't make any difference. I, however, will continue the description with downloading it, because with that approach we are not quite done yet.

If you are on GitHub, following the link you got, there is the name of the repositiory at the top (the blue name that was `birc-ctib-test/translating-codons-mailund` on the image above), below that there is a tool-bar (Code, Issues, Pull requests, Actions, ...), and below that four buttons. The only button that is interesting for us is the green Code one.

Click on that.

![GitHub Code](img/github-code.png)

There are three ways you can download the repository: you can "clone" it, you can open ith with GitHub Desktop, or you can download a zip file. The last option is no use to us, because we will only get a copy of the code, and we want a repository we can work with. The first option is something we can do if we have the command-line git tools installed. Then you copy the URL and in your terminal you write

```sh
> git clone https://github.com/<url to repo>
```

The second option lets you open and administrate the repository with a GUI tool, [GitHub Desktop](https://desktop.github.com). If you are not familiar with working on the command line, this is a good choice, and it is an excellent tool for the kind of work we will be doing.

In any case, whether you got the code using VS Code, GitHub Desktop, or you cloned the repository using the command line, you should now have a copy of the repository on your own machine.

## The status of an assignment

Let's go back to the GitHub page for your repository. I want you to explore the first four tabs in the tool bar (we will not need any of the others in this class).

![Four main tabs](img/four-main-tabs.png)

The first one, **Code**, is where you can get an overview of the content of your repository (and it does show more than just code). It has its uses, but for the purpose of this class, there is nothing here that we cannot simply see in our own repository.

The second, **Issues**, is for tracking, you guessed it, issues. When you have identified what tasks you need to complete a project, or if you have identified a bug that you need to fix later, you can go here and add a new issue.

![Issues](img/issues.png)

If you click the big green "New issue" button, you can add an issue.

![New issue](img/new-issue.png)

You can add labels to issues, assign them to group members, and many other things, but for the scope of projects in this class, that is likely over-kill. It is up to you, however, if and how you choose to use issues.

Under **Pull requests** you find something you might not be familar with: "pull requests". The reason you are unfamiliar with it, is that it is a rather GitHub-specific term. Pull requests are a mechanism for sharing code between repositories and between so-called branches in repositires, and the mechanism provides a way of reviewing changes before you inflict them on others.

We won't be using this mechanism, except in one way. I have configured GitHub Classroom to make one pull request when it created your repository, called Feedback, and you should see it here.

![Pull requests](img/pull-requests.png)

It is hardly big enough to notice, but there is a red x after the **Feedback** pull request. That bit is important, it means that the pull request does not pass some tests that I have set up. But click on the pull request to get more information.

![Feedback pull request](img/feedback-pr.png)

The description at the top of the pull requests tells you that you can use it communicate with me, and that is how we will handle the mandatory projects. You can use the pull request to add comments to each other, you add comments at the bottom of the page, but if you mention me (adding `@mailund`) in a comment, I will be notificed and can come running to help you out.

On a pull request, I can see all the changes you have made, and I can easily comment on your code, and on specific lines of the code, much easier than via email. If you are using VS Code to edit the code, it can even show line-specific comments I have made while you are editing. That detailed level of feedback is the reason we have this pull request. So don't close it if you want feedback (and me checking if you have passed the assignment is a form of feedback, so I will let you work out the consequences of closing before a project is accepted).

After the initial description, on all programming assignments, you should see the results of some tests. (They will move lower as you add comments, but they should always be there).

![Feedback tests](img/feedback-tests-pr.png)

For most assignments, I have added some consistency tests that are run on your code every time you push changes to GitHub (see below). They will, of course, fail when you haven't solved the assignment yet, and there is nothing wrong with that. It gives us something to work with.

(Do **not** push the "Merge pull request" button here; that would close the pull request and prevent you from further feedback. The big green tick-mark just tells you that you could if you wanted to, but you could also poke yourself in the eye with a fork if you wanted to, and that doesn't mean that it is a good idea).

If you click at the "Details" link next to a test, you go to the **Actions** tab, and into the details of a particular script.

![Failed job](img/failed-job.png)

There should be information enough there to tell you why the test failed, and that gives you information on how to fix it. A failed test is always good news, since it gives you information about what to do next.

If you click on the **Actions** tab at the top, you will get an overview of all the test scripts ever run.

![Actions](img/actions.png)

As you make your way through an exercise, these should eventually turn green.

For the mandatory projects, once we pass the deadline, I will come swooping in and review the Feedback pull request and either approve it or ask for changes. If the tests are not passing at this point, it will be a short review--get the tests to pass--so make sure that they pass before the deadline.

## Making changes to your own repository

The repository you have on your computer now really consists of two separate things: the files that you are currently working on, and the "track changes" log of the history of the repository.

Unlike tools such as Word or Google Docs, Git doesn't automatically incorporate changes into the history. If it did, most of the history of your code would be in an inconsistent state, since the code is unlikely to even compile and run if you are halfway through writing a function.

Git remember the changes you have commited to its history, and you can get information about which changes you have made since you last commited with `git status`. If you have not changed anything, the result is something like this:

```sh
> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

But let's say you have made changes to a file, for example this file, then the command will show you that.

```sh
> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

It tells us that our branch is up to date with `origin/main` (which doesn't mean anything to us yet, but see below), and that there are files that are modified but not staged for commit.

Try to go to the end of this file and write `DONE` on the last line. Then run the command and see what it says.

If you are using your editor or GitHub Desktop to interact with Git, then you can see similar information in a GUI. For a beginner, this might be more convinient, but I will continue the description using the command line. You can follow along using your GUI tool instead; it will have the same commands.

You have to explicitly add changes to the history, and you do that with two commands, `add` and `commit`.

The `add` command tells Git which files you have changed and want it to remember the changes on. Adding a file is called "staging" it, in Git-speak, but it just means that you want the next commit to include this file.

Let's add `README.md` so it will be staged for a commit.

```sh
> git add README.md
> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   README.md
```

Now `README.md` is moved from changes not staged for commit to changes that will be committed. It is still not commited, though, it is just staged. You can stage multiple files as you work on them, and wait with committing them to history until later.

When you are ready to commit, use

```sh
> git commit -m "I wrote DONE at the end of README.md"
```

The `-m` option is a message that we associate to the changes we commit. You can leave out the `-m` option, then `git` will open an editor to get the commit message, but you cannot leave out a message.

Now run `git status` again

```sh
> git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

No there are no changes to commit, staged or otherwise, but the command says that our branch is ahead of `origin/main`. This is because we have only told our own "track changes" about what we have been up to. The repository that sits in the cloud hasn't been informed about them yet. We will get to that in the next section.

The two-stage `add` + `commit` is necessary when you create new files, but if all the files you want to commit are already known to Git, and you want to commit all changes, you can combine the two commands using the option `-a`. If you write

```sh
> git commit -a -m "commit message"
```

the `-a` tells Git to just add all the modified files before committing.

However, it is only the files it knows about that it will add. Try adding a file to this repository, call it `hello.txt` and put `World!` in it. Then try committing with `-a -m` and see what happens. Then try adding `hello.txt`

```sh
> git add hello.txt
```

and try to commit once more.


## Pushing changes to GitHub and pulling changes back

Now, what is it about that `ahead of 'origin/main'` in the `git status` message?

```sh
> git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

The more you commit, the more you are ahead, so if you did more than one commit (and you should if you did both exercises), then you are more than 1 commit ahead now.

You have commited something to the history of your own local repository, but that does not mean that the repository that sits at GitHub knows about it. It is not nosy, and it will not keep track of all the copies that might be floating around. If you want it to know about it, then you have to tell it, and you do that by "pushing" your changes to it. The `origin/main` that Git is talking about is the repository that sits at GitHub. (Technically, it is a "branch" on that repository, but we don't need to get technical here).

The command for pushing to another repository is `git push`, so try this:

```sh
> git push
```

You don't need a commit message here, because you are not committing anything. All the changes that are relevant for this transaction are already known to your own repository, with commit messages, and it is just informing `origin/main`, the repository on GitHub, about them.

If there are changes that the repository at GitHub knows about, but your local repository does not, you can get them down to you with a reverse push, also known in the English language as a pull.

```sh
> git pull
```

There are various reasons why commit/pull is a two step procedure rather than a single command, but they matter little for projects such as those in this class, so there is no need to get into that. Suffices to know is that this is how it is.


## Merge conflicts

So, you can make changes to your repository and then push those changes to GitHub. If you have multiple computers, and you are working on the same project there, you can use this mechanism to synchronise them--a little safer than you can with Dropbox or OneDrive--but we want a little more out of a version control system. We also need to synchronise with collaborators, and in the projects in this class, we need to synchronise within groups.

If you have tried to collaborate by sharing a directory on Dropbox, you know that if several people add files to the same drive concurrently, there can be conflicts. If both Alice and Bob write to the file Caroline.txt at the same time, Dropbox can't consider both versions the "correct" one, and you have to resolve the conflict; you have to determine which if any of them is correct, or you need to merge the changes that Alice and Bob have made.

It is the same with Git, although here it is a bit safer than the mess that Dropbox does, since here we synchronise entire directories at a time and we can never end up with a mix of files from two different copies.

XXX


## Exercise 1:

Write DONE on the last line. (This is currently the last line, so add a line below it; don't for get to add a newline after DONE.)
