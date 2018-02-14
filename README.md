# Welcome to the SSXG Website

*The official website of the Solar System Exploration Group at the University of Toronto*

## Visitors

If you are here by mistake, [click here](https://uoftssxg.github.io/) to return to the website.

## Contributors

This site is made with [GitHub Pages](https://pages.github.com/) and [Jekyll](https://jekyllrb.com/docs/home/).

### Getting started

First install Jekyll by following the instructions [here](https://jekyllrb.com/docs/installation/) (or [here](https://jekyllrb.com/docs/windows/) if you are on Windows). Next you need to clone the repository locally. With git installed, type the following into the terminal:

```
git clone https://github.com/uoftssxg/uoftssxg.github.io.git
```

### Testing the website

Hopefully the above links helped you install (or update) Ruby, bundler and jekyll. Bundler ensures that the site's dependencies are up to date and Jekyll allows you to build the site on your computer to test it out. To do this, run:

```
bundle exec jekyll serve
```

This will compile the website on your computer, and make it accessible from any web browser at the address [http://localhost:4000](http://localhost:4000).

This is a great risk-free way to check how your features look as you develop them. You can even make changes to the *HTML, Javascript, or CSS* files and see them update live by refreshing the page.

When you are finished you can type **CTRL** + **c** to interrupt the Jekyll server.

*Note:* if you make any changes to the setup files, e.g. *_config.yml*, you will need to interrupt the Jekyll server and then compile it again from scratch with another **bundle exec jekyll serve**.

### Making changes

We use a style of git-fu called the *feature-branch* workflow (described in detail [here](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)). It consists of the following steps:

1) Make a new branch locally for your changes. All changes should happen on a dedicated branch, *never on master*

```
git checkout -b new-feature
```

2) Update files on your **new-feature** branch, then add and commit

```
git status
git add <your-files>
git commit -m "Add xyz feature or Fix #123 bug"
```

3) Push your local branch to GitHub. If this is the first time you are pushing type

```
git push -u origin new-feature
```

If you have already pushed and therefore the **new-feature** branch already exists on GitHub, type

```
git push -f
```

4) Open a [pull request](https://help.github.com/articles/about-pull-requests/) on GitHub for your branch to be merged into master

5) Other contributor(s) will review and comment on your merge. If they suggest any fixes, you may need to make adjustments and redo steps 2 and 3 (don't worry your pull request will still exist). When all discussions are resolved, your branch will be merged into master

6) Now that master has been updated, all contributors (including you) will need to update their local repositories with

```
git checkout master
git pull
```

**Note:** When collaborators are working simultaneously, this workflow requires two extra mini-steps (it is good to get into a habit of always inserting these steps just in case).

2b) After your changes are comitted locally, but before you push them to GitHub, check that your local master branch is up to date

```
git checkout master
git pull
```

2c) If any changes were pulled, you will need to update your **new-feature** branch to bring it up to speed with the latest changes on master

```
git checkout new-feature
git rebase master
```

2d) If any of the same lines were changed in master and also on your branch, you will need to resolve a [merge conflict](https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/). To do this, open the files that **git status** says are conflicted, remove the `<<<<<< ======= >>>>>>>` junk that was added and keep only the parts that you wish to keep in your final version. When you are ready, continue the rebase with

```
git rebase --continue
```

3-6) Now you can push your rebased branch and finish the steps normally.

## Acknowledgements

This website was made possible by the fine folks at [HTML5up](https://html5up.net) using the [spectral](https://html5up.net/spectral) theme published by @arkadianriver [here](https://github.com/arkadianriver/spectral).

## LICENCE

This work is provided under the Creative Commons Attribution 3.0 Public License. See [LICENSE](LICENSE.txt) for more details.
