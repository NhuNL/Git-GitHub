
# GitHub setup

## Get access to the course organisation

1. [Sign up to GitHub Enterprise](https://git.generalassemb.ly/join) if you haven't already

1. Send us your username

1. Wait to be granted access to the course organisation [`DS-LDN-30`](https://git.generalassemb.ly/DS-LDN-30)

## Fork and clone the course materials

1. Open the [`DS30-Course-Materials`](https://git.generalassemb.ly/DS-LDN-30/DS30-Course-Materials) repository page in GitHub Enterprise

1. Fork the repository into your account and note down its URL (which will look like `https://git.generalassemb.ly/your-username/DS30-Course-Materials.git`)

1. Open a terminal

1. Move to the folder where you'd like to store the course materials

1. Clone your fork to a local repository
    ```bash
    git clone https://git.generalassemb.ly/your-username/DS30-Course-Materials.git
    ```

1. Add the repository in the course organisation as another remote repository
    ```bash
    git remote add upstream https://git.generalassemb.ly/DS-LDN-30/DS30-Course-Materials.git
    ```

1. Confirm that you have two remote repositories set up (with different URLs)
    ```bash
    git remote -v
    ```

## Pull changes from the course repository

At the start of each session:

1. Make sure you have committed any changes you wish to keep

1. Pull from the course repository
    ```bash
    git pull upstream master
    ```

1. Accept the commit message for the merge

1. Update your fork
    ```bash
    git push origin master
    ```

### Conflict resolution

In case of conflicts:

1. For each conflicted file, decide whether to keep your version (`--ours`) or the one in the course repository (`--theirs`)
    ```bash
    git checkout --ours path/to/conflicted.file
    ```

1. Add and commit any changes

## Push changes to your fork

At the end of each session:

1. Add and commit any changes you wish to store

1. Push to your fork
    ```bash
    git push origin master
    ```
