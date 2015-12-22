---
title: Installation
taxonomy:
    category:
        - docs
---

### Preparation

The actual installation procedure takes less than two minutes on most sites.  **Kunena** is a Joomla component and it is installed like any other Joomla extension using the Joomla installer.

1. [Technical Requirements](../../basics/requirements)
2. [Read the release notes](../../troubleshooting) for the version of Kunena that you intend to install 
3. Make sure that you have properly implemented Joomla Search Engine Optimisation ([SEO](../../faq/seo)) 
4. What are the recommended file and directory permissions? 

>>> Software installation is not something to be done impulsively.  It requires good planning and site preparation.  The key to a successful and trouble-free upgrade of **Kunena** depends on having a solid Joomla foundation upon which you can build a web-based discussion forum.  This solid foundation relies as much on your own understanding about how to install Joomla extensions as it does on having a dependable hosted environment.


##### The difference between installing and upgrading Kunena
If you never had Kunena (any version) installed before.  If you have installed Kunena before then you should look at the article [Upgrade Guide](../../basics/upgrade). It is important to note that it is **not** necessary to uninstall Kunena in order to upgrade to a new version.

##### Choosing the right installation procedure for you
There are several ways that you can install **Kunena** 

1. By Joomla installer
2. Web installer (At the moment disabled by Joomla)

#### Language support

1. Install joomla languages.
2. Install Kunena language pack.
3. Install Kunena. 

Everything should be translated, sometimes some language strings aren't translated. We need translators todo that. Check [transifex](https://www.transifex.com/Kunena-Forum/) and help us to support your language.
Kunena Language pack supports 58 languages.  The language packs are available from the [download](http://www.kunena.org/download) page.  Just install it by the Joomla installer.

### Installing Kunena

Installation of Kunena is a trivial process. In fact, there is no real installation.  You have **two** options for installing Kunena.  The first, and simplicity way is simply grab the **zip**, the other way is to install the source from **web installer**:

##### Option 1: Install with ZIP package

The easiest way to install Kunena is to use the ZIP package and install it:

1. Download the latest **Kunena** package from the [download](http://kunena.org/downloads) page.
2. Install it by the Joomla installer.


##### Option 2: Install from Web Installer

The alternative method is to install Kunena from the GitHub repository and then run a simple dependency installation script:

1. Go to the web installer
2. Search Kunena, or select it
3. Click on install
4. Kunena will be installed


##### Successful Installation

The first time it loads, there is some compilation happening. Refresh your browser and you will get a faster, cached version.

By default, Kunena comes with some sample topics to give you something to get started with. The forum isn't functional yet, you still need to configure it, add content, extend it, or customize it as much as you like. After the configuration, you must enable the forum item (menu).

##### Installation & Setup Problems

If any issues are discovered during the initial page load (or after a cache-flush event) you may see an error page:

Please consult the [Troubleshooting](../../troubleshooting) section for help regarding specific issues.

#### Kunena Updates

##### Automatic Updates

The preferred method for updating Kunena is to use the **joomla extention updater**. All you need to do then is navigate to the update manager, and select the kunena update, and clicking on update.

Full information can be found in the [Kunena Updates](../../advanced/Kunena-gpm).

>>>> It's important to backup first before doing the update.
