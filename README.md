

# Git Workflow Guide

Follow these steps to set up and manage your Git repository:

## Step 1: Initialize a new Git repository
```sh
git init
```

## Step 2: Add your files to the staging area
```sh
git add .
```

## Step 3: Commit your changes with a message
```sh
git commit -m "Initial commit"
```

## Step 4: Create a new repository on GitHub
Do this on the GitHub website.

## Step 5: Add the remote repository URL
```sh
git remote add origin https://github.com/your-username/your-repository.git
```

## Step 6: Push your code to the remote repository
```sh
git push -u origin master
```

## Step 7: Pull the latest changes from the remote repository
```sh
git pull origin master
```

## Step 8: Create and switch to a new branch for development
```sh
git checkout -b development
```

## Step 9: Push the development branch to the remote repository
```sh
git push -u origin development
```

## Step 10: Create and switch to a new branch for production
```sh
git checkout -b production
```

## Step 11: Push the production branch to the remote repository
```sh
git push -u origin production
```

## Step 12: Merge changes from development to production
```sh
git checkout production
git merge development
```

## Step 13: Push the merged changes to the remote production branch
```sh
git push origin production
```

