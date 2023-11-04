# MacOS-cheat sheet
Quick reference to most common tools when setting up a new Mac

## Pre-requisites check
```shell
zsh --version
git --version
pip --version
```

### Rosetta

>Rosetta 2 enables a Mac with Apple Silicon to use apps built for a Mac with an Intel processor.

```shell
sudo softwareupdate --install-rosetta
```
[Apple Support](https://support.apple.com/en-au/HT211861)

## Install Oh-my-zsh

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
[Oh-my-zsh](https://ohmyz.sh/#install)

## Command Line Tools (CLT) for Xcode

```shell
xcode-select --install
```

## Install Homebrew

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
Follow the post-installation steps listed in your Terminal.

[Homebrew](https://docs.brew.sh/Installation)

## Generate SSH Keys
Follow the steps on the [GitHub guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Generate GPG keys
```shell
brew install gnupg
gpg --version
```
Follow the steps on the [GitHub guide](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)

## AWS CLI
```shell
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
sudo installer -pkg AWSCLIV2.pkg -target /
which aws
aws --version
```
[Installation Guide for version 2](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
[Set up the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-quickstart.html)