#Solving & Preventing Merge Conflicts
![](https://octodex.github.com/images/Professortocat_v2.png)
##By: [Tatiana Tylosky](https://twitter.com/tatianatylosky)

###Table of Contents

* TF Branches Overview
  * Curric team
  * Eng team
* Merge Conflicts
  * What are they?
  * Why do they happen?
* Prevention by best practices
* Solving Merge Conflicts

###TF Branches

####Curriculum Branches
![](http://i.imgur.com/bf4hpLn.png)

####Eng Branches
![](http://i.imgur.com/mJu0BdQ.png)

###What is a Merge Conflict?
In a perfect world, everyone is working on different lines of code in
the preview (curric team) or develop (eng team) branch but sometimes...

![](http://i.imgur.com/vCkvoEo.png)

###Why do Merge Conflicts Occur?

1. Someone updated the preview branch by merging new code while you were
   working on your branch

2. AND you modified the **same** line of code that they did.

Github is NOT smart enough to know which version you want.

###Prevention by using Best Practices

1. Pull/fork before you start working.

2. Name your branches properly.

3. Always push to develop/preview not master.

4. Merge early and often.

5. Don't panic.

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
