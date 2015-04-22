---
title: Requirements
taxonomy:
    category: docs
---

Kunena has intentionally been designed with few requirements.  You can easily run Kunena on your local computer, as well as 99% of all Web hosting providers. The following Kunena system requirements are:

1. Webserver (Apache, Nginx, LiteSpeed, IIS, etc.)
2. PHP 5.3.1 or higher (>= 5.6.8 recommended)
3. MySQL 5.1 or higher (>= 5.5 recommended)
4. Joomla! 3.4.1 or greater (>= 3.4.1 recommended)

>>> Our installer will check for minimal version requirements and will abort the install if they are not met.

## Web Servers

Even though technically you do not need a standalone Web server, it is better to run one, even for local development. Luckily there are many options depending on your platform:

### Mac

* OS X 10.9 Mavericks already ships with the Apache Web server and PHP 5.4, so job done!
* [MAMP/MAMP Pro](http://mamp.info) comes with Apache, MySQL and of course PHP.  It is a great way to get more control over which version of PHP you are running, setting up virtual hosts, plus other useful features such as automatically handling dynamic DNS.

### Windows

* [XAMPP](https://www.apachefriends.org/index.html) provides Apache, PHP, and MySQL in one simple package
* [EasyPHP](http://www.easyphp.org/) provides a personal Web hosting package as well as a more powerful developer version
* [MAMP](http://mamp.info) is a long-time Mac favorite, but now available for Windows.
* [IIS with PHP](http://php.iis.net/) is a fast way to run PHP on Windows.

### Linux

* Many distributions of Linux already come with Apache and PHP built-in, if it's not built-in, then usually the distribution provides a package manager where you can install Apache and PHP without much hassle.  More advanced configurations should be investigated with the help of a good search engine.

>>> Kunena works best with PHP 5.5 or higher. For more speed and more secure.

### Apache Requirements

Even though most distributions of Apache usually come with everything needed, for the sake of completeness, here is a list required Apache modules:

* `mod_cache`
* `mod_expires`
* `mod_headers`
* `mod_rewrite`


### IIS Requirements

Although IIS is considered a webserver ready to 'run-out-of-box' there are some changes that need to be made.
To get **Kunena** to run on an IIS server you need to install **URL Rewrite.** This can be accomplished using **Microsoft Web Platform Installer** from within IIS. You can also install URL Rewrite by going to [iis.net](http://www.iis.net/downloads/microsoft/url-rewrite).

### PHP Requirements

Most hosting providers and even local LAMP setups have PHP pre-configured with everything you need for Kunena to run out of the box.  However, some windows setups, and even Linux distributions (I'm look at you Debian!) ship with a very minimal PHP compile. Therefore, you may need to install or enable these PHP modules:

* `gd` (a graphics library used to manipulate images)
* `curl` (client for URL handling used by GPM)
* `mbstring` (multibyte string support)

##### Optional Modules

* `apc` (PHP 5.4) or `apcu` (PHP 5.5+) for increased cache performance
* `opcache` (PHP 5.5+) for increased PHP performance
* `xcache` alternative to *apc*, not as fast, but still pretty good
* `xdebug` useful for debugging in development environment


### Permissions

For Kunena to function properly your webserver needs to have appropriate **file permissions** in order to write logs, caches, etc.

By default Kunena will install with `644` and `755` permissions for folders and files respectively. Most hosting providers have configurations that ensure the webserver running PHP, will create and modify files as your user account.  This means that Kunena runs **out-of-the-box** on the vast majority of hosting providers.

However, if you are running on a dedicated server, or even your local environment, you may need to adjust permissions to ensure you **user** and your **webserver** can modify files as needed.  There are a couple of approaches you can take.

1. In a **local development environment**, you can usually configure your webserver to run as your user.  This way the web server will always create and modify files as your user and you will never have issues.

2. Change the **group permissions** on all files and folders so that the webserver's group has write access to files and folders while keeping the standard permissions.  This requires some commands (note: adjust `www-data` to be the group your apache runs under (`www-data`, `apache`, `nobody`, etc):

```
chgrp -R www-data .
find . -type f | xargs chmod 664
find . -type d | xargs chmod 775
find . -type d | xargs +s
umask 0002
```
