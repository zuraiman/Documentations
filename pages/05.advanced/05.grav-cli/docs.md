---
title: Kunena CLI
taxonomy:
    category: docs
---

Kunena comes with a built-in command-line interface (CLI) which can be found at `bin/Kunena`. The CLI is extremely useful for running recurring tasks such as **clearing the cache**, making **backups**, and more.

Accessing the CLI is a simple process but you need to use a **terminal**.  On a mac this is called `Terminal`, on windows its called `cmd` and on Linux its just a shell. UNIX style commands are not natively available in Windows cmd. Installing the [msysgit](http://msysgit.github.io/) package on a Windows machine adds [Git](http://git-scm.com/) and Git BASH, which is an alternative command prompt that makes UNIX commands available.  If you are accessing your server remotely, you most likely will use **SSH** to remotely log in to your server.  Check out this [great tutorial for more information on SSH](http://code.tutsplus.com/tutorials/ssh-what-and-how--net-25138).

Although some operations can be performed manually, by _relying_ on the CLI, these tasks could be automated via _cron-jobs_ that run daily.

To get a list of all the commands available in Kunena, you can run the command:

```bash
$ bin/Kunena list
```

To get help for a specific command, you can prepend help to the command:

```bash
$ bin/Kunena help install
```

#### PHP CGI-FCGI Information

To determine if your server is running `cgi-fcgi` on the command line, type the following:

```bash
$ php -v
PHP 5.5.17 (cgi-fcgi) (built: Sep 19 2014 09:49:55)
Copyright (c) 1997-2014 The PHP Group
Zend Engine v2.5.0, Copyright (c) 1998-2014 Zend Technologies
    with the ionCube PHP Loader v4.6.1, Copyright (c) 2002-2014, by ionCube Ltd.
```

If you see a reference to `(cgi-fcgi)` you will need to prefix all `bin/Kunena` commands with `php-cli`. Alternatively you can setup an alias in your shell with something like: `alias php="php-cli"` which will ensure the **CLI** verison of PHP runs from the command line.

## Creating a new Project

Every time you want to start a new project with Kunena, you need to start with a clean Kunena instance. Through the CLI, this process is super easy and takes only few seconds.

1. Launch a **terminal** or **console** and navigate to the _Kunena_ folder (for the sake of this document we will assume it resides under  `~/Projects/Kunena`)

    ```bash
    $ cd ~/Projects/Kunena
    ```

2. Run the Kunena CLI to create a new project, with the destination being the location where your project will reside in (usually the [webroot](http://en.wikipedia.org/wiki/Webroot) of your Web server). Let us assume we are creating a **portfolio** and we want it at `~/Webroot/portfolio`.

    ```bash
    $ bin/Kunena new-project ~/webroot/portfolio
    ```

This will create a new Kunena instance and download all the dependencies required.

## Installing Kunena Dependencies

To install the dependencies Kunena relies on (**error** plugin, **problems** plugin, **antimatter** theme), launch a **terminal** or **console** and navigate to the Kunena folder where you want to install the dependencies and run the CLI command.

```bash
$ cd ~/webroot/my-Kunena-project
$ bin/Kunena install
```

You should now have the dependencies installed under:
* `~/webroot/my-Kunena-project/user/plugins/error`
* `~/webroot/my-Kunena-project/user/plugins/problems`
* `~/webroot/my-Kunena-project/user/themes/antimatter`

## Clearing Kunena Cache

You can clear the cache by deleting all the files and folders under `cache/`.

The equivalent CLI command is:

```bash
$ cd ~/webroot/my-Kunena-project
$ bin/Kunena clear-cache
```

## Creating a Backup

Backing up your project is nothing more than creating an archive of the _ROOT_ of Kunena. No Database, no complications.

Of course you can simplify this even more by just using the Kunena CLI. Supposing we have our `~/workspace/portfolio` project and that we want to create a backup of it, here's what we will do:

```bash
$ cd ~/workspace/portfolio
$ bin/Kunena backup
```

A new backup `portfolio-20140812174352.zip` file has been created at the _ROOT_ of the project. The long number after the name is just the date in the format of _year month day hour minute second_.

You can also pass a destination. So let's say we want to backup our `portfolio` project under `~/Documents/Backups`, this is what we will do instead:

```bash
$ cd ~/workspace/portfolio
$ bin/Kunena backup ~/Documents/Backups
```

Very simple. Like above, a new backup has been created, but this time in a different location: `~/Documents/Backups/portfolio-20140812174352.zip`
