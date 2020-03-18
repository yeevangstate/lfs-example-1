# Using Git LFS in other projects

Git LFS is useful in more projects than the repository we used for this training exercise. This section reviews how you can use Git LFS in the future in other projects you work on.


### New Projects

#### Tell LFS what files to tracking

To tell Git LFS which files you want it to track in a new project perform the following steps. 

> Note: The example repository is used just to provide context to the instructions.

1. Open your command line application.
1. Change your current working directory to the `lfs-example` repository.
1. To associate a file type in your repository with Git LFS, run `git lfs track` followed by the name of the file extension you want to automatically upload to Git LFS.

For example, to associate the .dmg file, enter the following command:

```sh
$ git lfs track "*.dmg"
> Adding path *.dmg
```

Every file type you want to associate with Git LFS will need to be added with `git lfs track`. This command amends your repository's `.gitattributes` file and associates large files with Git LFS.

> Note: We strongly suggest that you commit your local `.gitattributes` file into your repository. Relying on a global `.gitattributes` file associated with Git LFS may cause conflicts when contributing to other Git projects.
