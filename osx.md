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
     `$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
  * Ensure that everything is up to date:
     `$ brew update && brew upgrade`
  * You know it worked if...
     * The output of `$ which brew` is `/usr/local/bin/brew`.
     * The output of `$ brew doctor` is `ready to brew`.

## Git

  * To install this version control system on your machine: `$ brew install git`
  * You know it worked if...
     * The output of `$ git --version` is > 2.0.

## Go and Go Env setup
