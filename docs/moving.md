# Moving the file to Git LFS

Before we tell Git LFS what files to track, we should identify what files are taking up the most space in our repository.

#### Exploring the repository files

1. Open your command line application.
1. Change your current working directory to the `lfs-example` repository.
1. Run `git lfs migrate info`, your output should look similar to:

        ```sh
        migrate: Fetching remote refs: ..., done.                               migrate: Sorting commits: ..., done.                               migrate: Examining commits: 100% (0/0), done. 
        ```

    By default, `git lfs migrate info` only displays files that don't exist within commits on the remote repository.
1. Run `git lfs migrate info --everything`, your output should look similar to:

        ```sh
        migrate: Sorting commits: ..., done.                               migrate: Examining commits: 100% (8/8), done.    
        *.dmg 	18 MB 	  1/1 files(s)	100%
        *.md  	6.4 KB	10/10 files(s)	100%
        *.html	2.5 KB	  4/4 files(s)	100%
        ```

> Note: If we only wanted to include files above a specific size, we could modify the previous command with `--above=1mb`

Now that we have identified the file that needs to be tracked with Git LFS it is time to import it into Git LFS and automatically fix the existing history of the project. 

#### Migrating the file to Git LFS

1. In your command line application run, `git lfs migrate import --everything --include="*.dmg"`.

    This is going to modify the history of the project to include the object that is now tracked in Git LFS.

1. To push the changed history run, `git push --force`.

    This is going to rewrite the commit history of the project. Keep in mind all people working on the project should be made aware that this needs to occur.