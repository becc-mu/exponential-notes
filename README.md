# exponential-notes

The aim was to build this single page app notes using self rendering components, similar to React. However we were restricted using vanilla javascript without any third party framework which meant we had to create our own test suite in order to test drive the development.

To guide the team on how to write these components this example [repo](https://github.com/becc-mu/component-example) was created.

## Collaboration processes

### Branching

Before starting work on a new issue it is important that a new branch is made off the master which can then be used for making changes and submitting a pull request with which, after code review, will merge back into the master.

how to create a branch locally

Check you are currently in the master branch

```
$ git checkout master
```

Fetch the latest data from github

```
$ git fetch origin
```

Pull the master branch so that it’s at the latest commit

```
$ git pull
```

Make the new branch (e.g. add-note)

```
$ git branch add-note
```

Checkout the branch

```
$ git checkout add-note
```

When making commits it is useful to include in the commit messsge which issues have been fixed. This will enable all issues and projects to be automatically updated accordingly. An example of this would be a commit message like this:

```
fixes #45
fixes #63
```
“fixes” is a keyword which is required for this to work. [github guidance on this](https://help.github.com/articles/closing-issues-using-keywords/)

For the first push the upstream flag needs to be used.

```
$ git push -u origin add-note
```

### Preparing a Pull Request

on your local machine
At this point it is important to resolve the conflicts on the branch to be merged.

Fetch the latest master

```
$ git fetch —-all
```
Merge the master into the branch (e.g. add-note <= master)

```
$ git merge master
```
(NB ensure you are still checked out in the correct branch and not the master).

Any conflicts will now be highlighted. Once the conflicts are resolved locally the branch can be pushed.

```
$ git push
```
### on github
request pull request. (e.g. master <= add-note) make sure to include in the comments section of pull request all the issue ID's for the relevant issues. This will automatically update the status in the project.

Request review by assigning to another member of the team - ideally who wasn't involved in writing the code.

