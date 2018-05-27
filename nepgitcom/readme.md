Git Cheat Sheet - Git-Flow [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
===============
<hr>
<p align="center">
	<img alt="Git" src="../Img/git-logo.png" height="190" width="455">
</p>
<hr>

# Other Available Languages:
1. [Arabic Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-ar.md)
2. [Chinese Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-zh.md)
3. [Hindi Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-hi.md)
4. [Turkish Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-tr.md)
5. [Spanish Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-es.md)
6. [Nepalese Git Cheat Sheet](empty)

Git cheat sheet saves you from learning all the commands by heart.

Be free to contribute, update the grammar mistakes. You are also free to add your language file.
<hr>

Git Cheat Sheet Nepalese
===============
###अनुक्रमणिका
* [सेटअप](#सेटअप-)
* [कन्फिगरेसन फाइलहरू](कन्फिगरेसन-फाइलहरू) 
* [सिर्जना](#सिर्जना)
* [स्थानीय परिवर्तनहरू](#स्थानीय-परिवर्तनहरू)
* [खोजी गर्नुहोस्](#खोजी-गर्नुहोस्)
* [कमिटि इतिहास](#कमिटि-इतिहास)
* [शाखाहरू र ट्यागहरू](#शाखाहरू-र-ट्यागहरू)
* [अपडेट र प्रकाशित](#अपडेट-र-प्रकाशित)
* [मर्ज र विस्थापन](#मर्ज-र-विस्थापन)
* [पूर्ववत](#पूर्ववत)
* [Git प्रवाह](#Git-प्रवाह)

<hr>

[###सेटअप](###सेटअप)                                                                 @@  गर्न
 को लागी


#####वर्तमान कन्फिगरेसन देखनु:
```
git config --list
```

#####भण्डार कन्फिगरेसन देखनु:
```
git config --local --list
```

#####विश्वव्यापी विन्यास देखनु:
```
git config --global --list
```

#####प्रणाली कन्फिगरेसन देखनु:
```
git config --system --list
```

#####संस्करण इतिहास पूर्वावलोकन गर्दा क्रेडिटको लागि पहिचान योग्य नाम सेट गर्न:
```
git config --global user.name “[firstname lastname]”
```

#####एक इमेल ठेगाना सेट गर्न जुन हरेक इतिहास मार्करसँग सम्बन्धित हुनेछ:
```
git config --global user.email “[valid-email]”
```

#####सजिलो समीक्षाको लागि Git को लागि स्वचालित आदेश रेखा रंग सेट गर्न:
```
git config --global color.ui auto
```

#####प्रतिबद्धताको लागि वैश्विक सम्पादक सेट गर्न:
```
git config --global core.editor vi
```

<hr>

[##कन्फिगरेसन फाइलहरू](##कन्फिगरेसन-फाइलहरू)

#####भण्डार विशिष्ट कन्फिगरेसन फाइल [--local]:
```
<repo>/.git/config
```

#####प्रयोगकर्ता-विशिष्ट कन्फिगरेसन फाइल [--global]:
```
~/.gitconfig
```

#####प्रणाली-विस्तृत विन्यास फाइल [--system]:
```
/etc/gitconfig
```

<hr>

[##सिर्जना](##सिर्जना)

#####अवस्थित भण्डार क्लोन गर्न:

त्यहाँ दुई तरिकाहरू छन्:

को द्वारा SSH

```
git clone ssh://user@domain.com/repo.git
```

को द्वारा HTTP

```
git clone http://domain.com/user/repo.git
```

#####नयाँ स्थानीय भण्डार सिर्जना गर्न:
```
git init
```

<hr>

[##स्थानीय परिवर्तनहरू](##स्थानीय-परिवर्तनहरू)


#####काम गर्ने निर्देशिकामा परिवर्तनहरू:

```
$ git status
```

#####ट्रयाक गरिएका फाइलहरूमा परिवर्तनहरू:

```
$ git diff
```

#####अर्को प्रतिबद्धताहरूमा सबै वर्तमान परिवर्तनहरू थप्नु:

```
$ git add .
```

#####& Lt; फाइल & gt; मा केहि परिवर्तनहरू थप्नु। अर्को प्रतिबद्धतामा:

```
$ git add -p <file>
```

#####ट्रयाक गरिएका फाइलहरूमा सबै स्थानीय परिवर्तनहरू प्रतिबद्ध गर्नु:

```
$ git commit -a
```

#####पहिलेको प्रतिबद्धता परिवर्तन भयो:

```
$ git commit
```

#####सन्देशसँग प्रतिबद्धता गर्न:

```
$ git commit -m 'message here'
```

#####स्टेजिंग क्षेत्र छोड्दै र सन्देश थप्न प्रतिबद्ध गर्न:

```
$ git commit -am 'message here'
```

#####केही अघिल्लो मितिमा प्रतिबद्धता गर्न:

```
git commit --date="`date --date='n day ago'`" -am "Commit Message"
```

#####अन्तिम प्रतिबद्धता परिवर्तन गर्न:<br>
<em><sub>प्रकाशित प्रतिबद्धताहरू संशोधन नगर्नुहोस्!</sub></em>

```
$ git commit -a --amend
```

#####अन्तिम प्रतिबद्धताको कमेटर मिति बदल्नु:

```
GIT_COMMITTER_DATE="date" git commit --amend
```

#####अन्तिम प्रतिबद्धताको मिति लेखक परिवर्तन गर्नु:

```
git commit --amend --date="date"
```

#####हालको शाखाबाट कुनै अन्य शाखामा असामान्य परिवर्तनहरू सार्नु:<br>
```
git stash
git checkout branch2
git stash pop
```

#####विफलता परिवर्तनहरू हालको शाखामा पुनःस्थापित गर्नु:

```
git stash apply
```

#####विफलताको अन्तिम सेट हटाउनु:

```
git stash drop
```

<hr>

[##खोजी](#खोजी)

#####डाइरेक्टरीमा सबै फाइलहरूमा पाठ खोज:

```
git grep "Hello"
```

#####पाठ खोजीको कुनैपनि संस्करणमा:

```
$ git grep "Hello" v2.5
```

<hr>

[###Commit History](##कमिटि-इतिहास)

#####सबै कमिटिहरू देखाउनुहोस्, नयाँसँग सुरू गर्नुहोस् (यसले हैश, लेखक जानकारी, प्रतिबद्धताको मिति र प्रतिबद्धताको शीर्षक देखाउनेछ:
```
$ git log
```

#####सबै कमेन्टहरू देखाउनुहोस् (यसले केवल प्रतिबद्ध हैश र प्रतिबद्ध सन्देश देखाउनेछ):

```
$ git log --oneline
```

#####एक विशिष्ट प्रयोगकर्ताको सबै कमेन्टहरू देखाउनुहोस्:

```
$ git log --author="username"
```

#####विशिष्ट फाइलको लागि समयको साथ परिवर्तनहरू देखाउनुहोस्:

```
$ git log -p <file>
```

#####प्रदर्शन गर्दछ जुन केवल दायाँ तिर रिमोट / शाखामा उपस्थित छ

```
$ git log --oneline <origin/master>..<remote/master> --left-right
```

#####कसले परिवर्तन गर्यो, के र कहिले &lt;file&gt;:
```
$ git blame <file>
```

#####सन्दर्भ लगाउनुहोस्:

```
$ git reflog show 
```

#####सन्दर्भ लग इन गर्नुहोस्:

```
$ git reflog delete
```
<hr>

[##Branches & Tags](##शाखाहरू-र-ट्यागहरू)

#####सबै स्थानीय शाखाहरू सूचीबद्ध गर्नुहोस्:

```
$ git branch
```

#####सबै रिमोट शाखाहरू सूचीबद्ध गर्नुहोस्:

```
$ git branch -r
```

#####HEAD शाखा स्विच गर्नुहोस्:

```
$ git checkout <branch>
```

#####नयाँ शाखा बनाउनुहोस् र स्विच गर्नुहोस्:

```
$ git checkout -b <branch>
```

#####तपाईंको वर्तमान HEAD मा आधारित नयाँ शाखा सिर्जना गर्नुहोस्:

```
$ git branch <new-branch>
```

#####रिमोट शाखामा आधारित नयाँ ट्र्याकिङ शाखा सिर्जना गर्नुहोस्:

```
$ git branch --track <new-branch> <remote-branch>
```

#####स्थानीय शाखा मेटाउनुहोस्:

```
$ git branch -d <branch>
```

#####स्थानीय शाखालाई हटाउनुहोस्:

<em><sub>तपाईंले अनमर्जित परिवर्तन गुमाउनुहुनेछ!</sub></em>

```
$ git branch -D <branch>
```

#####ट्यागको साथ वर्तमान प्रतिबद्धता चिन्ह लगाउनुहोस्:

```
$ git tag <tag-name>
```

#####एक सन्देश समावेश गर्ने ट्यागको साथ वर्तमान प्रतिबद्धता चिन्ह लगाउनुहोस्:

```
$ git tag -a <tag-name>
```
<hr>

[##अपडेट र प्रकाशित](##अपडेट-र-प्रकाशित)


#####सबै हालको कन्फिगर गरिएको सम्झौताहरू सूचीबद्ध गर्नुहोस्:

```
$ git remote -v
```

#####टाढाको बारेमा जानकारी देखाउनुहोस्:

```
$ git remote show <remote>
```

#####नयाँ रिमोट भण्डार थप्नुहोस्, नाम & lt; रिमोट & gt ;:

```
$ git remote add <remote> <url>
```

#####& Lt; रिमोट & gt; बाट सबै परिवर्तनहरू डाउनलोड गर्नुहोस्, तर HEAD मा एकीकृत नगर्नुहोस्:

```
$ git fetch <remote>
```

#####परिवर्तनहरू डाउनलोड गर्नुहोस् र सीधा मा सीधा मर्ज / एकीकृत गर्नुहोस्:

```
$ git remote pull <remote> <url>
```

#####HEAD बाट सबै परिवर्तनहरू स्थानीय भण्डारमा प्राप्त गर्नुहोस्:

```
$ git pull origin master
```

#####Get all changes from HEAD to local repository without a merge:
```
git pull --rebase <remote> <branch>
```

#####Publish local changes on a remote:
```
$ git push remote <remote> <branch>
```

#####Delete a branch on the remote:
```
$ git push <remote> :<branch> (since Git v1.5.0)
or
git push <remote> --delete <branch> (since Git v1.7.0)
```

#####Publish your tags:
```
$ git push --tags
```
<hr>
##Merge & Rebase

#####Merge <branch> into your current HEAD:
```
$ git merge <branch>
```

#####Rebase your current HEAD onto &lt;branch&gt;:<br>
<em><sub>Don't rebase published commit!</sub></em>

```
$ git rebase <branch>
```

#####Abort a rebase:
```
$ git rebase --abort
```

#####Continue a rebase after resolving conflicts:
```
$ git rebase --continue
```

#####Use your configured merge tool to solve conflicts:
```
$ git mergetool
```

#####Use your editor to manually solve conflicts and (after resolving) mark file as resolved:
```
$ git add <resolved-file>
```

```
$ git rm <resolved-file>
```

#####Squashing commits:
```
$ git rebase -i <commit-just-before-first>
```

Now replace this,

```
pick <commit_id>
pick <commit_id2>
pick <commit_id3>
```

to this,

```
pick <commit_id>
squash <commit_id2>
squash <commit_id3>
```
<hr>
##Undo

#####Discard all local changes in your working directory:
```
$ git reset --hard HEAD
```

#####Get all the files out of the staging area(i.e. undo the last `git add`):
```
$ git reset HEAD
```

#####Discard local changes in a specific file:
```
$ git checkout HEAD <file>
```

#####Revert a commit (by producing a new commit with contrary changes):
```
$ git revert <commit>
```

#####Reset your HEAD pointer to a previous commit and discard all changes since then:
```
$ git reset --hard <commit>
```

#####Reset your HEAD pointer to a remote branch current state.
```
git reset --hard <remote/branch> e.g., upstream/master, origin/my-feature
```

#####Reset your HEAD pointer to a previous commit and preserve all changes as unstaged changes:
```
$ git reset <commit>
```

#####Reset your HEAD pointer to a previous commit and preserve uncommitted local changes:
```
$ git reset --keep <commit>
```

#####Remove files that were accidentally committed before they were added to .gitignore
```
$ git rm -r --cached .
$ git add .
$ git commit -m "remove xyz file"
```
<hr>

##Git-Flow

###Index
* [Setup](#setup)
* [Getting Started](#getting-started)
* [Features](#features)
* [Make a Release](#make-a-release)
* [Hotfixes](#hotfixes)
* [Commands](#commands)
<hr>


###Setup
######You need a working git installation as prerequisite. Git flow works on OSX, Linux and Windows.

#####OSX Homebrew:
```
$ brew install git-flow
```

#####OSX Macports:
```
$ port install git-flow
```

#####Linux (Debian-based):
```
$ apt-get install git-flow
```

#####Windows (Cygwin):
######You need wget and util-linux to install git-flow.
```
$ wget -q -O - --no-check-certificate https://github.com/nvie/gitflow/raw/develop/contrib/gitflow-installer.sh | bash
```
<hr>


###Getting Started
######Git flow needs to be initialized in order to customize your project setup. Start using git-flow by initializing it inside an existing git repository:
#####Initialize:
######You'll have to answer a few questions regarding the naming conventions for your branches. It's recommended to use the default values.
```
git flow init
```
<hr>


###Features
######Develop new features for upcoming releases. Typically exist in developers repos only.
#####Start a new feature:
######This action creates a new feature branch based on 'develop' and switches to it.
```
git flow feature start MYFEATURE
```

#####Finish up a feature:
######Finish the development of a feature. This action performs the following:
######1)Merged MYFEATURE into 'develop'.
######2)Removes the feature branch.
######3)Switches back to 'develop' branch
```
git flow feature finish MYFEATURE
```

#####Publish a feature:
######Are you developing a feature in collaboration? Publish a feature to the remote server so it can be used by other users.
```
git flow feature publish MYFEATURE
```

#####Getting a published feature:
######Get a feature published by another user.
```
git flow feature pull origin MYFEATURE
```

#####Tracking a origin feature:
######You can track a feature on origin by using
```
git flow feature track MYFEATURE
```
<hr>


###Make a Release
######Support preparation of a new production release. Allow for minor bug fixes and preparing meta-data for a release

#####Start a release:
######To start a release, use the git flow release command. It creates a release branch created from the 'develop' branch. You can optionally supply a [BASE] commit sha-1 hash to start the release from. The commit must be on the 'develop' branch.
```
git flow release start RELEASE [BASE]
```
######It's wise to publish the release branch after creating it to allow release commits by other developers. Do it similar to feature publishing with the command:
```
git flow release publish RELEASE
```
######(You can track a remote release with the: ```git flow release track RELEASE``` command)

#####Finish up a release:
######Finishing a release is one of the big steps in git branching. It performs several actions:
######1)Merges the release branch back into 'master'
######2)Tags the release with its name
######3)Back-merges the release into 'develop'
######4)Removes the release branch
```
git flow release finish RELEASE
```
######Don't forget to push your tags with ```git push --tags```
<hr>


###Hotfixes
######Hotfixes arise from the necessity to act immediately upon an undesired state of a live production version. May be branched off from the corresponding tag on the master branch that marks the production version.

#####Git flow hotfix start:
######Like the other git flow commands, a hotfix is started with
```
$ git flow hotfix start VERSION [BASENAME]
```
######The version argument hereby marks the new hotfix release name. Optionally you can specify a basename to start from.

#####Finish a hotfix:
######By finishing a hotfix it gets merged back into develop and master. Additionally the master merge is tagged with the hotfix version
```
git flow hotfix finish VERSION
```
<hr>


###Commands
<p align="center">
    <img alt="Git" src="../Img/git-flow-commands.png" height="270" width="460">
</p>
<hr>

###Git flow schema

<p align="center">
    <img alt="Git" src="../Img/git-flow-commands-without-flow.png">
</p>
<hr>







































