# Git branch name

This page has git branch name ideas that we've gathered. We welcome feedback.

Contents:

* [Git branch naming conventions](#git-branch-naming-conventions)
  * [Git commit message](#git-commit-message)
  * [Emoji](#emoji)
  * [Issue number](#issue-number)
  * [Version number](#version-number)
  * [Date-time stamp](#date-time-stamp)
  * [Group names](#group-names)
  * [Workflow prefix](#workflow-prefix)
* [Name tokenization](#name-tokenization)
  * [Kebab case or snake case or camel case](#kebab-case-or-snake-case-or-camel-case)
  * [Slash separator](#slash-separator)
* [Git branch edit description](#git-branch-edit-description)
  * [Git alias](#git-alias)
* [See also](#see-also)


## Git branch naming conventions


### Git commit message

Use direct imperative text, akin to a git commit message, that says what the branch does when it's merged.

Examples:

* add-help-button

* fix-page-layout

* optimize-search-speed

Benefits: easy to understand the purpose, easy for inter-team communications.


### Emoji

Use a branch name with an emoji that's akin to an icon, colorful, and fun.

Examples:

* 🙂login-button (a smiling face emoji means add a feature)

* 🐛table-layout (a bug emoji means fix a bug)

* 🐇page-speed (a rabbit emoji means optimize an area to make it faster)


Benefits: easy to skim visually, fun for casual participants, creative.


### Issue number

Use a branch name with an issue number based on your issue tracker, for example your issue tracker has issue number 100 and your branch name could be "100-foo-bar".

Examples:

* 100-add-login-button

* 101-fix-table-layout

* 102-optimize-page-speed

Benefits: easy to jump between the issue tracker and the branch name.


### Version number

Use a branch name with a version number, for example a branch for version 1.0.0 could be "1.0.0-foo-bar".

Examples:

* 1.0.0-add-login-button

* 1.0.1-fix-table-layout

* 1.1.0-optmize-page-speed

Benefits: easy to see version ranges, group them, and also delete them when the version is done.


### Date-time stamp

Use a branch name with a date or time, for example a branch created on January 1 2020 could be "2020-01-01-foo-bar".

Examples:

* 2020-01-01-add-login-button

* 2020-01-02-fix-table-layout

* 2020-01-03-optimze-page-speed

Benefits: easy to see time ranges, group them, and also expire them after enough time has passed.


### Group name

Use a branch name with your own group names, for example authentication/authorization could use "aa", or user interface branch could use "ui", or optimization opportunities could use "oo".

Examples:

* aa-login-button

* ui-table-layout

* oo-page-speed

Benefits: easy to cluster by subteam, for example a security team looks at "aa", a design team looks at "ui", and a performance team looks at "oo".


### Workflow tag

Use a branch name with your own workflow tag name, for example work in progress could use the tag name "wip", or a branch ready for user acceptance testing could use the tag name "uat", or a temporarly research branch could start with the tag name "tmp".

Examples:

* wip-login-button

* uat-table-layout

* tmp-page-speed

Benefits: easy to understand in terms of customer delivery planning, if the teams are able to update their branch names as the branches reach various stages of delivery.


## Name tokenization


### Kebab case or snake case or camel case

Use a branch name with kebab case which means dashes, or snake case which means underscores, or camel case which means use upper-case letters instead of a separator characters.

Examples:

* add-login-button (kebab case)

* fix_table_layout (snake case)

* optimizePageSpeed (camel case)


### Slash separator

Use a slash "/" to simulate a directory and subdirectory.

Examples:

* features/login-button

* fixes/table-layout

* optmizations/page-speed

Benefits: if you use a git GUI client that treats a slash "/" as a directory separator, then you may enjoy this kind of organization.

Caveats: Git branch names do not use directories, and many git clients and sites ignore the slash. Branches are implemented as paths, so you cannot have a branch named "foo" and another branch named "foo/bar".


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

Our related repos:

* [Git commit message: how to write a great git commit message and commit template for version control](https://github.com/joelparkerhenderson/git_commit_message)

* [GitHub special files and paths, such as README, LICENSE, /.github, /docs](https://github.com/joelparkerhenderson/github_special_files_and_paths)

* [Git commit template for better commit messages](https://github.com/joelparkerhenderson/git_commit_template)


Git branch organization:

* [A successful git branching model by Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/)

* [How to organize your git branches by Darío Kondratiuk](https://dev.to/hardkoded/how-to-organize-your-git-branches-4dci)


Git alias ideas:

* [GitAlias](https://github.com/gitalias/gitalias)
