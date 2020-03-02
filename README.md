# Git branch name

This page has git branch name ideas that we've gathered. We welcome feedback.

Contents:

* [Git branch naming conventions](#git-branch-naming-conventions)
  * [Git commit message](#git-commit-message)
  * [Emoji](#emoji)
  * [Issue number](#issue-number)
  * [Version number](#version-number)
  * [Date-time stamp](#date-time-stamp)
  * [Slash separator](#slash-separator)
* [Git branch edit description](#git-branch-edit-description)
  * [Git alias](#git-alias)
* [See also](#see-also)


## Git branch naming conventions


### Git commit message

Use direct imperative text, akin to a git commit message, that says what the branch does when it's merged.

Examples:

* add-login-button

* fix-table-layout

* optimize-page-speed

Benefits: easy to understand the purpose, easy for inter-team communications.


### Emoji

Use emoji to make a branch name that's akin to an icon, colorful, and fun.

Examples:

* 🙂login-button (a smiling face emoji means add a feature)

* 🐛table-layout (a bug emoji means fix a bug)

* 🐇page-speed (a rabbit emoji means optimize an area to make it faster)


Benefits: easy to skim visually, fun for casual participants, creative.


### Issue number

Start the branch name with an issue number based on your issue tracker, for example your issue tracker has issue number 100 and your branch name could be "100-foo-bar".

Examples:

* 100-add-login-button

* 101-fix-table-layout

* 102-optimize-page-speed

Benefits: easy to jump between the issue tracker and the branch name.


### Version number

Start the branch name with a version number, for example a branch for version 1.0.0 could be "1.0.0-foo-bar".

Examples:

* 1.0.0-add-login-button

* 1.0.1-fix-table-layout

* 1.1.0-optmize-page-speed

Benefits: easy to see version ranges, group them, and also delete them when the version is done.


### Date-time stamp

Start the branch name with a date or time, for example a branch created on January 1 2020 could be "2020-01-01-foo-bar".

Examples:

* 2020-01-01-add-login-button

* 2020-01-02-fix-table-layout

* 2020-01-03-optimze-page-speed

Benefits: easy to see time ranges, group them, and also expire them after enough time has passed.


### Slash separator

Use a slash "/" to simulate a directory. Git branch names do not use directories, and many git clients and sites ignore the slash.

Examples:

* features/login-button

* fixes/table-layout

* optmizations/page-speed

Benefits: if you use a git GUI client that treats a slash "/" as a directory separator, then you may enjoy this kind of organization.


## Git branch edit description

To add more information to a branch, we edit the branch description, for example to say the purpose of the branch, or contact information for the maintainers, or links to issue tracker items.

To edit a branch description:

```sh
git branch --edit-description
```

To see a branch description:

```sh
git config branch.<name>.description
```

To set a branch description to one line:

```sh
git config branch.<name>.description "This is an example description"
```


### Git alias

To use a git alias, edit your git config file (such as `~/.gitconfig`) and add these git aliases:


```sh
bd = !"git config branch.$(git rev-parse --abbrev-ref HEAD 2>/dev/null).description"
be = branch --edit-description
```

To set the current branch description:

```sh
git bd "This is an example branch"
```

To see the current branch description:

```sh
git bd
```

To edit the current branch description:

```sh
git be
(launches your editor)
```


## See also

* [Git commit message](https://github.com/joelparkerhenderson/git_commit_message)

* [A successful git branching model by Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/)

* [How to organize your git branches by Darío Kondratiuk](https://dev.to/hardkoded/how-to-organize-your-git-branches-4dci)


TODO:

* [What are some examples of commonly used practices for naming git branches?](https://stackoverflow.com/questions/273695/what-are-some-examples-of-commonly-used-practices-for-naming-git-branches)

