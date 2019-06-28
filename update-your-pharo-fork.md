# Update your Pharo fork with the official repository

**Scenario**: You have a fork of Github Pharo Project and you would like to update it with the official repository [github.com/pharo-project/pharo](github.com/pharo-project/pharo). 
In this tutorial you will learn how to update a *Branch* in you repository. 
If you want to update all your repository, just repeate this procedure to all the branchs.  

This tutorial has 3 steps: 

1. Create a new image and sincronize your remote repository
2. Sincronize your local repository with official Pharo repository
3. Push the updated data to your remote repository 

## Step 1 – Create a new image and sincronize your remote repository

Create a new Pharo Image and open Iceberg. Go to repair repository and chose **_Clone again this repository_**. 
Enter the informations of your fork (your Github username/pharo) and select HTTPS:

![image](https://user-images.githubusercontent.com/39618015/60343940-b9fce600-99b5-11e9-94e3-ea1f26f3c3b7.png)
![image](https://user-images.githubusercontent.com/39618015/60344050-faf4fa80-99b5-11e9-862c-75cb9633877c.png)
![image](https://user-images.githubusercontent.com/39618015/60344108-15c76f00-99b6-11e9-9b6e-3106c33609e3.png)

If this error happens, just ignore it, close all the windows and open Iceberg again:
![image](https://user-images.githubusercontent.com/39618015/60344173-368fc480-99b6-11e9-938c-503a1de05a0c.png)

Now you need to do a **_Fetch_** to download your repository data and sincronize it with your local image:
![image](https://user-images.githubusercontent.com/39618015/60344218-53c49300-99b6-11e9-82c6-b05d725cb025.png)

## Step 2 – Sincronize your local repository with official Pharo repository 

Now you need to create a **_New branch_**, because we need to delete our local branch to load it from the official repository:
![image](https://user-images.githubusercontent.com/39618015/60344288-7fe01400-99b6-11e9-922e-e42f3ebb4c31.png)

Now we are going to delete the local branch:
Select **_Repository_**, select in local **_Branches_** the branch that you want to update and than delete it. In this case **_Pharo8.0_**:
![image](https://user-images.githubusercontent.com/39618015/60344382-af8f1c00-99b6-11e9-9106-9d483fb63b4e.png)
![image](https://user-images.githubusercontent.com/39618015/60344406-c6357300-99b6-11e9-8580-ac30fd30c108.png)

Now you can do **_Checkout branch_** in the remote branch. 
Go to **_Remotes/pharo-project_** and select **_Checkout branch_** in **_Pharo8.0_**:
![image](https://user-images.githubusercontent.com/39618015/60344474-ea914f80-99b6-11e9-83fa-2df3fd8cfe6d.png)

Be sure you are selected this option to do checkout **_DO NOT CHECKOUT any packages_**. 
This means we are going to update only the local repository, without apply the new changes in the current image:
![image](https://user-images.githubusercontent.com/39618015/60344535-0f85c280-99b7-11e9-82ce-68962a7e77aa.png)

## Step 3 – Push the updated data to your remote repository 

After your local repositoty be updated with the official repository, you can **_Push_** everything to your own repository:
![image](https://user-images.githubusercontent.com/39618015/60344592-30e6ae80-99b7-11e9-93ae-38e69772a8c5.png)

Be sure you are selecting your repository to Push in it. 
Enter your Github login and now you have your Github repository updated with the official Github Pharo Project Repository:
![image](https://user-images.githubusercontent.com/39618015/60344679-5a9fd580-99b7-11e9-9829-41a2542de860.png)

The status of repository in Iceberg is **_Uncommited changes_**, but you don't need commit it.
Your Github repository already is update:
![image](https://user-images.githubusercontent.com/39618015/60344707-6f7c6900-99b7-11e9-8b18-36238107224f.png)
![image](https://user-images.githubusercontent.com/39618015/60344735-80c57580-99b7-11e9-9098-349a9d4b0598.png)
