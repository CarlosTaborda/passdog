# Passdog
Is a very simple command line tool to manage passwords for Linux or WSL, passdog protect
your passwords in a keychain encrypted  by AES256, you can add, edit, search and list your passwords.
Passdog create a file that contains all your passwords, you set  one password to protect the keychain.

You can enable synchronizing with github creating a private repo and setting 
```bash
export PASSDOG_REPO="git@github.com:user/repo.git
export PASSDOG_REPOKEYPATH="/home/user/.ssh/id_github
```
in you .bashrc file


![](https://raw.githubusercontent.com/CarlosTaborda/passdog/main/passdog.gif)
# Install
- Download passdog from this repo
- Copy the passdog file to bin folder 
- Go to use

# Requirements
vim, gpg, grep, column, sed, zip, unzip, git


# Basic Usage
The keychain path is
```bash
~/.passdog/passdogstore.csv
```

For initialize the Keychain 
```bash
passdog -i
```

For add a credential to  the Keychain 
```bash
passdog -pc
```

For list all passwords
```bash
passdog -pl
```

For search a crendential
```bash
passdog -ps "search_term"
```

For delete a crendential (2 is the credential number usage -ps option to know it)
```bash
passdog -pd 2
```

For display usage
```bash
passdog -h
```

For edit the file that contain all credentials
```bash
passdog -pe
```
and get info about more functions like: remove storage, remove credentials, generate ramdom password...

if you want migrate your keychain only copy the **~/.passdog/passdogstore.csv** to new machine in the ~/ directory

## _Full list options_
![](https://raw.githubusercontent.com/CarlosTaborda/passdog/main/passdog_help.PNG)