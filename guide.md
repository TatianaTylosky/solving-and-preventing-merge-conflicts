##Solving & Preventing Merge Conflicts
<img src="https://octodex.github.com/images/Professortocat_v2.png" width="200" />

The purpose of this overview is to teach those who are less familiar with
Github how to make pull requests and solve merge conflicts for the
TF curriculum or code base.

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
Thinkful's curriculum is set up so that multiple contributors can work on
separate branches that are then merged together by a course lead.

<a name="curriculumbranches"></a>
###Curriculum Branches
![](http://i.imgur.com/bf4hpLn.png)

<a name="engbranches"></a>
###Eng Branches
![](http://i.imgur.com/mJu0BdQ.png)

<a name="mergeconflicts"></a>
##Merge Conflicts

<a name="whatarethey"></a>
###What is a Merge Conflict?
In a perfect world, everyone is working on different lines of code in
the preview (curric team) or develop (eng team) branch but sometimes...

![](http://i.imgur.com/vCkvoEo.png)

<a name="whymergeconflicts"></a>
###Why do Merge Conflicts Occur?

1. Someone updated the preview branch by merging new code while you were
   working on your branch

2. AND you modified the **same** line of code that they did.

Github is NOT smart enough to know which version you want.

<a name="prevention"></a>
##Prevention by using Best Practices

<a name="pullrequests"></a>
### How to make good pull requests

1. Communicate with others and let them know what you are working on.

2. Fork repository to your personal github

3. Use git clone and copy paste the SSH URL. Notice you are cloning whatever branch you are currently on in github. Default is master which is good. For example, <code>git clone git@github.com:TatianaTylosky/amaze-curric.git</code>

4. Create new branch and name somewhat appropriately. For example, <code>git checkout -B
   tati-edits</code>

5. Make edits/update to this new branch you have created locally. **NOTE: If you need to make changes to file name you need to make sure all other pull request have been merge.**

6. Do <code>git status</code> in order to see the file you have
   changed. Then use <code>git add
   name-of-edited-file</code> to the files you modified. Then do <code>git commit -m "Fix Typo"</code>.

7. Push your new branch with the changes to your personal github. For
   ex <code>git push origin tati-edits</code>

8. Go to your github to your forked repository and click the green
   compare and pull request button.

9. Compare <code>base fork: Thinkful-Ed/curric..base: preview</code> to <code>head fork: Tatianatylosky..base: master</code>

10. Have your pull request reviewed

<a name="overview"></a>
###Overview

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

