---
title: 'Language Files'
---

### Introduction

This article helps you to locate **Kunena** language files in your installation or GitHub tree. The language files contain the translations of many thousands of symbolic names used in Kunena. If you want to find a particular symbolic name (or translated text) we recommend that you use a search tool like [Wingrep](http://www.wingrep.com/) to find where the text string is defined.

Our recommendation is that people should not edit the original source code directly but, instead, define one's own custom overrides to change the value of symbolic names. To create a language override you should go to **_Extensions -> Language(s) -> Overrides -> New_** to define a new value for the symbolic name that you want to use instead of the one(s) that are defined as part of the standard installation. For further information about using Joomla langage overrides, see [Language Overrides in Joomla](http://docs.joomla.org/Language_Overrides_in_Joomla).

**Kunena** installation kits only install English. Other languages must be installed separately. Non-English translations can be obtained by going to the [download page](http://www.kunena.org/download). If you upgrade from older versions you will also need to update the non-English translations, separately.
If you want to translate **Kunena**, please read [Translating Kunena](../../languages/translating-kunena) and [Transifex](../../languages/transifex)) articles.

##### Kunena installs the following language files:

* `./administrator/components/com_kunena/language/en-GB/`
en-GB.com_kunena.controllers.ini
en-GB.com_kunena.ini
en-GB.com_kunena.install.ini
en-GB.com_kunena.libraries.ini
en-GB.com_kunena.models.ini
en-GB.com_kunena.sys.ini
en-GB.com_kunena.views.ini
en-GB.plg_finder_kunena.sys.ini
en-GB.plg_kunena_alphauserpoints.sys.ini
en-GB.plg_kunena_community.sys.ini
en-GB.plg_kunena_comprofiler.sys.ini
en-GB.plg_kunena_gravatar.sys.ini
en-GB.plg_kunena_joomla.sys.ini
en-GB.plg_kunena_kunena.sys.ini
en-GB.plg_kunena_uddeim.sys.ini
en-GB/en-GB.plg_quickicon_kunena.sys.ini
en-GB/en-GB.plg_system_kunena.sys.ini

* `./components/com_kunena/language/`
en-GB.com_kunena.controllers.ini
en-GB.com_kunena.ini
en-GB.com_kunena.models.ini
en-GB.com_kunena.templates.ini
en-GB.com_kunena.tpl_blue_eagle.ini
en-GB.com_kunena.views.ini
en-GB.kunena_tmpl_crypsis.ini
en-GB.mod_kunenamenu.ini
en-GB.mod_kunenamenu.sys.ini

All others languages have files inside the Joomla language directories:

 `./administrator/language/`
 `./language/`
 
 ##### Official language pack
 
The Kunena installation package contains support only for English language forums but other languages may be separately downloaded and installed. Translating Kunena is managed as part of the [Transifex](https://www.transifex.com/Kunena-Forum/) project. The [download page](http://www.kunena.org/download) contains the additional languages pack, which includes all translated languages, both **_complete_** and **_incomplete_**. The language pack installed only languages, which are installed in Joomla already.