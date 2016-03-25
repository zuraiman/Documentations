---
title: 'Install Languages'
published: true
process:
    markdown: true
child_type: default
routable: true
cache_enable: true
visible: true
---

The **Kunena** installation package contains support only for English language forums but other languages may be separately downloaded and installed.  This guide shows you how to install other languages.
When you upgrade from one version to a different version you should also remember that you will need to separately download and upgrade all other languages you may be using on your site.

The Kunena installation package contains support only for English language forums but other languages may be separately downloaded and installed. Translating Kunena is managed as part of the [Transifex](https://www.transifex.com/Kunena-Forum/) project. The [download page](http://www.kunena.org/download) contains the additional languages pack, which includes all translated languages, both **_complete_** and **_incomplete_**.

### Language Packs for Kunena

#### Official language pack

Our official language pack can be found in our [download page](http://www.kunena.org/download). Some languages may have been fully translated but they are included anyway. Incomplete translations may result in untranslated strings appearing as `COM_KUNENA_THIS_IS_THE_KEY`. So if you start seeing strings like this, your translation isn't up to date and **Kunena** is using the last-known translation that you have installed on your site. 

### Installation procedure

Install the language pack with the Joomla! installer. All the available languages will be updated during the installation process. If you add more languages into your site, you need to install the language pack again to include missing languages.

* Make sure that your site is using your language:  go to **_Extensions -> Language(s)_** - click the **_Install Language_** icon and search for "Your lanuage"; select it and click the install button.
* Go to **_Extensions -> Language(s)_**: Your language should now be in the list - select it and make it your default language.
* Download the **Kunena** language pack from the site [download page](http://www.kunena.org/download).
* **_Extensions -> Manage -> Upload Package File_** to upload and install the .zip file.
* The language pack installed only languages, which are installed in Joomla already.

#### Not everything may be translated

Translated Kunena showing untranslated menu. You will notice that, although the forum is translated into your language, the menu at the top of the page is not translated. This may or may not occur in your particular site but it is easy enough to translate the menu items by going to the Joomla **_Menus_**, select the menu **_Kunena Menu_** and translate each item manually, one by one.

#### Helping with the task of completing the translation

Many of the languages in this package are missing translations. If you think you can complete the remaining parts of a translation, or you could write a translation that has not yet been written for Kunena, the Kunena translation team invites you to participate in the [Transifex](../../languages/transifex) project. If you have the skills and you would like to help, please look at the [Transifex](../../languages/transifex) article to see how you can help us with our translation work.