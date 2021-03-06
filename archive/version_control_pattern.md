# Github-flow

### Github-Flow is a working practice that helps to:
1. Maintain overall code quality
2. Facilitate collaboration on a single project
3. Protect the codebase

We have tweaked it a little from what is [described on GitHub][1] 

### There are 6 steps to our process:
1. Create or clone a repo.
```sh
# For example, to clone this repo.
git clone git@github.com:moj-analytical-services/our-coding-standards.git
```

2. Create an issue in Github that describes what you're working on
To create an issue, use [the Github website](https://guides.github.com/features/issues/).

3. Create a new branch for the work you're about to do, with a name corresponding to the issue
```sh
# To create a new branch and switch onto it.
git checkout -b my-new-sensibly-named-branch
```

4. Make some commits on the new branch.
```sh
# Make some changes then stage each file you've changed - e.g. file1.txt and file2.txt.
git add file1.txt
git add file2.txt
# etc

# Commit your changes using a descriptive commit message.
git commit

# This will take you into your default text editor
# Write a descriptive commit message
```
>**Note:**
>If you have not configured your text editor, you may get stuck in Vim. You can exit using the following command: `:q!`. Then configure your default text editor for Git
```sh
git config --global core.editor <my-favourite-text-editor>
 # Then try again
git commit
```

5. When you're ready, submit a pull request and wait for peer-review.
```sh
# push your branch to the remote repo
git push origin my-new-sensibly-named-branch
# then go to github, open a PR and invite at least one reviewer
```
Make sure that you reference the issue in your pull request, by using the hash (#) symbol - see [here](https://help.github.com/articles/autolinked-references-and-urls/) for further guidance.  This makes it easy in future to see what changes were made to the code in response to the issue.

6. To make further changes, just make more commits on the same branch and push them to the remote repo again.

7. Once peer review is complete, and any comments addressed, merge into the master branch using a [rebase](https://github.com/blog/2243-rebase-and-merge-pull-requests).

8. The version of master on Github is now ahead of the version of master on your local machine.  Bring your local version up to date using `git checkout master`, `git pull`.  You are now in sync with Github, and ready to start a new branch.

The **master branch should be 100% functional at all times**, on any machine.  Please ensure it is [protected](https://help.github.com/articles/about-protected-branches/) and that your tests and / or linters run automatically on all pull requests.

For some further reading we strongly suggest reading this [article][2] that explains these git commands and others in a bit more detail.

If you want to test this out, clone this repo and make a contribution :)

[1]: https://guides.github.com/introduction/flow/
[2]: https://gist.github.com/blackfalcon/8428401
