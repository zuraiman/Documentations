---
title: Upgrade
---

### Preparation

The actual installation procedure takes less than two minutes on most sites.  **Kunena** is a Joomla component and it is installed like any other Joomla extension using the Joomla installer.

1. [Technical Requirements](../../basics/requirements)
2. [Read the release notes](../../troubleshooting) for the version of Kunena that you intend to install 
3. Make sure that you have properly implemented Joomla Search Engine Optimisation ([SEO](../../faq/seo)) 
4. What are the recommended file and directory permissions? 

>>>  Upgrading software is not something to be done impulsively.  It requires good planning and site preparation.  The key to a successful and trouble-free upgrade of **Kunena** depends on having a solid Joomla foundation upon which you can build a web-based discussion forum.  This solid foundation relies as much on your own understanding about how to install Joomla extensions as it does on having a dependable hosted environment.

### The difference between installing and upgrading Kunena

If you have never installed Kunena before then you should look at the article [Installation Guide](../../basics/installation). It is important to note that it is not necessary to uninstall Kunena in order to upgrade to a new version.

The upgrade process preserves your existing forum configuration, any categories you defined, moderator assignments, user data, topics, posts, etc. created with the previous installation of Kunena. The upgrade process may structurally alter the internal arrangement of the way that your forum was configured including the definition of categories, users, templates, emoticons, ranks, topics, posts, etc. If you customised or replaced any files that were installed by a previous version of Kunena then, as a general rule, you will lose those customisations. If you added your own files to those normally installed by Kunena, you will not lose those files.

### Reviewing your Joomla installation

More than ever, upgrading means that you need to carefully examine your Joomla installation because, unlike installing Kunena for the first time, most people already have many other Joomla extensions installed on their websites. For many people these other Joomla extensions - particularly if they are old and have not been updated for a long time - can cause problems when you upgrade Kunena. It is not true that Kunena causes these problems. Rather it is that Kunena uses new and updated core components of Joomla that are likely to cause other extensions to conflict with Kunena if they are not handled properly.

Many older installations - sites that have been running without any noticeable problems if you were using previous versions of Kunena - involve outdated and unsupported features that were added to make those other extensions work properly. In certain cases, many of these older Joomla extensions need to be updated, uninstalled or replaced with better alternatives so that you will avoid having problems when you upgrade Kunena. Some of these issues are referred to elsewhere in this Wiki.

You should be particularly cautious about keeping your existing site template. Use the time when you want to upgrade Kunena as an opportunity to "make over" your website; replace your site template with a version that was developed for the most recent versions of Joomla. Use the time to update software that integrates with Kunena, such as [Community Builder](http://www.joomlapolis.com/) or [JomSocial](http://www.jomsocial.com/), for example, if you are using these things.

The Kunena project team does not officially endorse any third-party SEF products. Some of these have been known to cause serious usability and performance issues. If you have questions about third-party SEF tools, ask the developers of those products if they are aware of compatibility issues with Kunena.

#### To summarise:

1. Make sure that you have updated Joomla to the latest version (see [http://www.joomla.org](http://www.joomla.org)).
2. Make sure that you have updated other Joomla extensions to their latest versions.
3. Make sure that you are using a Joomla site template that works with the Mootools 1.4 (or later versions of Mootools). If in doubt, contact the author of the Joomla template.
4. If you are using a third-party SEF product, verify that the product is not responsible for causing usability or performance issues by disabling it or uninstalling it as you see fit. In any case, interoperability problems between third-party SEF products is not within the scope of the Kunena project to resolve. These are matters that involve the developers of those products.
5. Test your upgrade on a test site first.

### From which previous Kunena versions can I upgrade?

The upgrade process can be done with any Kunena versions (K 1.0, K 1.5, K 1.6, K 2.0 or K 3.0) or any FireBoard versions (1.0.4+).

### Upgrading

#### Method 1: As easy as 1-2-3

Go to the [Kunena download page](http://www.kunena.org/download) and find the area that relates to Kunena. Download the package and install it by the Joomla installer. The installation procedure will then proceed automatically, without further user intervention, and will show an animated status bar.
When the installation is finished, install Kunena language pack (if you had previously installed it).

#### Method 2: Using Joomla autoupdate

>>>> It is possible that problems can occur using Joomla’s autoupdate feature and, when these problems occur, you will stop receiving reminders that there are new versions of Kunena available. Use the autoupdate feature at your own risk! Remember, it is your responsibility to make sure that you have made a backup of your website before you update software.

1. On the Joomla Control Panel, you will see that there is a update for Kunena.
2. Click Kunena Update Now!
3. Select Kunena and, optionally, Kunena Language Pack (if you had previously installed it).
4. Click Update
5. After a few seconds the Kunena upgrade process will continue automatically.