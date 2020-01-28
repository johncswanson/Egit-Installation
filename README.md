# Egit-Installation for IBM Explorer for z/OS <!-- omit in toc -->

This code pattern goes through the process of installing the Egit plug-in to IBM Explorer for z/OS Aqua. It also shows how to work with the plug-in to create a new git repository, adding an existing git repository, cloning a git repository from a remote host, and how to commit and push to a git repository.

This work is being done as part of a series of code patterns around bringing DevOps practices to z/OS Connect projects.

### Prerequisites:

- IBM Explorer for z/OS Aqua must be installed. If it is not installed please reference this guide on installing it: [Installing IBM Explorer for z/OS Aqua](https://www.ibm.com/support/knowledgecenter/en/SSBDYH_3.2/com.ibm.zexpl.install.client.doc/topics/install20.html)
- Basic knowledge of the git source code manager tool.

### Sections: <!-- omit in toc -->

- [1. Installing the eGit Plug-in](#1-installing-the-egit-plug-in)
-Follow this section to obtain the eGit Plug-in and add it to the IBM Explorer for z/OS (Aqua) environment.
- [2. Creating a Git Repo with eGit](#2-creating-a-git-repo-with-egit)
-The eGit tool connects projects to a local (workstation) repository.  The repository can be created manually outside the tool or using the tool's interface.  This section shows how to do so within the tool BEFORE starting your project.
- [3. Creating a Repo from an Existing Project](#3-creating-a-repo-from-an-existing-project)
-Follow this section if you have an existing project that you would like to add to a Git Repo.
- [4. Clone a Git Repository](#4-clone-a-git-repository)
-Follow this section if you would like to replicate an existing Git repository to the eGit workspace.  You will then be able to work with the project artifacts.
- [5. Working with Egit](#5-working-with-egit)
-This section reviews how to make changes to a local project, commit those changes to the local repository and push them to a remote repository.

## 1. Installing the eGit Plug-in

**1.1** Open IBM Explorer for z/OS. ![Open IBM Explorer for z/OS](docs/source/images/Windows-Egit-Installation-Screenshots/1.1-OpenZOSExplorer.png)

**1.2** Click on **Help** -> **Install New Software...** ![Install New Software](docs/source/images/Windows-Egit-Installation-Screenshots/1.2-InstallNewSoftware.png)

**1.3** Click the **Add** Button. ![Add Buttton](docs/source/images/Windows-Egit-Installation-Screenshots/1.3-AddButton.png)

**1.4** Type "eGit" for **Name** and "http://download.eclipse.org/egit/updates" for **Location**. Then click **OK**. ![eGit Location](docs/source/images/Windows-Egit-Installation-Screenshots/1.4-EgitLink.png)

**1.5** Click the check box next to **Git integration for Eclipse**. Also, click the check box next to **Show only software applicable to target environment**. Then click **Next**. ![Check Boxs](docs/source/images/Windows-Egit-Installation-Screenshots/1.5-CheckBoxs.png)

**1.6** Click the **Next** Button. ![Install Remediation Page](docs/source/images/Windows-Egit-Installation-Screenshots/1.6-InstallRemediationPage.png)

**1.7** Click the **Next** Button. ![Install Details](docs/source/images/Windows-Egit-Installation-Screenshots/1.7-InstallDetails.png)

**1.8** Click the radio button to accept the terms of the license agreements, then click **Finish**. ![Accept Licenses](docs/source/images/Windows-Egit-Installation-Screenshots/1.8-AcceptLicenses.png)

**1.9** A window will pop up during the install. Make sure the check box next to **Eclicpse Foundation\, Inc; Java Software...** is checked. Then click **OK**.<br/> ![Trust Certificates](docs/source/images/Windows-Egit-Installation-Screenshots/1.9-TrustCertificates.png)

**1.10** Once the plug-in is finished installing IBM Explorer for z/OS will need to be restarted before it can be used. A pop-up window should appear asking you to restart. Click **Yes**.![Restart Explorer](docs/source/images/Windows-Egit-Installation-Screenshots/1.10-Restart.png)

## 2. Creating a Git Repo with eGit

**2.1** Reopen IBM Explorer for z/OS if it did not repoen automatically.

**2.2** Click on **Window** -> **Perspective** -> **Open Perspective** -> **Other...**. ![Open Perspective List](docs/source/images/Windows-Egit-Installation-Screenshots/2.2-OpenPerspectiveList.png)

**2.3** Select **Git** and click **OK**. <br/> ![Selectn Git](docs/source/images/Windows-Egit-Installation-Screenshots/2.3-SelectGit.png)

**2.4** Select **Create new local Git repository** ![Select Create New Repo](docs/source/images/Windows-Egit-Installation-Screenshots/2.4-CreateNewRepo.png)

**2.5** Select the Directory you wish to create a git repository for. Then click **Create**. ![Select Dir](docs/source/images/Windows-Egit-Installation-Screenshots/2.5-SelectDir.png)

**2.6** See that the repository now shows up in the **Git Repositories** view. ![Git Repo View ](docs/source/images/Windows-Egit-Installation-Screenshots/2.6-SeeRepo.png)

## 3. Creating a Repo from an Existing Project

**3.1** Open a Project in the **Project Explorer**. ![Open Project](docs/source/images/Windows-Egit-Installation-Screenshots/3.1-OpenProject.png)

**3.2** Right click on the Project. Then click **Team** -> **Share Project...** ![Share Project](docs/source/images/Windows-Egit-Installation-Screenshots/3.2-ShareProject.png)

**3.3** Select **Git**, then click **Next**. ![Select Git](docs/source/images/Windows-Egit-Installation-Screenshots/3.3-SelectGit.png)

**3.4** Click the **Create** Button. If your project has already been initialized as a git reposiotry then this window won't show. You will be imidiately taken to the next step. ![Click Create](docs/source/images/Windows-Egit-Installation-Screenshots/3.4-ClickCreate.png)

**3.5** Choose the directory for your repository, then click **Finish**. ![Directory Location & Finish](docs/source/images/Windows-Egit-Installation-Screenshots/3.5-DirLocation&Finish.png)

**3.6** Click **Finish**. ![Click Finish](docs/source/images/Windows-Egit-Installation-Screenshots/3.6-Finish.png)

**3.7** The repository is now created. If you follow the sets in sections 2.2 & 2.3 to open the Git Perspective, you can see the newly created repo. ![New Repo](docs/source/images/Windows-Egit-Installation-Screenshots/3.7-GitPerspective.png)

## 4. Clone a Git Repository

**4.1** Click the **Clone a Git repository** link or the Clone icon at the top. ![CloneRepo](docs/source/images/Windows-Egit-Installation-Screenshots/4.1-CloneGitRepo.png)

**4.2** Enter the information of the repository you wish to clone. As you enter the **URI** the **Host** and **Repository Path** should fill themselves out. If not port is specified the default port will be used and if no User ID and Password are provided it will assume there is no authetication needed. Then click **Next >**. ![EnterRepoInfo](docs/source/images/Windows-Egit-Installation-Screenshots/4.2-EnterRepoInfo.png)

**4.3** Select the Branches you wish to clone then click **Next >**. ![Branch Selection](docs/source/images/Windows-Egit-Installation-Screenshots/4.3-BranchSelection.png)

**4.4** Enter the location on you machine to which you would like to save the cloned repository. Then click **Finish**. ![Branch Selection](docs/source/images/Windows-Egit-Installation-Screenshots/4.4-LocalDestination.png)

**4.5** Now your cloned repository should show up in the Git Perspective of z/OS Explorer. ![See Cloned Repo](docs/source/images/Windows-Egit-Installation-Screenshots/4.5-SeeClonedRepo.png)

## 5. Working with Egit

**5.1** Once your project has either been created, imported or cloned, you should now see it in the Git Perspective of z/os Explorer. ![Git Project](docs/source/images/Windows-Egit-Installation-Screenshots/5.1-GitProject.png)

**5.2** Expand the Git Project by clicking the **>** to the left of the project. Then expand the **Working Tree** section. In this section you should see a **.git** folder, a **.project** file and the project folder itself. Expand the project folder to see all the files and folders in your project. Double click on any file to open it. ![Open Fil](docs/source/images/Windows-Egit-Installation-Screenshots/5.2-OpenFile.png)

**5.3** Make a change to the file you opened, then save the file. ![Make a Change](docs/source/images/Windows-Egit-Installation-Screenshots/5.3-MakeAChange.png)

**5.4** Once you save the file, it should appear in the **Unstaged Changes** section below. ![Unstaged Changes](docs/source/images/Windows-Egit-Installation-Screenshots/5.4-UnstagedChanges.png)

**5.5** Click the plus symbol to stage only the selected files or click the double plus symbol to stage all unstaged changes. ![Stage Changes](docs/source/images/Windows-Egit-Installation-Screenshots/5.5-StageChanges.png)

**5.6** The file changes should now have moved to the **Staged Changes Section**. ![Stage Changes Section](docs/source/images/Windows-Egit-Installation-Screenshots/5.6-StagedChangesSection.png)

**5.7** In the **Commit Message** section, type a message that describes the changes you made. Then click the **Commit** button if you would like to commit your changes to the local git repository on you machine, or the **Commit and Push...** button if you would like to commit the change to the local git repository and push the commit to a remote repository. ![Commit Changes](docs/source/images/Windows-Egit-Installation-Screenshots/5.7-CommitChanges.png)

**5.8** If you are pushing to a remote repository you may be asked to provide authentication. ![Provide Authentication](docs/source/images/Windows-Egit-Installation-Screenshots/5.8-ProvideAuthentication.png)

**5.9** You will then be shown the results of your commit and push. Click **Close** once you are done viewing the results. ![Commit and Push Results](docs/source/images/Windows-Egit-Installation-Screenshots/5.9-CommitAndPushResults.png)

**5.10** If a remote is not already added to your git project you can add one by expanding the Git project in the Git Perspective. Then right clicking the **Remote** section. The click **Create Remote...** ![Adding a Remote](docs/source/images/Windows-Egit-Installation-Screenshots/5.10-AddingRemote.png)

**5.11** Enter a name for the remote repository then click **Create**. ![Name the Remote](docs/source/images/Windows-Egit-Installation-Screenshots/5.11-NameTheRemote.png)

**5.12** Click on **Change...** ![Click Change](docs/source/images/Windows-Egit-Installation-Screenshots/5.12-ClickChange.png)

**5.13** Enter the **URI** of your remote repository. As you enter the **URI** the **Host** and **Repository path** fields should fill themselves out. If you remote repository requires authentication also enter a **Username** and **Password**. The click **Finish**. ![Enter Remote Info](docs/source/images/Windows-Egit-Installation-Screenshots/5.13-EnterRemoteInfo.png)

**5.14** Now click **Save** to save the remote repository to your git project. You can also click **Save and Push** to save the remote then push the project to the remote repository. ![Save and Push](docs/source/images/Windows-Egit-Installation-Screenshots/5.14-SaveAndPush.png)

**5.15** If you did not provide a username and password before and one is required, you may be asked again to provide one. ![Authentication](docs/source/images/Windows-Egit-Installation-Screenshots/5.15-Authenticate.png)

**5.16** If you decided to push to the new remote, you will now see a results of the push. You can click **Close** when you are finished looking through the push results. ![Push Info](docs/source/images/Windows-Egit-Installation-Screenshots/5.16-PushInfo.png)
