# Introduction to Git and GitHub

Version control, Git, and GitHub are, each on their own, larger topics than we can handle in this class, but they are each such essential tools that you must learn how to use them. When it comes to programming, the first two, and to a lesser degree the third, are vital for handling any non-trivial project safely and efficiently. Beyond programming, any kind of project where you need to work structured and disciplined with data and processes that can vary over time will benefit greatly from these tools or tools like them.

This exercise will show you have to get started and how we will use the tools in this class. If you are interested in learning a little more, you can download an (admittedly slightly dated) book I wrote on the topic here: [The Beginner's Guide to Git and GitHub](https://www.dropbox.com/s/1d086uef0fpehbj/Git-and-GitHub.pdf?dl=0).

## Getting assignment repositories

In version control systems, "repositories" essentially refer to directories with something like "track changes" enabled. Different systems differ on how this is implemented, but it reasonably accurately describes how the Git system works. If you have a Git repository, you have a directory (including its subdirectories) where you can make changes. Git will track them, such that you can go back and see what the project looked like in the past, compare the transitions between different versions, revert to older versions if you need to, and much more.

Also, the standard for version control systems, at least for the last 20-30 years, is that they have a distributed nature, where versions of your project can live in the cloud and be accessed by multiple collaborators. Each collaborator has his or her own local repository, where they can make changes that are not visible to others. These local repositories know about one or more repositories that sit in the cloud, where they can push local changes to make them visible to the world, or from where they can pull down changes others have made.

GitHub handles this cloud-like behaviour for us, storing a repository in the cloud and connecting our local repositories to it, so it is not something we need to worry about in day-to-day life. We can just work in our repository, push changes when we want to, and pull down our collaborators' changes when they have made them.

To use GitHub, you need an account there. It is free; you just need to sign up, so if you haven't got an account already, go to [https://github.com](https://github.com) and follow the instructions for signing up.

We need to get a repository to work with for the next step.

I have set up a system in this class that will create repositories for you. (It is not by any means hard to do it yourself--I suspect it will take less than five minutes to figure out how it is done--but the repositories I have set up include template code and various tools relevant to the class). Whenever I give you an exercise or project assignment on GitHub, you get a URL that you can click paste into your browser. You get those on the weekly exercise sheets.

The system I use for this is called GitHub Classrooms, and that is the interface you will be met with when you click on an assignment link. It isn't essential to know how this works, just that it works a little different from what you would have to do to set up repositories on your own.

The first time you click on a link, you will be asked to identify yourself. I don't know what GitHub identifier you have, so you need to tell me who you are. Do not choose someone else at this point; I can change it, but I will be cross with you if you give me extra work.

![Identifying yourself from the roster](img/selecting-from-roster.png)

Once you have identified yourself, you can accept the assignment. There is only one button to press, so you can probably work out what you need to do.

![Accepting an assignment](img/accept-assignment.png)

You only need to identify yourself the first time; GitHub Classroom remembers which students have which GitHub identifiers (within a class).

For group assignments, you also need to create or join a team. If you are the first one to log in, you only have the option of creating a team

![Creating a team](img/create-team.png)

and you can give it any name you want, as long as it isn't taken.

![Naming a team](img/create-team-name.png)

When you log in, if there are already teams, you can join an existing one or create a new one.

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

In the sidebar, it shows you information about a so-called pull request. Get away from there for now; I will explain it in a little bit. Click on the "files" icon (top left corner) to see the files in the repository instead.

![Files in VSCode](img/files-in-vscode.png)

You are not really working on the cloud here, VS Code has downloaded the repository for you, and if you open a terminal, you can see where the repository sits on your file system.

![Location of files in vscode](img/terminal-vscode.png)

If you are okay with that location, you can leave the code there, and you are done with setting up the repo.

You can work directly with the repository in VS Code if you want or download it from GitHub manually. It doesn't make any difference. However, I will continue the description of downloading it because we are not quite done with that approach.

If you are on GitHub, following the link you got, there is the name of the repositiory at the top (the blue name that was `birc-ctib-test/translating-codons-mailund` on the image above), below that there is a tool-bar (Code, Issues, Pull requests, Actions, ...), and below that four buttons. The only button that is interesting for us is the green Code one.

Click on that.

![GitHub Code](img/github-code.png)

There are three ways you can download the repository: you can "clone" it, open it with GitHub Desktop, or download a zip file. The last option is of no use to us because we will only get a copy of the code, and we want a repository we can work with. We can choose the first option if the command-line git tools are installed. Then you copy the URL, and in your terminal, you write

```sh
> git clone https://github.com/<url to repo>
```

The second option lets you open and manage the repository with a GUI tool, [GitHub Desktop](https://desktop.github.com). If you are not familiar with working on the command line, this is a good choice, and it is an excellent tool for the kind of work we will be doing.

In any case, whether you got the code using VS Code, GitHub Desktop, or you cloned the repository using the command line, you should now have a copy of the repository on your own machine.

## The status of an assignment

Let's go back to the GitHub page for your repository. I want you to explore the first four tabs in the toolbar (we will not need any of the others in this class).

![Four main tabs](img/four-main-tabs.png)

The first one, **Code**, is where you can get an overview of the content of your repository (and it does show more than just code). It has its uses, but for the purpose of this class, there is nothing here that we cannot simply see in our own repository.

The second, **Issues**, is for tracking, you guessed it, issues. When you have identified what tasks you need to complete a project, or if you have identified a bug that you need to fix later, you can go here and add a new issue.

![Issues](img/issues.png)

If you click the big green "New issue" button, you can add an issue.

![New issue](img/new-issue.png)

You can add labels to issues, assign them to group members, and many other things, but that is likely overkill for the scope of projects in this class. However, it is up to you if and how you choose to use issues.

Under **Pull requests**, you find something you might not be familiar with: "pull requests". You are unfamiliar with it because it is a rather GitHub-specific term. Pull requests are a mechanism for sharing code between repositories and between so-called branches in repositories. The tool provides a way of reviewing changes before you inflict them on others.

We won't be using this mechanism, except in one way. I have configured GitHub Classroom to make one pull request when it created your repository, called Feedback, and you should see it here.

![Pull requests](img/pull-requests.png)

It is hardly big enough to notice, but there is a red x after the **Feedback** pull request. That bit is important; it means that the pull request does not pass some tests that I have set up. But click on the pull request to get more information.

![Feedback pull request](img/feedback-pr.png)

The description at the top of the pull requests tells you that you can use it to communicate with me, which is how we will handle the mandatory projects. You can use the pull request to add comments to each other, you add comments at the bottom of the page, but if you mention me (adding `@mailund`) in a comment, I will be notified and can come running to help you out.

I can see all the changes you have made on a pull request, and I can easily comment on your code and on specific lines of the code; much easier than via email. If you are using VS Code to edit the code, it can even show line-specific comments I have made while you are editing. That detailed level of feedback is the reason we have this pull request. So don't close it if you want feedback (and me checking if you have passed the assignment is a form of feedback, so I will let you work out the consequences of closing before a project is accepted).

After the initial description, you should see the results of some tests on all programming assignments. (They will move lower as you add comments, but they should always be there).

![Feedback tests](img/feedback-tests-pr.png)

For most assignments, I have added some consistency tests that are run on your code every time you push changes to GitHub (see below). They will, of course, fail when you haven't solved the assignment yet, and there is nothing wrong with that. It gives us something to work with.

(Do **not** push the "Merge pull request" button here; that would close the pull request and prevent you from further feedback. The big green tick-mark just tells you that you could if you wanted to, but you could also poke yourself in the eye with a fork if you wanted to, and that doesn't mean that it is a good idea).

If you click at the "Details" link next to a test, you go to the **Actions** tab and into the details of a particular script.

![Failed job](img/failed-job.png)

There should be enough information to tell you why the test failed, which gives you information on how to fix it. A failed test is always good news since it gives you information about what to do next.

If you click on the **Actions** tab at the top, you will get an overview of all the test scripts ever run.

![Actions](img/actions.png)

These should eventually turn green as you make your way through an exercise.

Once we pass the deadline for the mandatory projects, I will come swooping in and review the Feedback pull request and either approve it or ask for changes. If the tests are not passing at this point, it will be a short review--"get the tests to pass"--so make sure that they are passing before the deadline.

## Making changes to your own repository

The repository you have on your computer now really consists of two separate things: the files you are currently working on and the "track changes" log of the repository's history.

Unlike tools such as Word or Google Docs, Git doesn't automatically incorporate changes into the history. If it did, most of the history of your code would be in an inconsistent state since the code is unlikely to even compile and run if you are halfway through writing a function.

Git remembers the changes you have committed to its history, and you can get information about which changes you have made since you last committed with `git status`. If you have not changed anything, the result is something like this:

```sh
> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

But let's say you have made changes to a file, for example, this file, then the command will show you that.

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

It tells us that our branch is up to date with `origin/main` (which doesn't mean anything to us yet, but see below) and that there are files that are modified but not staged for commit.

Try to go to the end of this file and write `DONE` on the last line. Then run the command and see what it says.

If you are using your editor or GitHub Desktop to interact with Git, then you can see similar information in a GUI. This might be more convenient for a beginner, but I will continue the description using the command line. You can follow along using your GUI tool instead; it will have the same commands.

You have to explicitly add changes to the history, and you do that with two commands, `add` and `commit`.

The `add` command tells Git which files you have changed and wants to remember the changes. Adding a file is called "staging" in Git-speak, but it just means that you want the next commit to include this file.

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

Now `README.md` is moved from changes not staged for commit to changes that will be committed. It is still not committed, though; it is just staged. You can stage multiple files as you work on them, and wait with committing them to history until later.

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

Now there are no changes to commit, staged or otherwise, but the command says that our branch is ahead of `origin/main`. This is because we have only told our own "track changes" about what we have been up to. The repository that sits in the cloud hasn't been informed about them yet. We will get to that in the next section.

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

You have committed something to the history of your own local repository, but that does not mean that the repository that sits at GitHub knows about it. It is not nosy, and it will not keep track of all the copies that might be floating around. If you want it to know about it, you have to tell it, and you do that by "pushing" your changes to it. The `origin/main` that Git is talking about is the repository that sits at GitHub. (Technically, it is a "branch" on that repository, but we don't need to get technical here).

The command for pushing to another repository is `git push`, so try this:

```sh
> git push
```

You don't need a commit message here because you are not committing anything. All the relevant changes for this transaction are already known to your own repository, with commit messages, and it is just informing `origin/main`, the repository on GitHub, about them.

If there are changes that the repository at GitHub knows about but your local repository does not, you can get them down to you with a reverse push, also known in the English language as a pull.

```sh
> git pull
```

There are various reasons why commit/pull is a two-step procedure rather than a single command, but they matter little for projects such as those in this class, so there is no need to get into that. Suffices to know is that this is how it is.


## Pulling changes and merging conflicts

So, you can make changes to your repository and then push those changes to GitHub. If you have multiple computers and are working on the same project there, you can use this mechanism to synchronise them--a little safer than you can with Dropbox or OneDrive--but we want a little more out of a version control system. We also need to synchronise with collaborators, and in the projects in this class, we need to synchronise within groups.

If you have tried to collaborate by sharing a directory on Dropbox, you know that there can be conflicts if several people add files to the same drive concurrently. If both Alice and Bob write to the file Caroline.txt at the same time, Dropbox can't consider both versions the "correct" one, and you have to resolve the conflict; you have to determine which if any of them is correct, or you need to merge the changes that Alice and Bob have made.

It is the same with Git, although here it is a bit safer than the mess that Dropbox does since here we synchronise entire directories at a time, and we can never end up with a mix of files from two different copies.

Your local repository doesn't know if anyone has made changes to the one at GitHub, so if you ask for a `git status`, everything will look fine. It will tell you that "your branch is up to date with 'origin/main'".

```sh
> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

If you want to know if anything actually changed at `origin/main`, you need to get changes down. There are two options here: you can "fetch" changes, or you can "pull" changes. The first just gets information about the `origin/main`, so Git can inform you what your status is.

```sh
> git fetch
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/birc-ctib/intro-to-git-and-github
   874b90f..cc88e7d  main       -> origin/main
> git status
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

nothing to commit, working tree clean
```

Here, the status tells us that we are now one commit *behind* `origin/main`, which means someone has made changes on GitHub.

As the message also tells us, we can use `git pull` to merge those changes into our own repository, after which we will have them as well.

You don't need to do `git fetch` first; you could also go directly to `git pull`. It will fetch the changes and then merge them into our directory. That is usually what I do.

However, what happens if the changes you pull down are in conflict with your own?

Changes made to other files, or changes made to other parts of a text file, can automatically be merged. They are not in conflict since they do not change the same data. But it does happen that you have made changes to the same bits as someone else, for example, the same function. Then Git doesn't know what to do--it will not make a judgement call on your code--and you have to resolve them.

If you pull, and there are such conflicts, Git will inform you:

```sh
> git pull
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
```

Then, it will have put both versions of the conflicting file(s) into the files, and you will need to go and pick which ones you want or change the two versions into a third.  The conflicts are highlighted with `>>>>>` and `<<<<<` annotations, but your editor should be highlighting them as well and assist you in resolving the conflict.

While you are in this situation, a `git status` will also remind you:

```sh
> git status
On branch main
Your branch and 'origin/main' have diverged,
and have 2 and 2 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
    both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

If you use a GUI, it will also highlight merge conflicts.

Edit the files with conflict; in this case, it is `README.md`. Then add it and commit it, and you have merged the two conflicting paths.

You can also run into trouble when you try to push your changes to GitHub. If there are changes there, and you cannot automatically resolve them, the `git push` command will tell you:

```sh
> git push
To https://github.com/birc-ctib/intro-to-git-and-github.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/birc-ctib/intro-to-git-and-github.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

The solution is the same as above; you need to `git pull` to get the changes from GitHub, resolve the conflicts, and then commit the resolution into your local repository. When you have done that, you can push your changes, with the resolved conflicts, back to GitHub with `git push`.

This all sounds terribly complicated, but it becomes second nature when you have done it a few times. To begin with, though, I recommend that you use the GUI tools or your editor to assist you. They have good support for this.



## Exercise 1:

Write DONE on the last line. (This is currently the last line, so add a line below it; don't forget to add a newline after DONE.)
