# Costumer - Name of the project/Station

## Table-Of-Contents

- [Costumer - Name of the project/station](#Costumer---Name-of-the-project/station)
  - [Table-Of-Contents](#table-of-contents)
  - [Abstract](#abstract)
  - [Folder-Structure](#folder-structure)
  - [Branches](#branches)
    - [creating Branches](#creating-branches)
    - [creating Tags](#creating-tags)
  - [Version-Number-Format](#version-number-format)
  - [Contribution](#contribution)
  - [Version-Log](#version-log)

## Abstract

* Project description:
	Write a short description about the project.
* Related project spaces:
  * [Jira project](link to Jira project)
  * [Git project](link to Git repo)
  * [MS Teams group/folder](link to MS Teams group/folder)
* Required software and tools:
  * e.g. TwinCat3 version
  * e.g. HMI tool version
  * e.g. Control Plus Studio version (If it's a Nexeed project)


## Folder-Structure

*   **.\\**
*	**config\\** _config files of peripherals for the project_
*	**licenses\\** _license files for the project_
*	**tools\\** _tools for the project_
*   **src\\** _root folder for all project sources (for Nexeed projects use the predefined Nexeed folder structure inside src folder)_
*   **doc\\** _documentation / manuals_
*   **.gitignore**  _the git ignore file for this project_
*   **.gitattributes** _the git attribute file for the LFS support_
*   **README.md** _the file you read right now_

## Branches

The repository has some branches to allow collaboration on a centralized repository, and give everybody the possibility to orient onself. We've two main branches, we use this two to branch from and merge to.

> **The Main Branches Are:**
> -   **main**  _here are  **only**  our well tested releases_
> -   **develop**  _this is the choice for new features during the normal project work_

### Creating Branches

The initial master commit contains the reworked readme.md, .gitignore and .gitattributes files.
Since we don’t use Bitbucket and using GitLab instead, we can no longer create branches out of Jira. No matter what, we still stick to using the **Jira subtask id** as a prefix for the branch names of **feature** and **hotfix** branches.

Here are two examples:
**_feature/FRINST-14-analogvalueprocessing/efro_**  (here is Elias Froschauer working on feature analogvalueprocessing in project FRINST) and
**_hotfix/FRINST-15-analogvalueprocessingbug/toel_** (here is Tino working on a hotfix for the bug in analog value processing after production release). 

### Creating Tags
Every time you finish a task and merge a branch back to the main/master, then you have to fill out the version log here and you've to tag this commit with the prefix ***"version_"*** and the version number.
If you work in a group and the current online version is not the latest master or develop commit, you will need to tag the currently used branch with **"online"**.

## Version-Number-Format

The version number format for this project has following pattern: ***{major release}.{minor release}.{development state}{maintenance}***. Before the software is deployed to the machine, the major number is zero, if the software is deployed and tested 1st time the major number increase to one.

> **Version Number Format Description:**
> -   **major release**  _marks significant changes_
> -   **minor release**  _marks functional extensions or changes_
> -   **development state**  _**a**  is alpha state until start of commissioning (offline phase),  **b**  is beta state in commissioning until internal acceptance (FAT)  **r**  is release candidate from internal acceptance until operational handover (SAT),  **p**  is productive after operational handover_
> -   **maintenance**  _shows the number of patches and hotfixes_

Some examples:
-   **0.0.a0**  _initial commit_
-   **0.3.a7**  _add some features and some bug fixes, software is still in alpha state_
-   **0.3.b9**  _two more bug fixes and the software is now in commissioning beta state_
-   **1.0.r15**  _the software is internally accepted, machine is already running_
-   **1.0.p19**  _we handover the productive machine to customer_

## Contribution

-   The language of software and software comments is **English** and software documentation is **English**
-   Use **branch** and **tag** **rules** as defined earlier
-   If you extend or change the folder structure, then you have to **update this file**
-   You have to provide a **version description** with a small change log for every version tag within this file in the version log section
-   If you want to merge you software to the master branch, then you have to take care that your software is compiling  **without warnings and errors**.
-   If you edit this file you've to do it in **English** and to use the **markdown** format
-	It is **not** allowed to work in the main branches directly
-	It is **only** allowed to work in your own branches (with your ekvip name acronym) or on develop if it's a single source project
-	Every commit to feature or hotfix branch needs to contain the **Jira task id** before the commit description

## Version-Log

> - **version_0.0.a0** All files are suitable for our common Beckhoff projects. They already include specifications for Nexeed too.


