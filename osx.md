# Mac OSX #
===================

## Notes

* We will be installing multiple applications.
* The installation steps will be provided for each application.
* You should be able to copy and paste the lines into Terminal.
* Many instructions start with a dollar sign ($), this is a convention used to indicate a bash/terminal command.
* We recommend that you configure your system so that you can see both the instructions and Terminal at the same time.

## What you'll need

* [Editor](##editor)
* [Terminal](##terminal)
* [Xcode Command Line Tools](##xcode-command-line-tools)
* [Homebrew](##homebrew)
* [Git](##git)
* [Go and Go env setup](##go-and-go-env-setup)

## Editor

* For this workshop, unless you already have an editor, we suggest to download Atom from their [website](http://atom.io) and install it.
* Install `go-plus` plugin for your brand new editor, by typing `Command ⌘` + `,`.
* Type `go-plus` and install the package.

## Terminal

* We will use the terminal quite a lot, in fact, that would be the first thing we need to 'open' now.
* The fastest way to do that is by using spotlight search: `Command ⌘` + `Spacebar` and type `iterm`.

## Xcode Command Line Tools

* We will do this on the terminal: `$ xcode-select --install`
* This would install Xcode CLI into your machine.

## Homebrew

* To install this OSX package manager:

```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
```

* Ensure that everything is up to date:

```
$ brew update && brew upgrade`
```

* You know it worked if...
   * The output of `$ which brew` is `/usr/local/bin/brew`.
   * The output of `$ brew doctor` is `ready to brew`.

## Git

* To install this version control system on your machine: `$ brew install git`
* You know it worked if...
   * The output of `$ git --version` is > 2.0.
* Update your Git configuration:

```
$ git config --global user.name "Jane Doe"
$ git config --global user.email "doe@gmail.com"
$ git config --global push.default simple
```

* If you don't have a Github account, this is probably the time to do so.
* Go to github.com and create an account.
* You would then need to generate your ssh key: `$ ssh-keygen -t rsa -C "doe@gmail.com"`
* And then copy it to github.com, you can find your key with: `$ atom ~/.ssh/id_rsa.pub`
* Don't forget to update your Git configuration (again):

```
$ git config --global github.user "Jane Doe"
$ git config --global github.token your_token_here
```

* You know it worked if...
   * The output of `$ ssh -T git@github.com` is a full welcome phrase from Github.

## Go and Go Env setup

### Downloading Go

* Navigate to https://golang.org/dl/.
* Select the binary distribution for your OS and run the installation program.
* After you run the installation program, Go will be installed at the following location: /usr/local/go
* You know it worked if...
   * The output of `$ go env` is not an error message.

### Go Workspace

* Go workspace would be the physical place on the disk to store your Go codes.
* It is good practice to maintain one place to load and work on you Go projects.
* Create folders named `code/go/src` on your `$HOME` folder:
```
$ mkdir -p ~/code/go/src
```
* Update your `.bash_profile` with these enviromental variable:

```
$ export GOPATH="$HOME/code/go"
$ export GOROOT=/usr/local/go
$ export PATH="$PATH:$GOPATH/bin"
$ export PATH="$PATH:$GOROOT/bin"
```

* Source you profile: `$ source .bash_profile`
* You know it worked if...
* The output of `$ go env` includes non empty `GOPATH`.

## Have fun with Go!

![aww yeah](http://i.imgur.com/AmFax.gif)
