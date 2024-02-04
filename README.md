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


## NVM
```shell
brew update
brew install nvm
```

Follow the post-installation instructions. e.g. "You should create NVM's working directory if it doesn't exist":
```shell
mkdir ~/.nvm
```

## Node
```shell
nvm install 20
```

## Composer
A Dependency Manager for PHP
```shell
brew install composer
```
[Basic usage](https://getcomposer.org/doc/01-basic-usage.md)

## PHP
```shell
brew search php
brew install php
php -v
```
> To enable PHP in Apache add the following to httpd.conf and restart Apache:
LoadModule php_module /opt/homebrew/opt/php/lib/httpd/modules/libphp.so

    <FilesMatch \.php$>
        SetHandler application/x-httpd-php
    </FilesMatch>

> Finally, check DirectoryIndex includes index.php
DirectoryIndex index.php index.html

> The php.ini and php-fpm.ini file can be found in:
/opt/homebrew/etc/php/8.3/

> To start php now and restart at login:
brew services start php
Or, if you don't want/need a background service you can just run:
/opt/homebrew/opt/php/sbin/php-fpm --nodaemonize

```shell
cd /etc/apache2
sudo vi httpd.conf
```

## MySQL
```shell
brew install mysql
```

> We've installed your MySQL database without a root password. To secure it run:
mysql_secure_installation

> MySQL is configured to only allow connections from localhost by default

> To connect run:
mysql -u root

> To start mysql now and restart at login:
brew services start mysql
Or, if you don't want/need a background service you can just run:
/opt/homebrew/opt/mysql/bin/mysqld_safe --datadir\=/opt/homebrew/var/mysql

## TablePlus
[Download](https://tableplus.com/download)