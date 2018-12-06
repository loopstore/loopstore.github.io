# TESTING ONLY!

## You need to have a Google account to run this tutorial in Google Cloudshell

We recommend setting up a new gmail account for this tutorial at [https://accounts.google.com/signup](https://accounts.google.com/signup) and sign in to Cloudshell using that. 

This will clone the repository into the directory ~/loopstore and run the tutorial in Google Cloud Shell.

## If you are already running the tutorial in Cloud Shell, do not use the button below

Enter "teachme ~/loopstore/tutorial-docs/cloudshell/index.md" at the command line

    teachme ~/loopstore/tutorial-docs/cloudshell/index.md

[![Open in Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.png)](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/loopstore/loopstore&tutorial=tutorial-docs/cloudshell/index.md)

## Tutorial Code

*The idea is you build the LoopStore yourself!*

You are staring with an 'empty' git Master branch. Although not strictly necessary, we would *recommend switching to My-Working-Branch * by enetering:

    git checkout My-Working-Branch

The code generated following each tutorial step is stored on seperate Git branches (see "*Tutorial-Step Branches*" below).

The branches can be merged in order to create the version stored on the *Tutorial-Steps_FINAL-End* branch.

To switch to the Tutorial-Steps_FINAL-End branch 

Depending on what you what to explore, you may need to configure the tutorial code first.

To preserve the original Tutorial-Steps_FINAL-End branch, merge it to *My-Working-Branch*.



## Repo Structure - Using Git Branches 
The LoopStore repo has several git branches

### Master
This is where you will store the Master version of the code as you build the LoopStore. 

When you start the tutorial there is no code stored on this branch, just this README and other information in the project root directory ~/loopstore, and the tutorial documents, which stored under the  ~/loopstore/tutorial-docs/ directory.

### My-Working-Branch
By default when you check out the code you will be working on the Master branch.

*WE RECOMMEND SWITCHING TO My-Working-Branch*:
Whilst you're working on steps on the tutorial, it's a good idea to work on a copy or branch of you're code.

When you're happy it's all working, you can *merge* your changes to the Master branch. There are insructions on how to do this below.

To switch to My-Working-Branch enter
    git checkout My-Working-Branch

### Tutorial-Step Branches
There a serveral branches which store the versions of the code at the beginning and end of each step which requires code changes.

The format for these Tutorial-Step branch names is *Tutorial-Code-Step_[N][FINAL]-[Start][End]*, speicifying:
- Step number(N) or "FINAL" and
- "Start" or "End"

For convenience each tutorial step has a branch storing the code state at the beginning and the end of the step. The code at the start of a step should, of course, exactly match the end of the previous step and is effectively a clone of the Tutorial-Code-Step_N_[previous-step-number]-End

In other works, we starting from an 'empty' Master branch, Tutorial-Step branches are named from Tutorial-Step_1-End to Tutorial-Step_FINAL-End.

THIS ISN'T TREU ANY MORE - REWORKING.....*The branches have been created "backwards" from an 'empty' Master branch*, i.e.: 
- Tutorial-Step_FINAL-End is based on Master (containing just the tutorial and information docs)
- Tutorial-Step_FINAL-Start is based on Tutorial-Step_FINAL-End
- Tutorial-Step_[penultimate-step-number]-End is based on Tutorial-Step_FINAL-Start
- Tutorial-Step_[penultimate-step-number]-Start is based on Step_[penultimate-step-number]-End...
..and so on, until we reach Tutorial-Step_1-End
*Why?*
A tutorial branch will always be out of sync with the one it is based on.

This setup means that you can look back at changes made in each tutorial code step using the *git compare* command.

So, for example, you can see the changes made in the first step of the tutorial (which generates code) if you enter:
    git compare Master...Tutorial-Step_N_1-End
(provided Master is still empty)

To see what happens in the first step, enter:
    git diff Tutorial-Step_1-Start..Tutorial-Step_1-End


 

