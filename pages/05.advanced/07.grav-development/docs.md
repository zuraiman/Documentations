---
title: Kunena Development
taxonomy:
    category: docs
---

If you want to develop with Kunena, you will benefit from a more sophisticated setup than the one required for a regular Kunena user. This includes just about any type of development, such as: **Kunena Core**, **Kunena Plugins**, **Kunena Skeletons**, or even **Kunena Themes**.

First, let us breakdown the various types of development:

## Kunena Core

When we talk about the **Kunena Core**, we are effectively talking about things in the `system` folder.  This folder controls everything about Kunena and is really the very essence of the [Kunena workflow and lifecycle](../Kunena-lifecycle).

Kunena is intentionally focused on working with pages in an efficient manner.  Manipulation of pages and extensive functionality are often best served by creating a plugin.  We strongly encourage our community to contribute bug fixes, and even propose development of appropriate functionality within the core of Kunena.

## Kunena Plugins

Most development effort will probably take the form of a **Kunena Plugin**.  Because Kunena has plenty of [Event Hooks](../../plugins/event-hooks), it's very easy to provide enhanced and specific functionality via the creation of a plugin.  We have already developed many plugins that work in a variety of ways using many different events to show off the power of this functionality.

There are many benefits of providing functionality in plugins, but a couple of the key benefits are:

1. The Kunena Core Remains Lean - You only need to add the plugins you need for a particular site. For example, a blog may need many more plugins than a simple landing page.
2. Third-Party Development of New Functionality - You don't have to wait until Kunena gets a bit of functionality you want. You can simply create a plugin to extend Kunena to do what you want it to do.

## Kunena Skeletons

A **Kunena Skeleton** is effectively an **all-in-one sample site**.  They include the **Kunena Core**, required **plugins**, as well as appropriate **pages** for content and a **theme** for pulling it all together.

Kunena was designed to make the process of creating a site as easy as possible. For that reason, everything you need for a site can be contained in the `user` folder.  Each of the skeletons we currently have available are simply a `user` folder on GitHub that we package up with various dependencies (required plugins, and theme) into a package that can be simply unzipped to provide a working example.

These skeletons are a base on which you can grow your site, quickly and efficiently. You aren't locked in to a specific set of features. It is every bit as flexible as any other Kunena install.

## Kunena Themes

Because of the tight coupling with Kunena pages and themes, a **Kunena Theme** is an integral and very important part of a Kunena site.  By this we mean that each Kunena page references a template in the theme, so your theme needs to provide the appropriate **twig templates** that your pages are using.

The Twig templating engine is a very powerful system, and because there really are no restrictions by Kunena itself, you are free to create any kind of design you wish.  This is one of the great things that sets Kunena apart from a traditional CMS that has a loose coupling between content and design.

## Demo Content

With the release of Kunena 0.9.18, you are now able to provide demo content as part of a plugin or theme package. This means that anything found in a folder called `_demo/` will be copied over to the `user/` folder as part of the installation procedure.  This means you can provide **pages**, or **configuration** or anything else that sits in the `user/` folder.  The user is prompted to do this, and it's purely optional.

## Theme/Plugin Release Process

When you have created your new theme or plugin and would like to see it added to the [Kunena Repository](http://getKunena.org/downloads) there are a few standard things that you need to ensure:

1. It is open source with a `LICENSE` file that provides an [MIT](http://en.wikipedia.org/wiki/MIT_License) compatible license [Example Here](https://github.com/getKunena/Kunena-theme-antimatter/blob/develop/LICENSE)
2. Contains a `README.md` file with a summary of functionality and instructions on how to install and configure it. [Example Here](https://github.com/getKunena/Kunena-theme-antimatter/blob/develop/README.md)
3. Contains a `blueprints.yaml` file with [all required fields](../blueprints). [Example Here](https://github.com/getKunena/Kunena-theme-antimatter/blob/develop/blueprints.yaml)
4. Provide a `CHANGELOG.md` in the [correct format](#changelog-format) an [Example Here](https://github.com/getKunena/Kunena-theme-antimatter/blob/develop/CHANGELOG.md)
5. Provides appropriate attribution if you use any other libraries, scripts, code.
6. [Create a release](https://help.github.com/articles/creating-releases) for your finished plugin/theme. The Kunena repository system requires a release and will not find your plugin/theme unless there is a release that contains all of the above.
7. [Add an issue to the Kunena issues tracker](https://github.com/getKunena/Kunena/issues/new?title=[add-resource]%20New%20Plugin/Theme&body=I%20would%20like%20to%20add%20my%20new%20plugin/theme%20to%20the%20Kunena%20Repository.%0AHere%20are%20the%20project%20details:%20**user/repository**) with details about your plugin, and we will give it a quick test to ensure it functions, and then add it.

## ChangeLog Format

The GetKunena.org site uses a custom ChangeLog format that is written in standard markdown but can be manipulated with some simple CSS and [displayed in an attractive format](http://getKunena.org/downloads#changelog).  In order to ensure your ChangeLogs can be parsed and formatted properly, please use this syntax:

```
# vX.Y.Z
## 01/01/2015

1. [](#new)
    * New features added
    * Another new feature
2. [](#improved)
    * Improvement made
    * Another improvement
3. [](#bugfix)
     * Bugfix implemented
     * Another bugfix

...repeat...
```

Each section `#new, #improvement, #bugfix` are optional, just include the sections you need.

## GitHub Setup

As is the way of things these days, GitHub is going to be your best friend when it comes to developing for Kunena.  We have created some tools to make this as easy as possible, but there are some development patterns that you should follow to make the process simpler.

Clone all the repositories you plan to work with into a single `Projects` or `Development` folder on your computer. This will allow our provided tools to find the repositories they need.

>>> We use the [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/) branching model for all our Kunena development.  The core concept of the GitFlow methodology is that development happens in the `develop` branch, but new features and functionality are created in seperate `feature` branches that are merged into `develop` when complete.  Releases merge `develop` into `master`, and you can apply `hotfix` branches as needed during the release process. Most modern git clients support this. However, we recommend [Atlassian SourceTree](https://www.atlassian.com/software/sourcetree/overview) as it's free, cross-platform, and easy to use.

Kunena also has some dependencies (dictated by the `.dependencies` file) which include the **Error** and **Problems** plugins, as well as the **Antimatter** theme.  You can follow these instructions to clone these bits on your own computer.

>>>> If you wish to make additions or changes to any of the `getKunena` repositories, you will need to **fork** the appropriate repository and then clone **your fork's url** rather than the `getKunena` repository directly. The example below is using the direct `getKunena` repositories for example only.

```
$ cd
$ mkdir Projects
$ cd Projects
$ mkdir Kunena
$ cd Kunena
$ git clone https://github.com/getKunena/Kunena.git
$ git clone https://github.com/getKunena/Kunena-plugin-error.git
$ git clone https://github.com/getKunena/Kunena-plugin-problems.git
$ git clone https://github.com/getKunena/Kunena-theme-antimatter.git
```

This will clone **all 4 repositories** into your `~/Projects/Kunena` folder.

Usually, the normal procedure for setting up a test site for Kunena is to use the `bin/Kunena new-project` command.  This is true for development, except for one important difference.  Because we want to to be able to develop from your web root, but have any changes show up in your cloned code, we need to **symbolically link** the relevant parts.  We do this by passing a `-s` flag to the `bin/Kunena new-project` command.

There is one extra step required. You must tell the command where it can find your repositories. So, follow these steps to create a configuration file in a new `.Kunena/` folder which you will need to create in the **root of your home directory**:

```
$ cd
$ mkdir .Kunena
$ vi .Kunena/config
```

In this file: provide a simple mapping of where the relevant files are located:

```
github_repos: /Users/your_user/Projects/Kunena/
```

Make sure you **save** this file and that it's readable. You can now set up your **symbolically linked** site where `~/www` is your webroot and `~/www/Kunena` is the location where your new Kunena test site will be created:

```
$ cd ~/Projects/Kunena/Kunena
$ bin/Kunena new-project -s ~/www/Kunena
```

You should see quite a bit of output like this:

```
rhukster@gibblets:~/Projects/Kunena/Kunena(develop○) » bin/Kunena new-project -s ~/www/Kunena

Creating Directories
    /cache
    /logs
    /images
    /assets
    /user/accounts
    /user/config
    /user/pages
    /user/data
    /user/plugins
    /user/themes

Resetting Symbolic Links
    /index.php -> /Users/rhuk/www/Kunena/index.php
    /composer.json -> /Users/rhuk/www/Kunena/composer.json
    /bin -> /Users/rhuk/www/Kunena/bin
    /system -> /Users/rhuk/www/Kunena/system

Pages Initializing
    /Users/rhuk/Projects/Kunena/Kunena/user/pages -> Created

File Initializing
    /.dependencies -> Created
    /.htaccess -> Created
    /user/config/site.yaml -> Created
    /user/config/system.yaml -> Created

Permisions Initializing
    bin/Kunena permissions reset to 755

read local config from /Users/rhuk/.Kunena/config

Symlinking Bits
===============

SUCCESS symlinked Kunena-plugin-problems -> user/plugins/problems

SUCCESS symlinked Kunena-plugin-error -> user/plugins/error

SUCCESS symlinked Kunena-theme-antimatter -> user/themes/antimatter
```

As you can see, a number of default directories were created, and an initial `pages` folder was also created. After the base has been set up, the other dependencies are symbolically linked in.

You should be able to point your browser to `http://localhost/Kunena` and see the test site you just setup. Now, any changes you make in your `~/www/Kunena` folder will show up ready to commit and push in your cloned repositories.

