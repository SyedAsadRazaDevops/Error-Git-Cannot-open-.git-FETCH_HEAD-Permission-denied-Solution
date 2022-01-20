# Error-Git-Cannot-open-.git-FETCH_HEAD-Permission-denied-Solution


Git repositories contain a special folder called .git/. You may not have seen this folder because it is hidden. The hidden status of this folder is denoted by the full stop (“.”) that comes at the start of the folder name.

This folder contains various pieces of metadata about a repository. It tracks your project-specific configuration options, the references in your project, your current HEAD, among other crucial pieces of information about your repository.

Git needs read and write access to this folder. This is because its contents will change as you run commands like **git config **and **git pull**.

>run command on server:
```
git pull
```
>This command returns:
```
error: cannot open .git/FETCH_HEAD: Permission denied
```

# The Solution
We run tis command in repository using the “sudo” command. 

but not recommended for permanet solution,

To fix this issue, we are going to change the ownership of the files in our folder. We can do this using the chown command:
```
sudo chown -R <user-name>:staff  .git/file-path
```

This command changes the ownership details of all the files and folders in our repository, including the .git/ folder. 
We are now the owner of the directory and have full access to the project folder. 
We should now be able to pull our code:
```
git pull
```

thankyou!
