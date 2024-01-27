
In every walk with nature,
One receives far more than he seeks.
The winds whisper secrets of the ages,
And the earth hums life's melodies.
Listen closely, and you shall hear.
#Changing Multiple Commit Messages
To modify a commit that is farther back in your history, you must move to more complex tools. Git doesn’t have a modify-history tool, but you can use the rebase tool to rebase a series of commits onto the HEAD that they were originally based on instead of moving them to another one. With the interactive rebase tool, you can then stop after each commit you want to modify and change the message, add files, or do whatever you wish. You can run rebase interactively by adding the -i option to git rebase. You must indicate how far back you want to rewrite commits by telling the command which commit to rebase onto.

For example, if you want to change the last three commit messages, or any of the commit messages in that group, you supply as an argument to git rebase -i the parent of the last commit you want to edit, which is HEAD~2^ or HEAD~3. It may be easier to remember the ~3 because you’re trying to edit the last three commits, but keep in mind that you’re actually designating four commits ago, the parent of the last commit you want to edit:
#SOPHIA LI

Git interactive rebase
The entire Pro Git book, written by Scott Chacon and Ben Straub and 
published by Apress, is available here. All content is licensed under the 
Creative Commons Attribution Non Commercial Share Alike 3.0 license. versions of the book are available on Amazon.com.
The version found here has been updated with corrections and additions 
from hundreds of contributors. If you see an error or have a suggestion, 
patches and issues are welcome in its GitHub repository.

Changing Multiple Commit Messages
To modify a commit that is farther back in your history, you must move to 
more complex tools. Git doesn’t have a modify-history tool, but you can 
use the rebase tool to rebase a series of commits onto the HEAD that they 
were originally based on instead of moving them to another one. With the 
interactive rebase tool, you can then stop after each commit you want to 
modify and change the message, add files, or do whatever you wish. You can 
run rebase interactively by adding the -i option to git rebase. You must 
indicate how far back you want to rewrite commits by telling the command 
which commit to rebase onto.
Xinyu, Sophia, florent
For example, if you want to change the last three commit messages, or any 
of the commit messages in that group, you supply as an argument to git 
rebase -i the parent of the last commit you want to edit, which is HEAD~2^ 
or HEAD~3. It may be easier to remember the ~3 because you’re trying to 
edit the last three commits, but keep in mind that you’re actually 
designating four commits ago, the parent of the last commit you want to 
edit:
