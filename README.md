# Git-pullrq v0.1

Description:
> Creates a pull request from the command line and automatically opens the browser with the new pull request created.
> Made for lazy people as me, preventing some extra clicks and navigating through windows.
> Made for people that like using command.

### Features

- Extends [hub](https://hub.github.com/ target="_blank") pull request feature.
- Automatically creates a pull request and checksout master (optional).
- Perfect if your working with Jira tickets and auto transition between tasks. [1](#jira)
- If your are on branch master, it will abort mission, so no fears.


### Installation

```sh
$ cd ~/Desktop
$ git clone https://github.com/xexiu/git_bash_commands.git
$ sudo cp ~/Desktop/git_bash_commands/git-pullrq /opt/local/bin
```

- Refresh terminal or close/open it again.

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
``

### <a name="jira"></a> Jira Tickets
> If your branch starts with: PRO-1234, GOL-1234, CUS-1234 or any other word followed by "-" then a number
> the commit/s made after will have the start name of the branch in
> order to be more specific when making commints for a ticket that you have in Jira.

For example:

```sh
$ git checkout -b "CUS-3242/mybranch"
```

> The commits made on that branch will have: "[CUS-3242] - my commit message".
