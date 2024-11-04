![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document - morning

2024-10-29 ds-git.

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

##  🫱🏽‍🫲🏻 Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.
 
If there is any problem we can't solve directly: please mail [teaching@esciencecenter.nl](mailto:teaching@esciencecenter.nl).

## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, just raise your hand.

If you need help from a helper, place a pink post-it note on your laptop lid. A helper will come to assist you as soon as possible.

## 🖥 Workshop website

[link](https://esciencecenter-digital-skills.github.io/2024-10-29-ds-git/)

🛠 Setup

[link](https://esciencecenter-digital-skills.github.io/2024-10-29-ds-git#setup)

## 🗓️ Agenda
| Time | Topic |
|--:|:---|
| 10:45 | Welcome |
| 10:50 | Introduction to Git, setting up Git |
| 11:30 | Coffee break |
| 11:45 | Creating a repository, tracking changes |
| 12:30 | Lunch |

| Time | Topic |
|--:|:---|
| 13:30 | Welcome |
| 13:35 | Remotes in Github |
| 14:15 | Coffee break |
| 14:30 | Collaboration with Git and Github |
| 15:15 | END |

## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl.
Please request your certificate within 8 months after the workshop, as we will delete all personal identifyable information after this period.

## 🔧 Exercises

## 🧠 Collaborative Notes

Open your terminal.

- On Windows: Git Bash
- On Mac: find terminal
- On Linux: depends

### Git Setup

Set your name (in human readable form)

```bash
git config --global user.name "Your Name"
```

Set your email

```bash
git config --global user.email "your.name@company.where"
```

You can check you existing config

```bash
git config list
```

Set the default editor

```bash
git config --global core.editor "nano -w"
```

Set the default branch name

```bash
git config --global init.defaultBranch main
```

Open your configuration in an editor

```bash
git config --global --edit
```

### Create a new project

We will create a new project folder in a place that you like, for instance the `Desktop` folder. If you like `Documents` better, thats also fine.

```bash
cd ~/Desktop
```

Create a new directory (**m**a**k**e **dir**)

```bash
mkdir planets
```

Enter that directory (**c**hange **d**ir)

```bash
cd planets
```

Initialize the Git repo

```bash
git init
```

### Query status

:::info
You will use 

```bash
git status
```

very very often.
:::

List files in your repo

```bash
ls
```

To see **all** of them

```bash
ls -a
```

### Add content

Open any plain text editor to edit a text file (see [Resources](#%F0%9F%93%9A-Resources)), we keep using `nano` here.

```bash
nano mars.txt
```

:::info
Add the file to Git

```bash
git add mars.txt
```

Check the status (`git status`)

Create a commit

```bash
git commit -m 'Start notes on Mars as a base'
```
:::

Check the status (`git status`), should now be "working tree clean".

### Make modifications

Edit `mars.txt`.

:::info
See your changes:

```bash
git diff
```
:::

Record changes again

```bash
git add mars.txt
git commit -m 'Add concerns about the two moons'
```

Check your status again! (`git status`)

### View history

:::info
View the history of all commits

```bash
git log
```
:::

### Working with directories

Create some files in a sub-directory.

```bash
mkdir spaceships
cd spaceships
touch apollo-11.txt
touch sputnik-1.txt
```

Add the changes `git add spaceships` and check the status `git status`. All files were added to the repo. Commit changes.

### Compare older versions

We can use `git diff` a bit better to view changes since some previous commit. 

```bash
git diff HEAD~2 mars.txt
```

This will show the difference between now and two commits ago.

Check your log using `git log`. Pick a commit and copy the commit id (the long hexadecimal thing).

```bash
git diff 1234567890abcdef mars.txt
```

Now you'll see the changes since the selected commit.

### Undo changes

:::info
Restore a file to the latest committed version.

```bash
git restore mars.txt
```
:::

---

### Setting up an SSH key for GitHub

The easiest way to let your computer talk to GitHub is to set up an SSH key. To create a key, you can follow these [instructions by GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

Once created, you can use the following command to print your public SSH key:

```bash
cat ~/.ssh/id_ed25519.pub
```
Then you can copy the output and add it as a new key in the [Settings/SSH Keys](https://github.com/settings/keys) page of your GitHub account. As a title, it is recommended to put a recognisable name for your current computer, so you know which key to remove if you ever have to replace your computer.

To confirm it it has worked, you can try the following command:

```bash
ssh -T git@github.com
```

It should reply with something like `Hi <username>, you've succesfully authenticated!`.

### Remotes

:::info
Clone

```bash
git clone <url>
```

Push

```bash
git push origin main
```

Pull

```bash
git pull origin main
```
:::


### Ignoring changes

You can list files that should never be committed to the repo to a special file called `.gitignore`. See [the GitHub docs](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files).




## 📚 Resources

Text editors for beginners:

- [Microsoft VSCode](https://code.visualstudio.com/)
- [Notepad++](https://notepad-plus-plus.org/)

