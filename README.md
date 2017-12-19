# git-task
Simple task management for Git

Manages a list of tasks for the branch you're working on in a Markdown file,
and uses those tasks as commit messages.

Meant to be used as a way to keep track of tasks you want to do within a PR.

## Installation

This is a simple Bash script for the time being, place it on your path and
use it with `git task`.

## Usage

This records tasks in a file called `WIP.md` at the root of the repository.

Available commands:

`add`

Add a task to do as part of this branch. Creates the WIP.md file if it
does not exist.

`current`

Show the current task. This is considered to be the first task in WIP.md
that is not marked as done.

`done`

Update the `WIP.md` file to mark the current task as done, and do a commit
with the current task as a message. If all tasks are done, the `WIP.md`
file is deleted prior to committing.

`list`

Lists all tasks.

`pre-commit`
`prepare-commit-msg`

Commands meant to be used as part of the corresponding Git hooks. Their
combination is basically equivalent to `git task done`.
