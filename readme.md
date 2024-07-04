# ekvip Coding Ninjas Standard - Collections Concrete Implementation Library for TwinCAT Build 4026

<a name="toc"></a>
## Table-Of-Contents

1. [Table Of Contents](#toc)
2. [Summary](#summary)
3. [Folder Structure](#structure)
4. [Branches](#branches)
5. [Version Number Format](#versioform)
6. [Contribution](#contribution)
7. [Version Log](#version)

<a name="summary"></a>
## Summary

* project description: This is a TwinCAT 3 library project for concrete collection implementations. This project is ported to 4026 from [CNM Collections Lib](https://ekv-app-git-p01.ekvip.de/CNMTC3/cnm-collections-lib)
* For required software and tools, visit the confluence page:
* [confluence page](https://ekvip.atlassian.net/wiki/spaces/CNMS/pages/1663598599/CNM+Collections)
* [bitbucket project page](https://bitbucket.osb-ag.de/projects/CNMTC3/repos/cnm-collections-lib/browse)

<a name="structure"></a>
## Folder-Structure

*   **.\\**
*   **build\\** _contains the actual library files_
*   **src\\** _root folder for all project sources_
*   **test\\** _contains project sources for all test libraries_
*   **.gitignore**  _the git ignore file for this project_
*   **.gitattributes** _the git attribute file for the LFS support_
*   **README.md** _the file you read right now_

<a name="branches"></a>
## Branches

The repository has some branches to allow collaboration on a centralized repository, and give everybody the possibility to orient onself. We've two main branches, we use this two to branch from and merge to.

> **The Main Branches Are:**
> -   **master**  _here are  **only**  our well tested releases_
> -   **develop**  _this is the choice for new features during the normal project work_

### creating Branches

The initial master commit contains the reworked readme.md, .gitignore and .gitattributes files.
We **only** use the Jira project-tasks (only sub tasks) to create branches. You can choose between **feature** and **hotfix** branches in the Jira menu. To create a branch in Jira, choose the task you want to create a branch for and click on **"Create branch"** at the tab **"Development"** in the task view.

Here are two examples:  **feature/FRINST-14-analogvalueprocessing/efro**  (here is Elias Froschauer working on feature analogvalueprocessing in project FRINST) and  **_hotfix/FRINST-15-analogvalueprocessingbug/toel_**  (here is Tino working on a hotfix for the bug in analog value processing after production release). 

### creating Tags
Every time you finish a task and merge a branch back to the develop or master, then you have to fill out the version log here and you've to tag this commit with the prefix ***"version_"*** and the version number.
If you work in a group and the current online version is not the latest master or develop commit, you will need to tag the currently used branch with **"online"**.

<a name="versionform"></a>
## Version-Number-Format

The version number format for this project has following pattern: ***{major release}.{minor release}.{development state}{maintenance}***. Before the software is deployed to the machine, the major number is zero, if the software is deployed and tested 1st time the major number increase to one.

## Version-Number-Format

The version number format for this project has following pattern: ***{major release}.{minor release}.{development state}{maintenance}***. Before the software is deployed to the machine, the major number is zero, if the software is deployed and tested 1st time the major number increase to one.

> **Version Number Format Description:**

> -   **major release**  _marks api changes_
> -   **minor release**  _marks functional extensions or changes but api is still compatible_
> -   **build**  _**odd** number is beta state,  **even**  is stable release
> -   **revision**  _shows the number of patches and hotfixes_

Some examples:

-   **0.0.0.0**  _initial commit_
-   **0.3.0.7**  _add some features and some bug fixes, software is still in alpha state_
-   **0.3.2.9**  _two more bug fixes and the software is now in release state_
-   **1.0.4.15**  _the api has been changed, this needs changes in the used software as well_

<a name="contribution"></a>
## Contribution

-   The language of software and software comments is **English** and software documentation is **English**
-   Use **branch** and **tag** **rules** as defined earlier
-   If you extend or change the folder structure, then you have to **update this file**
-   You have to provide a **version description** with a small change log for every version tag within this file in the version log section
-   If you want to merge you software to the master branch, then you have to take care that your software is compiling  **without warnings and errors**.
-   If you edit this file you've to do it in **English** and to use the **markdown** format
-	It is **not** allowed to work in one of the main branches directly
-	It is **only** allowed to work in your own branches (with your ekvip name acronym)
-	Every commit to feature or hotfix branch needs to contain the **Jira task id** before the commit description

<a name="version"></a>
## Version-Log

### Versions 

1.	[0.0.0.0](#0.0.0.0)
2.	[1.0.0.0](#1.0.0.0)
3.	[1.1.0.0](#1.1.0.0)
4.	[1.3.3.0](#1.3.3.0)
5.	[1.4.1.0](#1.4.1.0)
6.	[1.5.3.3](#1.5.3.3)
7.	[1.5.9.14](#1.5.9.14)
8.	[1.6.0.1](#1.6.0.1)
9.	[1.6.0.2](#1.6.0.2)
10.	[1.6.2.1](#1.6.2.1)
11.	[1.7.0.0](#1.7.0.0)
12.	[1.8.0.0](#1.8.0.0)
13. [3.0.0.0](#3.0.0.0)
14. [4.0.0.0](#4.0.0.0)
15.	[5.0.0.0](#5.0.0.0)
16. [6.0.0.0](#6.0.0.0)
17. [7.0.0.0](#7.0.0.0)
18. [8.0.0.0](#8.0.0.0)
19. [9.0.0.0](#9.0.0.0)
20. [10.0.0.0](#10.0.0.0)
21. [11.0.0.0] (#11.0.0.0)

### 0.0.0.0 
_initial commit_

### 1.0.0.0 
-   Implementation for LinkedList
-   Includes Test Project with Test for LinkedList

### 1.1.0.0 
-   Add AbstractCollection to Lists

### 1.2.0.2
- fixed issue with containersize passed to external sorter_

### 1.3.3.0
- added basic Shell-, Merge-, and Timsort for ArrayLists

### 1.4.1.0
- changed ArrayLis so that it can use the Shell-, Merge- and Timsorter
- implemented Shellsort as default Sorter for ArrayList

### 1.5.3.3
- added CompareBounds to Mergesort

### 1.5.9.14
- Merge-, Shell-, Timsort for ArrayList all support CompareBounds

### 1.6.0.1
- Merge-, Shell-, Timsort for ArrayList can be notified about a change of the list and will go to error in that case

### 1.6.0.2
- Arraylists now notify the setted sorter about changes on all listchanging methods

### 1.6.2.1
- implemented fallback for Arraylistsorters if extern sorter is removed

### 1.7.0.0
- take care that mergesort sortbuffer is destructed if MergesortFB is destructed

### 1.8.0.0
- implemented clone method for Merge-, Tim-, and Shellsort on ArrayLists

### 3.0.0.0
- updated AbstractObjectLib to Version 2.0.4.7

### 4.0.0.0
- changed pop / dequeue to methods
- added SingleExectuionResult to the ArrayList IIndexable Methods
- added Namespaces to classnames

### 5.0.0.0
- removed Factorys from Input to LinkedLists and Trees
- added the Librarys as VAR_STAT to LL and Trees

### 6.0.0.0
- upgraded to CollectionInterfaces 6.0.0.0
- removed returnvalue from invert method

### 7.0.0.0
- added cyclemanagment to set methods

### 8.0.0.0
- integrated CNM_Collection_Interfaces 7.0.0.0 (New IObjectWrapper Interface)
- fixed a possible memoryleak in BalancedBinarySearchTreenode.destruct()
- Added a shared CollectionFactory that is used from all instances
- fixed Errors in Documentation (syntax)

### 9.0.0.0
- integrated CNM_Collections_Interfaces 8.0.0.0 (removed .root from ITree)
- made .root protected for BalancedBinarySearchTree

### 10.0.0.0
- adopted to Collection_Interface 10.0.0.0 (change of sorter interfaces )
- adopted LinkedList to use ILinkedElement where possible

### 11.0.0.0
- made changes To Naming and added missing Documentation
- implementet CNM_Collection_Interface 11.0.0.0 (changed spelling of ISet.subtract())

### 11.1.0.0
- add the AbstractMergeBasedSorter for the Arraylists that was formally located in the CNM_CollectionInterfaces

### 11.2.0.0
- arraylists and linkedlists now support clone and deepclone

### 12.0.0.0
- implemented new Interfacestructure of ILinkedList that wasprovided by CNM_CollectionInterfaces 14.0.0.0

### 13.0.0.0
- Collections can no longer contain themself
- LinkedListMergeSorter was refactored
