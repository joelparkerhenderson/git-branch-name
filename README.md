# Git branch name

This page has git branch name ideas that we've gathered. We welcome feedback.


## Git branch naming conventions


### Git commit message

Use direct imperative text, akin to a git commit message, that says what the branch does when it's merged, for example "add-login-button" or "fix-table-layout" or "optimize-page-speed". 

Benefits: easy to understand the purpose, easy for inter-team communications.


### Emoji

Use emoji to make a branch name that's akin to an icon, colorful, and fun, for example a branch that is a bug can use the bug emoji.

Benefits: easy to skim visually, fun for casual participants, creative.


### Issue number

Start the branch name with an issue number, for example your issue tracker has issue number 123, and the branch name could be "123-foo-bar".

Benefits: easy to jump between the issue tracker and the branch name.


### Version number

Start the branch name with a version number, for example a branch for version 1.0.0 could be "1.0.0-foo-bar".

Benefits: easy to see version ranges, group them, and also delete them when the version is done.


### Date-time stamp

Start the branch name with a date or time, for example a branch created on January 1 2020 could be "20200101-foo-bar".

Benefits: easy to see time ranges, group them, and also expire them after enough time has passed.


### Slash separator

Use a slash "/" to simulate a directory. Git branch names do not use directories, and many git clients and sites ignore the slash.

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


## See also

* [Git commit message](https://github.com/joelparkerhenderson/git_commit_message)

* [A successful git branching model by Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/)

* [How to organize your git branches by Darío Kondratiuk](https://dev.to/hardkoded/how-to-organize-your-git-branches-4dci)


TODO:

* [What are some examples of commonly used practices for naming git branches?](https://stackoverflow.com/questions/273695/what-are-some-examples-of-commonly-used-practices-for-naming-git-branches)

