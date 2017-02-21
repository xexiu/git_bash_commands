# Git-pullrq v0.1

Description:
> Creates a pull request from the command line and automatically opens the browser with the new pull request created.
> Made for lazy people as me, preventing some extra clicks and navigating through windows.
> Made for people that like using command.

### Features

- Extends <a href="https://hub.github.com/ target="_blank">hub</a> pull request feature.
- Automatically creates a pull request and checksout master (optional).
- Perfect if your working with Jira tickets and auto transition between tasks. [take me to the details](#jira)
- If your are on branch master, it will abort mission, so no fears.


### Installation

```sh
$ cd ~/Desktop
$ git clone https://github.com/xexiu/git_bash_commands.git
$ sudo cp ~/Desktop/git_bash_commands/git-pullrq /opt/local/bin
```

> Refresh terminal or close/open it again.

### How to

- create new branch.
- Start working on it like normally.
- After you finish, make:

```sh
$ git-pullrq "this is my commit message"
```

- Optional: add "-m" to checkout directly master after you make the pull request.

```sh
$ git-pullrq "this is my commit message" -m
```

### <a name="jira"></a> Jira Tickets
> If your branch starts with: PRO-1234, GOL-1234, CUS-1234 or any other word followed by "-" then a number
> the commit made after you start the pull request (git-pullrq "commit message") will have the start name of the branch in
> order to be more specific when making commints for a ticket that you have in Jira.

For example:

```sh
$ git checkout -b "CUS-3242/mybranch"
```

> The commits made on that branch will have: "[CUS-3242] - my commit message".

### To do?

- Maybe auto assign it to a person from your organisation after the pull request is made.
- Extra param if you want to add a specific reviewer for pull request.
- Any suggestions/ideas are welcomed.
- ...

### Bonus

- You can add an alias on your `bash_profile` if you need. For example: `alias gpr='git-pullrq'`
- If you wish to have sound and more visual effects then install <a href="https://github.com/julienXX/terminal-notifier" target="_blank">terminal notifier</a>
