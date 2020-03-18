# Install Git LFS

Before we can begin using Git LFS, we need to install it on our local machine. Below are the steps for installing Git LFS on your machine based on your operating system. 

#### MacOS

1. Navigate to [git-lfs.github.com](https://git-lfs.github.com/) and click **Download**. Alternatively, you can install Git LFS using a package manager:

    - To use [Homebrew](Homebrew), run `brew install git-lfs`.
    - To use [MacPorts](https://www.macports.org/), run `port install git-lfs`.

> If you install Git LFS with Homebrew or MacPorts, skip to step six.

1. On your computer, locate and unzip the downloaded file.
1. Open Terminal.
1. Change the current working directory into the folder you downloaded and unzipped.

```sh
$ cd ~/Downloads/git-lfs-1.X.X
```

> Note: The file path you use after `cd` depends on your operating system, Git LFS version you downloaded, and where you saved the Git LFS download.

1. To install the file, run this command:

```sh
$ ./install.sh
> Git LFS initialized.
```

> Note: You may have to use `sudo ./install.sh` to install the file.

1. Verify that the installation was successful:

```sh
$ git lfs install
> Git LFS initialized.
```

#### Windows 

1. Navigate to [git-lfs.github.com](https://git-lfs.github.com/) and click **Download**.

> Tip: For more information about alternative ways to install Git LFS for Windows, see this [Getting started guide](https://github.com/github/git-lfs#getting-started).

1. On your computer, locate the downloaded file.
1. Double click on the file called _git-lfs-windows-1.X.X.exe_, where 1.X.X is replaced with the Git LFS version you downloaded. When you open this file Windows will run a setup wizard to install Git LFS.
1. Open Git Bash.
1. Verify that the installation was successful:

```sh
$ git lfs install
> Git LFS initialized.
```
