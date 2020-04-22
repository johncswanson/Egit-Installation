# EGit Installation for IBM Explorer for z/OS <!-- omit in toc -->

This code pattern walks through the process of installing the EGit plug-in to IBM Explorer for z/OS (z/OS Explorer). It then shows how to work with the plug-in to perform some standard tasks related to source code management with Git such as creating a new Git repository, adding an existing Git repository, cloning a Git repository from a remote host, and committing and pushing to a Git repository.

This work is being done as part of a series of code patterns centered on bringing DevOps practices to z/OS Connect projects.

### Prerequisites:

- IBM Explorer for z/OS must be installed. If it is not installed please reference this guide on doing so: [Installing IBM Explorer for z/OS Aqua](https://www.ibm.com/support/knowledgecenter/en/SSBDYH_3.2/com.ibm.zexpl.install.client.doc/topics/install20.html)
- Basic knowledge of the git source code manager tool.

### Sections: <!-- omit in toc -->

- [1. Installing the EGit Plug-in](#1-installing-the-egit-plug-in)
- [2. Creating a Git Repo with EGit](#2-creating-a-git-repo-with-egit)
- [3. Creating a Repo from an Existing Project](#3-creating-a-repo-from-an-existing-project)
- [4. Clone a Git Repository](#4-clone-a-git-repository)
- [5. Working with EGit](#5-working-with-egit)

## 1. Installing the EGit Plug-in

**1.1** Open IBM Explorer for z/OS. ![Open IBM Explorer for z/OS](docs/source/images/Windows-Egit-Installation-Screenshots/1.1-OpenZOSExplorer.png)

**1.2** Click on **Help** -> **Install New Software...** ![Install New Software](docs/source/images/Windows-Egit-Installation-Screenshots/1.2-InstallNewSoftware.png)

**1.3** Click the **Add** Button. ![Add Button](docs/source/images/Windows-Egit-Installation-Screenshots/1.3-AddButton.png)

**1.4** Type **"eGit"** for **Name** and "http://download.eclipse.org/egit/updates" for **Location**. Then click **OK**. ![eGit Location](docs/source/images/Windows-Egit-Installation-Screenshots/1.4-EgitLink.png)

**1.5** Click the check box next to **Git integration for Eclipse**. Also, click the check box next to **Show only software applicable to target environment**. Then click **Next**. ![Check Boxes](docs/source/images/Windows-Egit-Installation-Screenshots/1.5-CheckBoxs.png)

**1.6** Click the **Next** Button. ![Install Remediation Page](docs/source/images/Windows-Egit-Installation-Screenshots/1.6-InstallRemediationPage.png)

**1.7** Click the **Next** Button. ![Install Details](docs/source/images/Windows-Egit-Installation-Screenshots/1.7-InstallDetails.png)

**1.8** Click the radio button to accept the terms of the license agreements, then click **Finish**. ![Accept Licenses](docs/source/images/Windows-Egit-Installation-Screenshots/1.8-AcceptLicenses.png)

**1.9** A window will pop up during the install. Make sure the check box next to **Eclipse Foundation\, Inc; Java Software...** is checked. Then click **OK**.<br/> ![Trust Certificates](docs/source/images/Windows-Egit-Installation-Screenshots/1.9-TrustCertificates.png)

**1.10** Once the plug-in is finished installing, IBM Explorer for z/OS will need to be restarted before it can be used. A pop-up window should appear asking you to restart. Click **Yes**.![Restart Explorer](docs/source/images/Windows-Egit-Installation-Screenshots/1.10-Restart.png)

## 2. Creating a Git Repo with EGit

**2.1** Re-open IBM Explorer for z/OS if it did not re-open automatically.

**2.2** Click on **Window** -> **Perspective** -> **Open Perspective** -> **Other...**. ![Open Perspective List](docs/source/images/Windows-Egit-Installation-Screenshots/2.2-OpenPerspectiveList.png)

**2.3** Select **Git** and click **OK**. <br/> ![Select Git](docs/source/images/Windows-Egit-Installation-Screenshots/2.3-SelectGit.png)

**2.4** Select **Create new local Git repository** ![Select Create New Repo](docs/source/images/Windows-Egit-Installation-Screenshots/2.4-CreateNewRepo.png)

**2.5** Select the Directory you wish the git repository to be saved in. _A sample path you can use is: **C:Users\<your-user-name>\git\repository**._ Then click **Create**. ![Select Dir](docs/source/images/Windows-Egit-Installation-Screenshots/2.5-SelectDir.png)

**2.6** See that the repository now shows up in the **Git Repositories** view. ![Git Repo View ](docs/source/images/Windows-Egit-Installation-Screenshots/2.6-SeeRepo.png)

## 3. Creating a Repo from an Existing Project

**3.0** **Set Up:** Creating a Project Example.

- **3.0.1** Click **Window -> Perspecitve -> Open Perspective -> Other...**. Then select the **z/OS Projects** perspective, then click **OK**. (_If you don't have the z/OS Projects perspective available, then jump to step 3.0.2_) Right click in the z/OS Projects view, then click **New -> z/OS Project...**. Enter a name for the project in the **Project name:** field (for example: "ProjectExample"). Then select **Do not create a subproject now**, then click **Finish**.
- **3.0.2** Click **Window -> Perspecitve -> Open Perspective -> Other...**. Then select the **Resource** perspective, then click **OK**. Right click in the Project Explorer view, then click **New -> Project...**. Next, in the wizard select the dropdown next to the **General** folder, then select **Project**, and click **Next** at the bottom. Then type a project name in the **Project name:** field (for example: "ProjectExample"). Then click **Finish**.

**3.1** Open a Project in the **Project Explorer**. ![Open Project](docs/source/images/Windows-Egit-Installation-Screenshots/3.1-OpenProject.png)

**3.2** Right click on the Project. Then click **Team** -> **Share Project...** ![Share Project](docs/source/images/Windows-Egit-Installation-Screenshots/3.2-ShareProject.png)

**3.3** Select **Git**, then click **Next**. ![Select Git](docs/source/images/Windows-Egit-Installation-Screenshots/3.3-SelectGit.png)

**3.4** Click the **Create** Button. If your project has already been initialized as a Git repository then this window won't show. You will be immediately taken to the next step. ![Click Create](docs/source/images/Windows-Egit-Installation-Screenshots/3.4-ClickCreate.png)

**3.5** Choose the directory for your repository, then click **Finish**. ![Directory Location & Finish](docs/source/images/Windows-Egit-Installation-Screenshots/3.5-DirLocation&Finish.png)

**3.6** Click **Finish**. ![Click Finish](docs/source/images/Windows-Egit-Installation-Screenshots/3.6-Finish.png)

**3.7** The repository is now created. If you follow the instructions in sections 2.2 & 2.3 to open the Git Perspective, you can see the newly created repo. ![New Repo](docs/source/images/Windows-Egit-Installation-Screenshots/3.7-GitPerspective.png)

## 4. Clone a Git Repository

**4.0 Set Up:** Create a GitHub account and Fork the repo.

- **4.0.1** Click this link: [GitHub SignUp](https://github.com/join?source=header), and create a GitHub account.
- **4.0.2** Now that you have your own GitHub account, click the **Fork** button at the top of this GitHub Repo. <br/> _This will create a copy of this repository under your GitHub account._ ![ForkRepo](docs\source\images\Windows-Egit-Installation-Screenshots\4.0.2-ForkRepo.png)
- **4.0.3** Now for the rest of this code pattern you will be using the GitHub repositoy under your account.

**4.1** Click the **Clone a Git repository** link or the Clone icon at the top. ![CloneRepo](docs/source/images/Windows-Egit-Installation-Screenshots/4.1-CloneGitRepo.png)

**4.2** Enter the information of the repository you wish to clone. To find the URI for your newly forked repo, click the **Clone or download** button on your GitHub Repo Page. ![CloneOrDownloadButton](docs/source/images/Windows-Egit-Installation-Screenshots/4.2.1-CloneOrDownloadButton.png) Then click the **Copy** button next to the URL to copy it to your clipboard. <br/> ![CopyURIButton](docs/source/images/Windows-Egit-Installation-Screenshots/4.2.2-CopyURIButton.png) <br/>
Paste the URI into the **URI** field. As you enter the **URI** the **Host** and **Repository Path** should fill themselves out. If no port is specified the default port will be used. In the **Authentication** section enter your GitHub username in the **User:** field and you GitHub password in the **Password:** field. Then click **Next >**. ![EnterRepoInfo](docs/source/images/Windows-Egit-Installation-Screenshots/4.2-EnterRepoInfo.png)

**4.3** Select the Branches you wish to clone then click **Next >**. ![Branch Selection](docs/source/images/Windows-Egit-Installation-Screenshots/4.3-BranchSelection.png)

**4.4** Enter the location on you machine to which you would like to save the cloned repository. Then click **Finish**. ![Branch Selection](docs/source/images/Windows-Egit-Installation-Screenshots/4.4-LocalDestination.png)

**4.5** Now your cloned repository should show up in the Git Perspective of z/OS Explorer. ![See Cloned Repo](docs/source/images/Windows-Egit-Installation-Screenshots/4.5-SeeClonedRepo.png)

## 5. Working with EGit

**5.1** Once your project has either been created, imported or cloned, you should now see it in the Git Perspective of z/OS Explorer. ![Git Project](docs/source/images/Windows-Egit-Installation-Screenshots/5.1-GitProject.png)

**5.2** Expand the Git Project by clicking the **>** to the left of the project. Then expand the **Working Tree** section. In this section you should see a **.git** folder, a **.project** file and the project folder itself. Expand the project folder to see all the files and folders in your project. Double click on any file to open it. ![Open Fil](docs/source/images/Windows-Egit-Installation-Screenshots/5.2-OpenFile.png)

**5.3** Make a change to the file you opened, then save the file. ![Make a Change](docs/source/images/Windows-Egit-Installation-Screenshots/5.3-MakeAChange.png)

**5.4** Once you save the file, it should appear in the **Unstaged Changes** section at the bottom of the window. ![Unstaged Changes](docs/source/images/Windows-Egit-Installation-Screenshots/5.4-UnstagedChanges.png)

**5.5** Click the plus symbol to stage only the selected files or click the double plus symbol to stage all unstaged changes. ![Stage Changes](docs/source/images/Windows-Egit-Installation-Screenshots/5.5-StageChanges.png)

**5.6** The file changes should now have moved to the **Staged Changes Section**. ![Stage Changes Section](docs/source/images/Windows-Egit-Installation-Screenshots/5.6-StagedChangesSection.png)

**5.7** In the **Commit Message** section, type a message that describes the changes you made. Then, click the **Commit** button if you would like to commit your changes to the local Git repository on you machine or the **Commit and Push...** button if you would like to commit the change to the local Git repository and push the commit to a remote repository. ![Commit Changes](docs/source/images/Windows-Egit-Installation-Screenshots/5.7-CommitChanges.png)

**5.8** If you are pushing to a remote repository, you may be asked to provide authentication. ![Provide Authentication](docs/source/images/Windows-Egit-Installation-Screenshots/5.8-ProvideAuthentication.png)

**5.9** You will then be shown the results of your commit and push. Click **Close** once you are done viewing the results. ![Commit and Push Results](docs/source/images/Windows-Egit-Installation-Screenshots/5.9-CommitAndPushResults.png)

**5.10** If a remote is not already added to your Git project, you can add one by expanding the Git Project in the Git Perspective. Then right clicking the **Remote** section. The click **Create Remote...** ![Adding a Remote](docs/source/images/Windows-Egit-Installation-Screenshots/5.10-AddingRemote.png)

**5.11** Enter a name for the remote repository then click **Create**. ![Name the Remote](docs/source/images/Windows-Egit-Installation-Screenshots/5.11-NameTheRemote.png)

**5.12** Click on **Change...** ![Click Change](docs/source/images/Windows-Egit-Installation-Screenshots/5.12-ClickChange.png)

**5.13** Enter the **URI** of your remote repository. As you enter the **URI** the **Host** and **Repository path** fields should fill themselves out. If the remote repository requires authentication also enter a **Username** and **Password**. The click **Finish**. ![Enter Remote Info](docs/source/images/Windows-Egit-Installation-Screenshots/5.13-EnterRemoteInfo.png)

**5.14** Now click **Save** to save the remote repository to your Git project. You can also click **Save and Push** to save the remote then push the project to the remote repository. ![Save and Push](docs/source/images/Windows-Egit-Installation-Screenshots/5.14-SaveAndPush.png)

**5.15** If you did not provide a username and password before and one is required, you may be asked again to provide one. ![Authentication](docs/source/images/Windows-Egit-Installation-Screenshots/5.15-Authenticate.png)

**5.16** If you decided to push to the new remote, you will now see a results of the push. Click **Close** when you are finished looking through the push results. ![Push Info](docs/source/images/Windows-Egit-Installation-Screenshots/5.16-PushInfo.png)
