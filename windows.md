# Windows

* We will be installing multiple applications.
* The installation steps will be provided for each application.
* You should be able to copy and paste the lines into Windows Command.
* We recommend that you configure your system so that you can see both the instructions and Terminal at the same time.

## What you'll need

* [Editor](##editor)
* [Git](##git)
* [Go and Go env setup](##go-and-go-env-setup)

## Editor

For this workshop, unless you already have an editor, we suggest to download
Atom from their [website](http://atom.io) and install it.

## Git

If you don't have a Github account, go to https://github.com/ and create a new account.

Download the latest version of [Git for Windows](https://github.com/git-for-windows/git/releases/tag/v2.11.0.windows.3)

After installation go to `Start` -> `All Programs` -> `Git` -> `Git Bash` and
generate ssh key:

```
$ ssh-keygen -t rsa -C "doe@gmail.com"
```

Go to `C:\Users\<your_user>\.ssh`, open the file `id_rsa.pub`,
copy the contents, go to to your Github profile and paste them [here](https://github.com/settings/keys)


## Go and Go env Setup

Download the latest 64-bit Go MSI package from https://golang.org/dl/

Install Go in `C:\Go\bin`

Ensure Go binary is in your `Path`.

Go to `System` -> `Advanced System Settings` -> `Environment Variables`

Select `Path` under `System variables` and append `;C:\Go\bin` to the current
value.

Test the installation by opening the Windows Command and typing:

```
go version
```

### Go workspace

Go workspace would be the physical place on the disk to store your Go codes.

It is good practice to maintain one place to load and work on you Go projects.

Create `C:\Users\<your_user>\code` and `C:\Users\<your_user>\code\src`

Ensure `GOPATH` is set to the path of the Go workspace that you just created

Go to `System` -> `Advanced system settings` -> `Environment Variables`

Click `New` under `System Variables`

```
Variable name: GOPATH
Variable value: C:\Users\<your_user>\code\go
```

Ensure the GOPATH has been set, open up Windows Command and type the following:

```
echo %GOPATH%
```

The command should output the Variable value you just set:

```
C:\Users\<your_user>\code\go
```

### Testing

Test Go packages installation by running typing the following on Windows Command:


```
go get github.com/golang/example/hello
```

```
%GOPATH%/bin/hello.exe
```

## Have fun with Go!

![aww yeah](http://i.imgur.com/AmFax.gif)
