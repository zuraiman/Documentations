---
title: 'Improving Performance'
---

### Improving Kunena performance

### Introduction

Is your forum running too slow for your taste? Or does it load relatively fast until the busiest time of the day?
This article will help you optimise both your server and your site so that it will be able to handle the load without having to buy a more powerful server.
As a general guide, you should also familiarise yourself with the [technical requirements](../../basics/requirements) for the version of **Kunena** that you may be using.

### Performance considerations:  why Kunena may run slower on your site

Normally most **Kunena** pages should load in less than a second or two. On a well-optimised server **Kunena** can show **Time to create page** to be less than 0.6 seconds. 

If your site runs slower than this, there are a few things you can do to improve performance. Here is a list of a few potential causes for the slowness:

* You have a lot of Joomla plugins installed on your system
* You have a lot of modules on your **Kunena** pages
* You are integrating **Kunena** with other components
* Your template is very complicated and has many cool features
* You're not using Joomla caching
* Your Apache settings are unoptimised
* Your MySQL settings are unoptimised
* Images, CSS and JavaScript files aren't cached in browsers
* Sometimes JavaScript issues may cause major slowdown in the browser

All of these issues have different symptoms which can be detected.

#### If your site is always too slow

The easiest way to check if your server is fast enough to run Joomla/**Kunena** is to load your front page (or any other page) after having logged in. If all page loads are slow (over 1-2 seconds for Joomla and over 3 seconds for **Kunena**) when there are no users in your site (at 3 o'clock in the morning, for example), you're often out of luck: you have bought a server plan which is inadequate and is really not meant to be used for dynamic and busy sites like a forum. Here are my recommendations for a minimum hosting plan for **Kunena**:

Small forums (10k posts, 1k users):
* 1024 MB of RAM guaranteed
* 1 CPU @ 667 MHz (or 1/4 CPU @ 2.67MHz) guaranteed
* Fast hard drive (min RPM 7.2K, preferably 15K or SSD)

Large forums (100-200k posts, 10k users):
* 4096 MB of RAM guaranteed
* 2 CPUs @ 2.66 Ghz guaranteed
* Fast hard drive (min RPM 15K or SSD)

The above numbers are just rough estimates; the actual requirements depend on your site's content and how many active (or concurrent) users you have on your site at any particular time.

Guaranteed CPU time is needed because that's the only thing that will ensure your site gets loaded even if the server is busy. Often even the best servers cannot handle more than 20 Joomla users loading a page at the same moment.

#### If your site is slow at peak times

If your site runs relatively fast most of the time, but has some major slowdowns when there are a lot of active users on your site, your server is most likely running out of CPU, memory or I/O. 

As long as your server can handle the load, everything runs relatively smooth. But if any of the resources run out, you will get 30-180 second page loads within just a few minutes. This effect is called saturation (you might like to think of it in terms of flooding rivers and sewer systems: if there's too much rain, large areas get flooded in a very short time or, even worse, the flood can stay for days or weeks!)

Running out of resources doesn't always mean that you need to buy a more powerful server. Often servers are not well optimised for Joomla/**Kunena** sites and there might be some tasks you would like to do in Joomla to make it lighter. The next sections will give you a few hints how to improve the performance.

### Optimising Joomla

Having less is faster. In many cases Joomla sites have many modules and plug-ins which are loaded but not really needed or used on the site. Having all of that costs memory and CPU time, sometimes more than you would expect. Even if the difference is small, following a few simple guidelines can make all the difference at peak times, when the most users are online.

#### Remove unused plugins

The first thing you should do is review the plugins that you've installed and/or enabled on your website. This is particularly important for Joomla! 1.5 sites because every loaded plug-in decreases the overall site performance and contributes to slowing down the system. The effect is smaller in Joomla! 1.7, but if you have a lot of system, user or content plug-ins (or you have **JomSocial** or **Community Builder** on your site), all of those must still be loaded and initialised, which adds to memory requirements and can contribute to performance degradation.

Just be careful not to disable or uninstall plug-ins that are needed for other components.

#### Remove extra modules

It's a good idea not to load too many extra modules in the **Kunena** pages. The main reason is that Kunena templates have a lot of information in them and it's better to give Kunena all the width it needs (e. g. all the left and right module positions).

There is also another reason to remove modules: some modules display content from other components or they are making a lot of database queries. Loading content from other components usually means extra CPU and memory usage, but the database queries are those which can bring your server down.

In Joomla there is an easy way to evaluate module performance. Just enable Joomla Debug Mode and reload the page. At the bottom of the page there's a summary that looks like this:

  Profile Information
  Application afterLoad: 0.000 seconds, 0.89 MB
  Application afterInitialise: 0.106 seconds, 4.74 MB
  Application afterRoute: 0.113 seconds, 5.49 MB
  Application afterDispatch: 1.319 seconds, 19.99 MB
  Application afterRender: **1.479 seconds**, **23.20 MB**
  
  Memory Usage
  24464304
  
  **21 queries logged**

The most important information has been highlighted in the above example. They are _time used, memory usage_ and _number of queries_. You should reload the page a few times to get more reliable numbers and try again without the module. If the numbers are noticeably smaller without that module, it's a good idea to remove it from all the forum pages.

**NOTE:** You must remove modules from all **Kunena** menu items, otherwise the modules will appear when you enter to some other page.

#### Optimise Kunena configuration

**Kunena** has a few configuration options which slow down your system. Some of them are enabled by default, because they are useful for most sites. But if you don't need those features, they can be disabled to make the forum load faster.

##### General / Basic Settings

* **Enable Debug Mode = No** If you're not debugging the system, this option should always be disabled. Using it decreases site performance more than 35% for nothing!

##### Frontend / Look And Feel

* **Topics Per Page** Smaller value makes topic lists faster (going from 40 to 20 = +20% performance gain, going from 20 to 10 = +15% performance gain).
* **Messages Per Page** Smaller value makes messages load faster (going from 24 to 12 = +25% performance gain, going from 12 to 6 = +15% performance gain).
* **Show Avatar on Categoriy Index and Recent Topics = No** means 5% faster page loads compared to **Yes**.

##### Extra / Statistics Settings

* **Show Who is Online = No** can make your site faster if you have a lot of users online.

#### Prefer simple Joomla templates

It may be cool to have the fanciest-looking Joomla template in your site, but complexity has a major drawback: it can make your site feel slow.  There may be other issues, too (see also [[My Joomla site template makes a mess of Kunena]]).

You can have the fastest and most optimised server in the world, but it doesn't matter much if it takes 3 seconds for your favorite browser to render all the cool features on the page. There is a tool called [YSlow](https://addons.mozilla.org/en-US/firefox/addon/yslow/) which allows you to benchmark your site.

#### Use Joomla caching

Enabling Joomla caching can make your forum load faster, especially if you have modules which take advantage of it.
Kunena Latest Module gains a huge performance improvement if cached.
**AVOID USING** System - Cache plug-in in your forum as it doesn't work well with dynamic content, especially if you allow guests to post.

### Server Optimisation

Most servers are sold with default Apache/PHP/MySQL settings, which are not ideal if you're running a dynamic site like Joomla. In addition Kunena has some special needs from the MySQL server because of the large amount of data in the database.

#### Cache static files in browser

A relatively large portion of the page load time is tied up in downloading images, stylesheets, scripts, flash, etc. Reducing the number of components in reduces the number of HTTP requests required to render the page. This is the key to faster pages.

Administrators often have limited tools to reduce the number of loaded components on the first page load, but once the files have been loaded into a browser's cache, there's no point making repeated requests for files that are unlikely to change. If these requests can be eliminated, page loads are much faster as the client doesn't have to wait for an answer if the files have not been modified.

This can be done by adding following lines in your Apache `.htaccess` file (also remember to check if mod_expires is enabled):

 * By default cache all files for one day
   ExpiresDefault "access plus 1 day"
 
 * Your document html
   ExpiresByType text/html "access plus 0 seconds"
 
 * Data
   ExpiresByType text/xml "access plus 0 seconds"
   ExpiresByType application/xml "access plus 0 seconds"
   ExpiresByType application/json "access plus 0 seconds"
 
 * Feed
   ExpiresByType application/rss+xml "access plus 5 minutes"
   ExpiresByType application/atom+xml "access plus 5 minutes"
 
 * Favicon (cannot be renamed)
   ExpiresByType image/x-icon "access plus 1 day"
 
 * Media: images, video, audio
   ExpiresByType image/gif "access plus 12 hours"
   ExpiresByType image/png "access plus 12 hours"
   ExpiresByType image/jpg "access plus 12 hours"
   ExpiresByType image/jpeg "access plus 12 hours"
 
 * HTC files (css3pie etc)
   ExpiresByType text/x-component "access plus 1 week"
 
 * Webfonts
   ExpiresByType application/x-font-ttf "access plus 1 week"
   ExpiresByType font/opentype "access plus 1 week"
   ExpiresByType application/x-font-woff "access plus 1 week"
   ExpiresByType image/svg+xml "access plus 1 week"
   ExpiresByType application/vnd.ms-fontobject "access plus 1 week"
 
 * CSS and JavaScript
   ExpiresByType text/css "access plus 1 day"
   ExpiresByType application/javascript "access plus 1 day"

The contents are tuned for Joomla and Kunena (installing a new version may cause wrong images to be used for 12 hours, css for 24 hours) unless the user reloads the page.

#### Apache

##### DNS lookup

You should disable the '''HostnameLookups''' directive to reduce latency on page loads so the server doesn't need to make extra requests to DNS servers before it can serve the page.

##### MaxClients

**MaxClients** sets the limit on maximum simultaneous requests that can be handled by the server. This limits the number of child processes that get spawned. Do not set too low such that new connections are put in queue, as those will eventually time-out and the server resources will be left unused. If you set this too high, it will cause the server to start swapping and the response time will degrade drastically. An appropriate value for MaxClients can be calculated as: MaxClients = Total RAM dedicated to Apache / Max child process size. For dynamic content such as PHP, it may be around 15-30M.

##### KeepAlive

The **KeepAlive** directive allows multiple requests to be sent over the same TCP connection. This is particularly useful for serving HTML pages with lots of images. If KeepAlive is set to Off, then for each images, a separate TCP connection has to be made. Overhead due to establishing TCP connections can be eliminated by turning On KeepAlive.

**KeepAliveTimeout** determines how long to wait for the next request. You should always use a value between 2-5 seconds. If the value is set too high, child processes are tied up waiting for the client when they could be used for serving new clients.

By default **KeepAliveTimeout** is almost always too high (15-30 seconds) and that's the most likely cause if your page loads slow down to 30-75 seconds on heavy load.

More information can be found at [Configuring Apache for Maximum Performance](http://www.howtoforge.com/configuring_apache_for_maximum_performance) and [Apache Performance Tuning](http://httpd.apache.org/docs/2.0/misc/perf-tuning.html).

#### MySQL

MySQL settings are typically not very well optimised for Kunena. 
Here is modified part of a **my.cnf** file (optimised for 2 CPUs / 4 threads, >4GB RAM, 350MB database):

 default_table_type      = InnoDB
 key_buffer              = 24M
 join_buffer_size        = 2M
 max_heap_table_size     = 128M
 max_allowed_packet      = 16M
 thread_stack            = 128K
 thread_cache_size       = 10
 
 max_connections needs to be 2-3x larger than MaxClients in Apache
 max_connections         = 300
 table_cache             = 4096
 
 thread_concurrency = 2x number of concurrent threads
 thread_concurrency      = 8
 query_cache_limit       = 1M
 
 Next 3 settings allows queries to be cached
 query_cache_size        = 96M
 query_cache_min_res_unit= 2K
 query_cache_type        = 1
 
 innodb_buffer_pool_size should be larger than your database size (if you have enough memory)
 innodb_buffer_pool_size = 384M

With these settings MySQL uses at most 1GB of RAM and loads the whole database into memory. InnoDB is used because it allows this, which makes the site to run much faster as everything is loaded into the memory and no I/O (disk access) is needed.

PS: remember to change all Kunena tables to use InnoDB, otherwise you don't benefit from these changes. You can do that easily from phpMyAdmin.

#### PHP

Most of the CPU usage on your server is spent inside Apache processes that run the PHP interpreter (or Joomla). There are ways to make PHP more efficient in both CPU and memory usage.

##### Use PHP opcode compiler

Caching compiled PHP scripts can save you a lot of time and server load. PHP extensions exists to make this easy for you; look for PHP cache solutions like APC, eAccelerator and xCache. These will cache PHP scripts in their compiled state so the same script will not have to be executed repeatedly for each client.

**Tip:** If you experience random white screens or your Apache server starts to die, you're hitting bugs in your PHP opcode compiler. If this happens to you, it may be safer to turn off PHP opcode caching (you can still keep using it in your Joomla cache).}}

##### Optimise your memory limit

While both Joomla and Kunena recommends you to use **memory_limit=64M**, try to minimise the value to save some resources and avoid memory leaks from wasting your memory. You can see the amount of used memory in each page by enabling Joomla Debug Mode.

Lowering the value is possible if you have minimised the number of the modules and plugins on your site. Just remember that integrating Kunena with other components and uploading large images also costs some memory, so be careful not to set the limit too low. If memory runs out, the page fails to load and you end up having either a blank page or an error message.
