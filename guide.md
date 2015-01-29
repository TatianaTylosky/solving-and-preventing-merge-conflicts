##Solving & Preventing Merge Conflicts
<img src="https://octodex.github.com/images/Professortocat_v2.png" width="200" />

The purpose of this overview is to teach you how to make pull requests and solve merge conflicts for the TF curriculum or code base.

##Table of Contents

* [TF Branches Overview](#TFBranches)
  * [Curric team](#curriculumbranches)
  * [Eng team](#engbranches)
* [Merge Conflicts](#mergeconflicts)
  * [What are they?](#whatarethey)
  * [Why do they happen?](#whymergeconflicts)
* [Prevention by best practices](#prevention)
  * [Making a Good Pull Request](#pullrequests)
  * [Overview](#overview)
* [Solving Merge Conflicts](#solving)
  * [Walkthrough](#walkthrough)
  * [Magical tricks to use](#tricks)

<a name="TFBranches"></a>
##TF Branches
Branches are copies of the same project that can exist either on Github
or locally on your computer. They allow multiple people to work on a project at the same time. After the work has been completed on a branch it is then merged back into the main project branch (called "preview" for curriculum and "develop" for engineering). After the **preview** or **develop** branch has been made stable a course lead or engineer will merge it with the **master** branch.

<a name="curriculumbranches"></a>
###Curriculum Branches
Thinkful's curriculum is set up so that multiple contributors can work on
separate branches that are then merged together by a course lead.

Example:
Fix-typo branch --> preview branch --> master branch

Naming convention:
Please use your name and then a couple words describing what you are
doing. For ex:

<code>tati-fix-typo</code>
<code>courtney-add-android</code>

![](http://i.imgur.com/bf4hpLn.png)

<a name="engbranches"></a>
###Eng Branches
Thinkful's code base ??? some comment here?

Example:
feature/python-guide branch --> develop branch --> master branch

![](http://i.imgur.com/mJu0BdQ.png)

<a name="mergeconflicts"></a>
##Merge Conflicts

<a name="whatarethey"></a>
###What is a Merge Conflict?

When Github doesn't know how to merge your updated branch with the main branch
you will get a merge conflict. Usually this means a project has been
modified at the same place in the two branches you are trying to merge.

![](http://i.imgur.com/vCkvoEo.png)

<a name="whymergeconflicts"></a>
###Why do Merge Conflicts Occur?

1. Someone updated the preview branch by merging new code while you were
   working on your branch

2. AND you modified the **same** line of code that they did.

***Github is NOT smart enough to know which version you want.***

<a name="prevention"></a>
##Prevention by Best Practices

<a name="pullrequests"></a>
### How to make good pull requests

There are three ways that TF currently makes pull requests depending on
the situation.

A) Quick updates for curriculum for those with write access

  If you see a typo or would like to make a quick change you can do
this directly on gitub.com. Go to the correct repo and file and edit the
<code>preview</code> branch directly using Github's editor. Click the
pencil icon to edit the file.

![](http://i.imgur.com/TcgzQ4f.png)

B) Curric writers and TF employees with write access

  It is important to pull, commit and merge OFTEN! Everytime you leave
your computer (within reason) you should do ALL of the following
instructions.

1. Communicate with others and let them know what you are working on.

2. In your terminal Use git clone and copy paste the SSH URL. You will clone the preview branch by default (which is good). For example, <code>git clone git@github.com:Thinkful-Ed/android.git</code> **NOTE: If you already have the repo cloned on your computer then just use <code>git pull origin preview</code> to make sure your local files are up to date.**

3. Create a new branch and name it appropriately.
   For example, <code>git checkout -B tati-edits</code>

4. Locally make edits to this new branch in the text editor of your
   choosing.
   **NOTE: If you need to make changes to file names you need speak with a course lead. If you are a course lead you need to make sure all other pull request have been merge.**

  As time passes you should do <code>git pull origin preview</code> to get the latest
updates on the Thinkful preview branch. This will not overwrite your
local updates.

5. Do <code>git status</code> in order to see the file you have changed. Then use <code>git add name-of-edited-file</code> to all the files you modified. Then do <code>git commit -m "Informative commit message"</code>.

6. Push your new branch with the changes to the Thinkful repo. For
   example, <code>git push origin tati-edits</code>

7. Go to the github to the Thinkful repository and click the green
   compare and pull request button.

8. By default you are probably comparing the correct branches. Just in case take a look. REMEMBER: You want Do not compare with Compare <code>base fork: Thinkful-Ed/curric..base: preview</code> to <code>head fork: Thinkful-Ed/curric..base: tati-edits</code>

9. Check to see if your branch can be automatically merge. If it can
   then let a course lead review it! If you have a merge conflicts then
follow the steps in the [merge conflict walkthrough](#walkthrough).

B) Contributors without write access (students or mentors)

1. Communicate with others and let them know what you are working on.

2. Fork the repository to your personal github.

3. Use git clone and copy paste the SSH URL. You will clone the master branch by default.
  For example, <code>git clone git@github.com:TatianaTylosky/amaze-curric.git</code>

4. Create a new branch and name it appropriately.
   For example, <code>git checkout -B tati-edits</code>

5. Locally make edits to this new branch.
   **NOTE: If you need to make changes to file names you need to make sure all other pull request have been merge.**

6. Do <code>git status</code> in order to see the file you have
   changed. Then use <code>git add
   name-of-edited-file</code> to the files you modified. Then do <code>git commit -m "Informative commit message"</code>.

7. Push your new branch with the changes to your personal github. For
   ex <code>git push origin tati-edits</code>

8. Go to your github to your personal forked repository and click the green
   compare and pull request button.

9. By default you are probably comparing the correct branches. Just in case take a look. REMEMBER: You want Do not compare with Compare <code>base fork: Thinkful-Ed/curric..base: preview</code> to <code>head fork: Tatianatylosky..base: master</code>

10. Check to see if your branch can be automatically merge. If it can
   then let a course lead review it! If you have a merge conflicts then
follow the steps in the [merge conflict walkthrough](#walkthrough).

<a name="overview"></a>
###Best Practices Overview

* Pull/fork before you start working.

* Name your branches properly.

* Always push to develop/preview not master.

* Merge early and often.

* Don't panic.


<a name="solving"></a>
##Solving Merge Conflicts

<a name="walkthrough"></a>
###Walkthrough

After you see...

![](http://i.imgur.com/vCkvoEo.png)

here is the general procedure you can follow in order to deal with merge
conflicts.

1. Make Git insert those HEAD tags

  In order to know where exactly you are having merge conflicts you need to follow the set of instructions that Github provides under the "Use the command line" link (see image above).

2. Manually find and correct the errors

  Open up your text editor and do a global search for either "HEAD" or ">>>>>>>>>". On sublime this can be done with command-shift-F. This should show you the tags that github put in so that you know where the merge conflicts are occuring.

3. Add and commit your updated branch

  <code>git commit -m “Fix merge conflicts”</code>

4. Push your updated branch

  <code>git push origin branch-name</code>

<a name="tricks"></a>
###Tricks

####Git Stash and Pop

If you are on a branch with uncommited changes and want to temporarily
switch branches without committing you can with <code>git stash</code>.
Using <code>git stash</code> will hide those changes from git allowing
you to either switch branches or commit a different set of changes. Once
you are ready to revisit those changes in order to commit them use
<code>git stash pop</code> and they will reappear!

####Git diff

Ask Kara

####Reset's?

Ask Kara

<a name="contribute"></a>
###Contribute!
Do you have more suggestions for this TF Guide? Make a Pull Request with
your new found knowledge and let us update it!
