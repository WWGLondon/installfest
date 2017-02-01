# Mac OSX #
===================

## Notes

* We will be installing multiple applications.
* The installation steps will be provided for each application.
* You should be able to copy and paste the lines into Terminal.
* Many instructions start with a dollar sign (`$`), this is a convention used to indicate a bash/terminal command. (**DO NOT** include the `$` sign when you copy & paste the command to your terminal)
* Replace anything with capital letters like `YOUR_NAME` with your own credentials.
* We recommend that you configure your system so that you can see both the instructions and Terminal at the same time.

## What you'll need

* [Editor](##editor)
* [Terminal](##terminal)
* [Xcode Command Line Tools](##xcode-command-line-tools)
* [Homebrew](##homebrew)
* [Git](##git)
* [Go and Go env setup](##go-and-go-env-setup)

## Editor

* For this workshop, unless you already have an editor, we suggest to download Atom from their [website](http://atom.io).
* Once you have that file, you can click on it to extract the application and then drag the new Atom application into your "Applications" folder.
* Install [`go-plus`](https://atom.io/packages/go-plus) plugin for your brand new editor:
  * On the application, open the settings either by clicking it from the drop down menu `Atom/Preference` or by typing `Command ⌘` + `,`
  * Locate the `+ Install`, click it and type in `go-plus` on the search bar.
  * You'll find `go-plus` package on the search result list, click on the install button to start the installation for the package.
* Another thing that will be quite handy is to install shell commands for Atom, this will allow you to open files from terminal with atom. To do this open the drop down menu `Atom` agin, there would be an option called `Install Shell Command`, click it and you're good to go.

## Terminal

* We will use the terminal quite a lot, in fact, that would be the first thing we need to 'open' now.
* The fastest way to do that is by `terminal` on your Spotlight search bar (top right on your desktop screen).
* Here is the basics terminal commands that might be handy for the future: https://www.youtube.com/watch?v=jDINUSK7rXE

## Xcode Command Line Tools

* We will do this on the terminal: `$ xcode-select --install`
* This would install Xcode CLI into your machine.

## Homebrew

* To install this OSX package manager:

  `$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

* Ensure that everything is up to date:

  `$ brew update && brew upgrade`

* You know it worked if...
   * The output of `$ which brew` is `/usr/local/bin/brew`.
   * The output of `$ brew doctor` is `ready to brew`.

## Git

* To install this version control system on your machine:

  `$ brew install git`

* You know it worked if...
   * The output of `$ git --version` is > 2.0.
* Update your Git configuration:

  `$ git config --global user.name "FIRSTNAME_SPACE_LASTNAME"`

  `$ git config --global user.email "YOUR_EMAIL_ADDRESS"`

  `$ git config --global push.default simple`

* If you don't have a Github account, this is probably the time to do so.
* Go to [github.com](http://github.com) and create an account.
* You would then need to generate your ssh key:

  `$ ssh-keygen -t rsa -C "YOUR_EMAIL_ADDRESS"`

* And then copy it to github.com, you can find your key with:

  `$ atom ~/.ssh/id_rsa.pub`

* Find your github token from [github settings page](https://github.com/settings/tokens), you'd need it for the commands below.
* Don't forget to update your Git configuration (again):

  `$ git config --global github.user "FIRSTNAME_SPACE_LASTNAME"`

  `$ git config --global github.token YOUR_TOKEN`

* You know it worked if...
   * The output of `$ ssh -T git@github.com` is a full welcome phrase from Github.

## Go and Go Env setup

### Downloading Go

* Navigate to https://golang.org/dl/.
* Select the binary distribution for your OS and run the installation program.
* After you run the installation program, Go will be installed at the following location: `/usr/local/go`
* You know it worked if...
   * The output of `$ go env` is not an error message.

### Go Workspace

* Go workspace would be the physical place on the disk to store your Go codes.
* It is good practice to maintain one place to load and work on you Go projects.
* Create folders named `code/go/src` on your `$HOME` folder:

  `$ mkdir -p ~/code/go/src`

* Ensure that you have a `.bash_profile` by running: `ls ~/.bash_profile`
* *IF* you have this response: `No such file or directory` then you need to create the file:

  `touch ~/.bash_profile`

* Update your `.bash_profile` with these environment variables:

  `$ export GOPATH="$HOME/code/go"`

  `$ export GOROOT=/usr/local/go`

  `$ export PATH="$PATH:$GOPATH/bin"`

  `$ export PATH="$PATH:$GOROOT/bin"`

* Source you profile: `$ source ~/.bash_profile`
* You know it worked if...
  * The output of `$ go env` includes non empty `GOPATH`.

## Have fun with Go!

![aww yeah](http://i.imgur.com/AmFax.gif)
