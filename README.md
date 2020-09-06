[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v1.4%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

# gitIntro

A skeleton repo for learning how to use GitHub and git.

Some useful links:

- [A guide to licences](https://help.github.com/en/articles/licensing-a-repository) How do I want people to be able to use my repo?
- [Github tutorials](https://guides.github.com) Useful short guides on different aspects of using GitHub and git.
- [A glossary of git terms](https://git-scm.com/docs/gitglossary) For distinguishing your _staging_ from _pushing_ and your _forking_ from _cloning_.
- [Download git](https://git-scm.com/downloads) For issuing git via the command-line.
- [Git Book](https://git-scm.com/book/en/v2) For a detailed and comprehensive guide to using git.
- [Tips on commit etiquette and best practices](https://hackernoon.com/git-it-together-some-tips-on-commit-etiquette-and-best-practices-for-junior-developers-1f147b8dfd56) from @Gunterja
- [Adding a code of conduct to your project](https://opensource.guide/code-of-conduct)

## An Introductory Exercise

### 1. Setting things up

- If you don't already have one, set up a free GitHub account by visiting [github.com](https://github.com) and clicking **Sign up for GitHub**.

- Ensure you have git running on your machine:

  To test, open a command prompt (Windows), terminal (MacOS) or shell (linux) and type:

  `git --help`

  If you see a page of help instructions you are good to go. If you receive a message like _git: command not found_ you will need to install git yourself:

  Visit [git-scm.com/downloads](https://git-scm.com/downloads) and follow the instructions for your platform. You can accept all the default options provided by the install program.

  Once installed, open a new command prompt/terminal/shell and check `git --help` works as expected.

### 2. Making a fork from someone else's repo

_This activity works best if you are completing it with someone else in order to see how to work together on a shared project. But if this is not practical, you can use this repo as the one you will fork._

- Open a new web page and open up a repo to fork (e.g. this one or a colleague who is following the same tutorial). This and other GitHub repos have the form `github.com/XXX/YYY` where `XXX` is the repo owner's GitHub account name and `YYY` is the name of the repo. This one is called [github.com/jwoLondon/gitIntro](https://github.com/jwoLondon/gitIntro)

- _Fork_ a copy of the repo by clicking the 'fork' link. This will create a copy of the repo in your own 'remote' GitHub space.

- Point your browser to this newly forked copy in your own GitHub space and click the green `Clone or download` button. Copy the URL provided, which will be something like _git<span>@github</span>.com:myAccountName/gitIntro.git_.

### 3. Working with a local copy of a remote repo

- Open a command prompt/terminal/shell and `cd` to a place where you would like to store a local copy of the remote repo.

- In the command window, type `git clone XXX` where _XXX_ is the reference you have just copied (_git<span>@github</span>.com:myUsername/gitIntro.git_). You can ctrl-v to paste it to the end of the line. This should download the repo from the remote location on GitHub and create a local copy of it on your computer. You can now make changes to this local copy that won't at this stage have any effect on the remote version sitting on GitHub.

- In your favourite editor create a new file called `myName.md` where _myName_ is your name without any spaces (e.g. `JoWood.md`). In this file, add some simple biographical details (that you are happy to be made public) and then save it.

### 4. Setting your identity

- Before you can commit and push files with git you will need to configure git with your identity. This should only be required once as the settings will be stored by git on your computer. From the command line, type:

  `git config --global user.email "me@myEmail.com"` (substituting your own email address)

  `git config --global user.name "my name"` (substituting your own name)

### 5. Pushing local changes back to a remote repo

- From the command line, ensure you are in the folder containing your local copy of the forked repo and then follow these three steps:

  `git add myName.md` (where _myName.<span>md</span>_ is the name of the file you have just created)

  This is called 'staging' and indicates the files that you wish to be considered for inclusion in your repo.

  `git commit --message "Add my biographical details"`

  Committing staged files is like taking a snapshot of your project at any stage in its development. The content in quotes after `--message` should be fewer than 50 characters in length and in the 'imperative voice' as if completing the sentence _"If accepted, this commit will..."_

  `git push`

  This is the act of transferring your most recent commit (snapshot of your project) to the remote repo. Assuming you haven't [set up an SSH key](https://help.github.com/en/articles/connecting-to-github-with-ssh), you will be asked to supply your GitHub credentials at this point.

  If you point a browser to your repo on GitHub and refresh the page, you should see your newly created file now listed as part of the repo.

### 6. Making a Pull Request (PR)

As a final step, you are going to make a request to the originator of the repo you forked asking them to incorporate the modifications you made to your version of it, back into their original version (If you have forked this repo, I will most likely reject PRs, but please feel free to make one in order to practice).

- With your browser pointing to your forked repo on GitHub, click the 'New Pull Request' button and give the PR a title such as “Add my bio details” and in the comment section add a rationale for your request, for example "I'd like to add my details to your repo so you can see my programming interests".

- Click the “Create Pull Request” button. This will send a message to the author of the repo you forked with the details of the changes you are requesting. It is now up to them to accept or reject your request. If they accept it, you will both now have a copy of a jointly authored repo!
