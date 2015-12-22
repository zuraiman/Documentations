---
title: SEO
---

### Introduction

Among other things, Search Engine Optimization is a Joomla! feature that permits the translation of [URLs](http://en.wikipedia.org/wiki/URL) into a more readable form for use with [search engine spiders](http://en.wikipedia.org/wiki/Search_engine_spider). To work with this feature click on **Global Configuration** in the backend Control panel. These more readable [URLs](http://en.wikipedia.org/wiki/URL) are sometimes called Search Engine Friendly (SEF) URLs. This article will show you how to use Joomla's built-in SEO features to generate SEF URLs.

### Implementing Joomla SEO

There are **three** things you must do:
1) _Search Engine Friendly URLs_:  When set to Yes, URLs are rewritten to be more friendly for search engine spiders. For example, the URL: `www.example.com/index2.php?option=com_content&view=etc...`, would turn into: `www.example.com/alias`. Most of the items created in Joomla! have an Alias box where a search engine friendly URL can be inserted. 
2) _Use URL Rewriting_: When set to Yes, Joomla! will use the _mod_rewrite_' settings of Apache when creating search engine friendly URLs. Please note: it is advised that you do not modify any `.htaccess` file without an understanding of how it works.
3) You must use the `.htaccess` file provided with Joomla! in order to use this setting.  To use this file, rename the `htaccess.txt` file (found in the root directory) to `.htaccess`.

[Claims](http://www.joomlaseo.com/) exist that it's possible to implement search engine-friendly (SEF) URLs without having to, correspondingly, use the Apache _mod_rewrite_ setting. These claims may be factual but they are not sufficiently substantiated to provide any guarantee. What is more often the case is that if people only click one option, or do not have a properly written `.htaccess` file, SEF URLs will not be generated and **Kunena** will not function correctly.
In some cases it may be necessary to implement a special case of the Apache server [.htaccess file](http://en.wikipedia.org/wiki/Htaccess) in order for you to make SEO operate. Joomla includes a template for this file, which is located in the root directory of your Joomla website; the file is named `htaccess.txt`; If you are experiencing problems in getting SEF URLs to operate, you should rename the file as `.htaccess` (do not forget the leading "." character). In exceptional cases, other changes to the `.htaccess` file may be necessary - see [.htaccess tutorial](http://www.javascriptkit.com/howto/htaccess.shtml).

##### Every Joomla component must have a menu item for it

If you want to implement SEF URLs on any Joomla website, you must have a menu item associated with the component. The menu item does not have to be displayed on your website but it must exist and it must be enabled (published).

#### SEO and Kunena

**Kunena** is fully compatible with the Joomla! SEO. It is recommended that the following SEO values be used (assuming that your website supports the use of SEO and any dependencies on `.htaccess` settings):

**Global Configuration -> (tab) Site -> SEO Settings -> Search Engine Friendly URLs: = Yes**
**Global Configuration -> (tab) Site -> SEO Settings -> Use URL Rewriting: = Yes**

>>>>> Do not forget to rename `htaccess.txt` to `.htaccess`! Use a different `.htaccess` file for servers that are not running Apache webserver software.

##### Kunena Configuration

**Dashboard -> Configuration -> General -> Seo Settings -> Search Engine Friendly URLs = Yes** (default = Yes)
This setting works only in conjunction with Joomla SEO.