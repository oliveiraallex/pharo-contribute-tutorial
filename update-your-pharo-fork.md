# Update your Pharo fork with the official repository

**Scenario**: You have a fork of Github Pharo Project and you would like to update it with the official repository [github.com/pharo-project/pharo](github.com/pharo-project/pharo). 

You don't need to update your fork often. But sometimes, you would like to update your fork with the official Pharo repository and you can do this very easy using Iceberg or using the command line. This tutorial you will learn how to update a *Branch* in your repository. If you want to update all your repository, just repeat this procedure to all the branches.

1. Updating your fork using [Iceberg](#iceberg)
2. Updating your fork using [Command line](#command-line)

# Iceberg

### Update your Pharo fork using Iceberg in 3 steps

This procedure has 3 steps: 

1. [Create a new image and synchronize your remote repository](#step-1-create-a-new-image-and-synchronize-your-remote-repository)
2. [Synchronize your local repository with official Pharo repository](#step-2-synchronize-your-local-repository-with-official-pharo-repository)
3. [Push the updated data to your remote repository](#step-3-push-the-updated-data-to-your-remote-repository)

## Step 1 Create a new image and synchronize your remote repository

Create a new Pharo Image and open Iceberg. The status of Pharo repository should be **_Local repository missing_**. We need to repair it. Go to **_Repair repository_** and chose **_Clone again this repository_**. 
Enter the information of your fork (your Github username/pharo) and select HTTPS:

![image](https://user-images.githubusercontent.com/39618015/60343940-b9fce600-99b5-11e9-94e3-ea1f26f3c3b7.png)
![image](https://user-images.githubusercontent.com/39618015/60344050-faf4fa80-99b5-11e9-862c-75cb9633877c.png)
![image](https://user-images.githubusercontent.com/39618015/60344108-15c76f00-99b6-11e9-9b6e-3106c33609e3.png)

If this error happens, just ignore it, close all the windows and open Iceberg again:
![image](https://user-images.githubusercontent.com/39618015/60344173-368fc480-99b6-11e9-938c-503a1de05a0c.png)

The status of your image can be **_Uncommitted changes_** or **_Fetch required_**. Follow the option 1 or 2:

1. In the first case, if the status of your image goes to **_Uncommited changes_**, you need to do a **_Fetch_** to download your repository data and synchronize it with your local image and go to **Step 2**:

![image](https://user-images.githubusercontent.com/39618015/60344218-53c49300-99b6-11e9-82c6-b05d725cb025.png)

2. In this second case, **_Fetch required_**, do a **_Fetch_** in the repository and follow the next steps:

![image](https://user-images.githubusercontent.com/39618015/60452215-59c4a900-9c2e-11e9-9409-5c82bc19eb9b.png)

Now the new status of your image is **_Detached Working Copy_**. To fix it, go to **_Repair repository_**, select **_Discard image changes_**, select this option to do checkout **_DO NOT CHECKOUT any packages_** and press **_Checkout_** button

![image](https://user-images.githubusercontent.com/39618015/60451687-ea9a8500-9c2c-11e9-8682-14e6b085f9b2.png)
![image](https://user-images.githubusercontent.com/39618015/60451711-fd14be80-9c2c-11e9-8de6-4c4622880dcd.png)
![image](https://user-images.githubusercontent.com/39618015/60452771-980e9800-9c2f-11e9-9a05-1512a665ef67.png)

## Step 2 Synchronize your local repository with official Pharo repository

Now you need to create a **_New branch_**, because we need to delete our local branch to load it from the official repository:
![image](https://user-images.githubusercontent.com/39618015/60453327-29cad500-9c31-11e9-9c5c-4ec293248023.png)
![image](https://user-images.githubusercontent.com/39618015/60344288-7fe01400-99b6-11e9-922e-e42f3ebb4c31.png)

Now we are going to delete the local branch:
Select **_Repository_**, select in local **_Branches_** the branch that you want to update and then delete it. In this case **_Pharo8.0_**:
![image](https://user-images.githubusercontent.com/39618015/60453532-b07fb200-9c31-11e9-9afb-33b05561d878.png)
![image](https://user-images.githubusercontent.com/39618015/60344406-c6357300-99b6-11e9-8580-ac30fd30c108.png)

Now you can do **_Checkout branch_** in the remote branch. 
Go to **_Remotes/pharo-project_** and select **_Checkout branch_** in **_Pharo8.0_**:
![image](https://user-images.githubusercontent.com/39618015/60344474-ea914f80-99b6-11e9-83fa-2df3fd8cfe6d.png)

Be sure you have selected this option to do checkout **_DO NOT CHECKOUT any packages_**. 
This means we are going to update only the local repository, without applying the new changes in the current image:
![image](https://user-images.githubusercontent.com/39618015/60453766-559a8a80-9c32-11e9-897c-75a5f0146c9c.png)

## Step 3 Push the updated data to your remote repository 

![image](https://user-images.githubusercontent.com/39618015/60344592-30e6ae80-99b7-11e9-93ae-38e69772a8c5.png)

Be sure you are selecting your repository to Push in it. 
Enter your Github login and now you have your Github repository updated with the official Github Pharo Project Repository:
![image](https://user-images.githubusercontent.com/39618015/60454247-a5c61c80-9c33-11e9-8c45-e3f502cbc8b6.png)

The status of the repository in Iceberg is **_Uncommitted changes_**, but you don't need to commit it.
Your Github repository already is updated:
![image](https://user-images.githubusercontent.com/39618015/60344707-6f7c6900-99b7-11e9-8b18-36238107224f.png)
![image](https://user-images.githubusercontent.com/39618015/60344735-80c57580-99b7-11e9-9098-349a9d4b0598.png)

# Command line

### Update your Pharo fork using the command line

You can also update your Pharo fork using the command line in 6 commands. You need to have a git command line installed.

1. $ git clone https://github.com/YOUR-USER-NAME/pharo.git
2. $ cd Pharo
3. $ git remote add pharo https://github.com/pharo-project/pharo.git 
4. $ git fetch pharo
5. $ git pull pharo Pharo8.0
6. $ git push origin Pharo8.0

![image](https://user-images.githubusercontent.com/39618015/60595538-7fc18900-9da7-11e9-8cf2-a454e1ee220a.png)
