## Changelog

Generate release note pages from git commit history.

### Installation

It's preferable to install it globally through [`npm`](https://www.npmjs.com/package/git-release-notes)

    npm install -g git-release-notes

### Usage

The basic usage is

    cd <your_git_project>
    git-release-notes <since>..<until> <template>
    Examples:
        To generate markdown changelog: git-release-notes f6cf9a..575fef markdown > markdown2.ejs
        To generate web page changelog: git-release-notes f6cf9a..575fef html > changelog.html


##### Template Variables

Several template variables are made available to the script running inside the template.

`commits` is an array of commits, each containing

* `sha1` commit hash (%H)
* `authorName` author name (%an)
* `authorEmail` author email (%ae)
* `authorDate` author date (%aD)
* `committerName` committer name (%cn)
* `committerEmail` committer email (%ce)
* `committerDate` committer date (%cD)
* `title` subject (%s)
* `messageLines` array of body lines (%b)


