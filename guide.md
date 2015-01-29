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
- Ask Zoe

![](http://i.imgur.com/bf4hpLn.png)

<a name="engbranches"></a>
###Eng Branches
Thinkful's code base ??? some comment here?

Example:
feature/python-guide branch --> develop branch --> master branch

Naming convention:
- Ask Kara

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

10. Have your pull request reviewed

<a name="overview"></a>
###Best Practices Overview

* Pull/fork before you start working.

* Name your branches properly.

* Always push to develop/preview not master.

* Merge early and often.

* Don't panic.


<a name="solving"></a>
##Solving Merge Conflicts

NOTES
How to fix
git pull upsteam master
add upstream
git remote add upstream ORIGINAL-MASTER
git fetch upstream (just fetch not merge)
git branch -a (to see all branches
git merge upstream/master
open text editor
how to find merge conflicts
git status
open file
search for “HEAD”
after fixed merge conflicts do git add
after they all fixed git commit -m “Fix merge conflicts”
git push origin update-branch-name

