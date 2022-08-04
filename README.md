# Complete Your First Software Engineering Assignment

## Learning Goals

- Understand the steps needed to complete an assignment and submit it in Canvas

## Introduction

During this course, you will work on various assignments as you learn to code.
All assignments will be interactive pieces of curriculum that require some work.
Some assignments may ask you to follow a set of instructions, while others will
ask you to figure out your own solution to pass specific tests. This lesson is
your first assignment!

All assignments are hosted on GitHub. In order to work on them, however, you
will need to complete work on your local machine. The general process is:

- Click the blue "Fork" button in Canvas
- Create a personal copy (a 'fork') of the assignment in GitHub
- Download your personal copy (referred to as 'cloning') to your computer
- Complete the required work
- Submit your completed work to Canvas

In this assignment, you'll learn the workflow that you will be using to complete
your assignments.

### A Quick Note on Organizing Work on Your Machine

Throughout this course, you will be downloading many assignments, so it is
important to keep your code organized. If you haven't yet, we recommend that you
go through the steps in
[the previous lesson](https://github.com/learn-co-curriculum/aws-organizing-work-on-your-computer)
to set up a directory where you can keep all of your work for this course.

> **Note:** The process we'll go through in this lesson will create sub-folders
> automatically. Whenever you are starting a new assignment, navigate back to
> the current `module-#` folder within your `code` folder (`cd ~/Development/code`) before cloning
> the assignment. This will ensure these sub-folders don't get created
> _within each other_.

### Accessing GitHub and Forking

All the lessons in this course have a corresponding repository (repo) in GitHub.
On this page in Canvas, you should see three icons in the **upper right**
corner. The first says **Fork**. The second is a button that looks like a
large-headed cat (GitHub's 'Octocat' icon), which will open the lesson's GitHub
repo _without_ forking. The third is a flag, which you can use to submit an
_issue_ for the lesson (e.g., if you find a typo or other error).

One way to fork an assignment is to click the Octocat button to go to the
assignment's GitHub repo and fork directly from that page. (We'll go through
that process in a later lesson.) However, when completing your Canvas
assignments, you should use the **Fork** button. Doing so will automate several
steps for you and ensure that, when you complete a lab, it is registered as
complete in Canvas.

Go ahead and fork this assignment by clicking the **Fork** button at the top of
the page.

<figure>
  <img src="https://curriculum-content.s3.amazonaws.com/fork-link.png" alt="fork link" height="25px">
  <figcaption><sm>This is just a picture, the button is up at the top of the page.</sm></figcaption>
</figure>

Clicking the **Fork** button will do one of two things — it will either start
the forking process or bring you to a page where you select where to create your
fork. If you're prompted to choose, select your personal GitHub account. The
forking process will begin and may take a few moments. When complete, you will
be redirected to a new copy of the assignment that exists under _your_ GitHub
account. The `README.md` file in your copy of the repository contains these
instructions, so you can continue this lesson here or in GitHub.

Forking is a process which creates an exact copy of a collection of code and
files. Once you've created a fork on your own GitHub account, you will be able
to edit the files in the repository and write your own code solution without
interfering with the original copy.

Once your fork is ready, the next step is to download (**clone**) your new
repository to your local machine.

### Cloning to Your Local Machine

To download the repository for this lesson, make sure you're in your personal
fork on GitHub, then click the **Code** button. A pop-up will appear which shows
several options for cloning: **HTTPS**, **SSH**, and **GitHub CLI**. **Before
doing anything else**, be sure to switch to **SSH**. With **SSH** selected, you
should see what looks sort of like an email in the box below, starting with
`git@github.com:`. You should see your GitHub name after the `:`.

> **Aside:** Why SSH? If you followed the setup instructions, you have added
> your personal SSH key to GitHub. GitHub will store your personal copies of all
> the work you do in this course. Because you've added your SSH key, GitHub will
> know who you are when you send work from your local machine to GitHub to be
> stored.

From here, click the copy button.

![clone-repo](https://curriculum-content.s3.amazonaws.com/phase-0/completing-assignments/clone-repo.gif)

Now, open your terminal and navigate to where you'd like to download the
assignment (e.g. `cd ~/Development/code`). Type `git clone` and a space, then
paste in the copied SSH link from GitHub. It should look something like this:

```console
$ git clone git@github.com:<your-user-name>/aws-completing-assignments.git
```

Press enter, and you should see a flurry of terminal activity.

> **Troubleshooting**: If you are a Mac user and you see the following message:
>
> `xcrun: error: invalid active developer path`
>
> You need to install the Xcode Command Line Tools. Run the following command to
> install them:
>
> ```console
> $ xcode-select --install
> ```
>
> And follow the prompts. Then try running the `git clone` command again. See
> [this Stack Overflow post](https://stackoverflow.com/a/52522566) for more
> details. Note that you may need to re-install `xcode-select` any time you
> update your Mac OS version.

Once the terminal gives you control to type again, a new folder with the GitHub
name of the assignment will have been created. Change directory into this folder
to access the assignment files.

```console
$ cd aws-completing-assignments
```

Now type `code .` to open up a text editor window with access to all of the
assignment's files. These instructions are now also available on your local
machine in `README.md`.

> Note: the first time you open a directory in Visual Studio Code, you'll see a
> message asking "Do you trust the authors of the files in this folders?" This
> is a [security feature][workspace-trust] of Visual Studio Code. It's safe to
> choose "Yes", and we recommend selecting the "Trust the authors of all the
> files in the parent folder" option to prevent this warning from coming up
> every time you open a lesson. Just be sure to download your code from trusted
> sources!

[workspace-trust]: https://code.visualstudio.com/docs/editor/workspace-trust

### Running Tests

Most assignments will have tests that check your work and provide immediate
feedback in the terminal. We'll walk through some examples in upcoming lessons.

This assignment has a single test: check to see if you've correctly cloned this
assignment to your local machine. If you've followed the steps above, you've
completed everything you need to do to pass the test; all that is left to do is
run it.

Before you can run the test, you need to install a few dependencies with `npm`.
We will always provide you with the dependencies required for any given lesson
in the `package.json` file, so all you will have to do is run:

```sh
npm i
```

This will install everything that is needed for the assignment you're working on. 
Note that you will have to do this step for every assignment that provides a `package.json`. 

Once you have everything installed, you can now run the actual test with the command:

```sh
npm test
```

You'll then see the results of your test. For example, if you passed this 
assignment's test, you should see the following:

```console
This assignment
    ✓ has been correctly cloned to your local environment


  1 passing (5ms)
```

Before submitting an assignment, do your best to ensure all your tests are passing!

> **Note:** If you did not receive a passing test, or if your terminal produced
> some sort of error, walk through the steps in this lesson again and make sure
> you've followed each one. If you got a "command not found" error, make sure you
> have installed all dependencies with `npm i`. If you're still receiving errors,
> we recommend going back through the local environment setup instructions again 
> to ensure everything is set up properly.

### Saving your Work 

As you do work on the assignment and pass tests, we recommend you **save** your work, 
both locally and remotely. Saving locally is as simple as hitting **Ctrl + S** on Windows
or **Command + S** on Mac. Saving remotely, however, requires the use of git and GitHub.
We will learn more about both extensively by the end of this module, but for now you just 
need to know three main commands, in this order: 

1. `git add`
2. `git commit` 
3. `git push` 

`git add` will track all the work you've done in the files you tell it to track. 
For example, if we only wanted to track the work done in the `README.md` file, you could run:

```sh
git add README.md
``` 

If you want to track the work done in all files within a particular folder, you could run the following instead of adding each file individually: 

```sh
git add .
```

Note that where you run these commands in the terminal matter! You must be in the directory
that contains the files for the assignment. Typically, this means the folder that you 
cloned down earlier. For this assignment, that would be the `aws-completing-assignments` folder. 

Once you've tracked all the work you want to save, you can them commit to saving the 
changes with `git commit`. When you commit your work, you **must** include a message 
stating what work you've done in this commit. 

To include a message with your commit, the command is: 

```sh
git commit -m "your short message here"
```

We'll learn more about making good commits later on, but typically they should be succint.
For now, they can say things like "complete first test" or "finish tests 1-3" or similar.

Finally, now that you've tracked all the changes you made and committed them all to 
be saved, you can push those changes up to a remote location. This remote location 
typically will be the repository you forked earlier. To do so, you "push" the changes 
up with the following command: 

```sh
git push origin main
```

Again, we will cover what all these commands mean in more detail later in this module. 
For now, just know that you must run all three of these commands in this order before 
you submit any assignment. 

### Submitting an Assignment

Once the test is passing and you've pushed your work up to your forked copy, 
you can head back to the assignment on Canvas. While viewing the assignment,
you should see a **Submit Assignment** _or_ **Start Assignment** button in 
the upper-right section of the page.

![submit assignment button](https://curriculum-content.s3.amazonaws.com/canvas-welcome/submit-assignment-canvas.png)

Clicking this button will bring you to the bottom of the page where you can
submit a URL link to your work. The link you should submit is **your forked** 
version of the assignment. Make sure it's **your version** of the repo by 
ensuring the link includes your GitHub username in the URL.

![submit assignment form](https://curriculum-content.s3.amazonaws.com/canvas-welcome/submit-assignment-canvas-form.png)

Upon submission you should see confetti appear, indicating that your submission
has been accepted.

Each assignment will be different and will include instructions on what is
required to complete it. Some labs will have many tests. You can run
`npm test` as many times as you'd like while working to solve these labs. Just
don't forget to submit your GitHub repository link once you're done!

## Conclusion

Congratulations! You've completed your first assignment! You now know how to work on 
and submit assignments going forward:

- Click the **Fork** button on the Canvas assignment
- Once the assignment is forked, clone it down to your local machine
- Complete any required work, then run `npm i` and `npm test`
- As you complete tests, run the following three `git` commands to save your work remotely:
  - `git add .`
  - `git commit -m "short message here"`
  - `git push origin main`
- When all tests are passing, go back to the Canvas assignment and submit the link to
**your forked version** of the assignment's GitHub repo  

Equipped with this knowledge, you are now ready to tackle greater challenges!
