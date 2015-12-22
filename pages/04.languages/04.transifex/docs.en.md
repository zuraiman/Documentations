---
title: '  Transifex'
---

###### _Transifex'' is a modern, open-source localisation platform. It’s a web system which automates the translation workflow for complex international projects._

### Translating Kunena

#### Register
You can register at (https://www.transifex.com/)

#### Kunena on Transifex
You can find the official translation page for **Kunena** under this URL: (https://www.transifex.com/Kunena-Forum/)

#### Joining a Transifex team
To manage the process of who is translating what, there are teams for each language: (https://www.transifex.com/Kunena-Forum/teams/).
Please create a new team for your language if there is no yet. Please use the five digit xx_XX language code instead of the two digit language code. Or request a membership to a specific language.

#### Doing the translation
Go back to the main page of the **Kunena** project page: (https://www.transifex.com/Kunena-Forum/). There you can see a list of the language files. To translate one of those just click on it. On the next side you can see some additional info and below is a list of the available languages. If your language is not listed, just click on **_add Translation_** and choose you language. If your language is available, you can click on it. Now you get a popup with some options. You can upload your local `.ini` file and **_Transifex_** will find the translations automatically or you can click on **_View strings online_**. When you press on **_Translate now_** you get a new view with all strings which are translated or should be translated. Just fill your translations into the text fields and press save. Your done with this file, go to the next.

For further information visit (http://docs.transifex.com/).

>>>> Please test that your language works in Joomla! before uploading the file into **_Transifex_**. Otherwise your translations may break during import!

**_There are some bugs in Transifex_** Joomla support, so please check these:
* **_NEVER use double quotes (")_** in your translation; use single quotes instead (also in HTML tags)
* If you edit files by hand, make sure that it uses **_Unix encoding_** before uploading the files back to Transifex.
* If you edit files by hand, make sure that you don't split the translations into more than one line (part of the translation disappears)

### Kunena Developer Info
Here I will shortly describe how you can setup the **_Transifex_** client to manage all translations.

#### Installation
##### Linux
The Linux package called `transifex-client` is included in the most distributions. 

##### Mac
##### Windows

#### Setup the client
It is really simple when you know what to do. I will show the way with clone from github!
* Clone Kunena or any module or plugin from github.
* Open a terminal/console and change directory to Kunena
* You can add your own language into `.tx/config` file (look below)
* `tx pull -l transifex language code` (see also) (http://docs.transifex.com/client/)

#### Add a new language

Because **_Transifex_** uses different language codes than Joomla! you should map your own language from **_Transifex_** to Joomla! format.

* Edit file called `.tx/config` and find language mapping rules inside [main] section:
**[main]**
host = (https://www.transifex.com)
lang_map = **ar:ar-AA, ca_ES:ca-ES, cs_CZ: cs-CZ ,da_DK:da-DK, de_DE:de-DE, [...] zh_TW:zh-TW**
* Now add rule for your own language; line breaks are not allowed for the variable!