---
title: 'Translating Kunena'
---

Our official language pack can be found in our [download page](http://www.kunena.org/download). Please read also [Language Installation Guide](../../languages/Language Installation).

### Translating Kunena

#### Use Transifex
 
**Kunena project** uses [Transifex](https://www.transifex.com/Kunena-Forum/) to maintain all available translations. Transifex provides easy to use online tools, which can be used to update translations easily and without any technical knowledge. Alternatively Transifex allows you to download the current translation and update it with your favourite tool. It also allows anyone to download the most current version of any translated file.

Downloaded files can be manually installed to your Joomla site. Please read [Language files](../../languages/language-files) for more information.

Having your language in Transifex is the only way to get it into **Kunena** distribution. For information how to use transifex read the wiki article about [Transifex](../../languages/transifex).

**_ There are some bugs in Transifex_** Joomla support, so please check these:
* **_NEVER use double quotes (")_** in your translation; use single quotes instead (also in HTML tags)
* If you edit files by hand, make sure that it uses **_Unix encoding_** (`\n`), **_not_** Windows (`\r\n`) or Mac (`\r`) before uploading the files back to Transifex.

#### Create language pack for your language

To create installable language file, you just have to follow these steps:
+ Get the latest [core language files](https://www.transifex.com/Kunena-Forum/) from Transifex if you don't have them
+ Download latest [Kunena language pack](http://www.kunena.org/download)
+ Take your language from the language pack
+ Extract the language files to separate folders (you can call them admin & site)
+ Copy updated files to the above folders and rename them to replace the original files
+ Create ZIP archive (please use the same name as we did)
+ Install ZIP file with the Joomla! installer and make sure that your translation works
+ Publish your translation.
 - Use the [Forum](http://www.kunena.com/forum/107-translations)
 - **_Having your language in Transifex is the only way to get it into Kunena distribution_**

#### What is allowed in .ini files

**_The translated string has to be encosed by double quotes:_**
COM_KUNENA_A_TEMPLATE_MANAGER_COULD_NOT_WRITABLE="Could not make the template parameter file writable"

**_Do not split translations into multiple lines (only first line will show up):_**
COM_KUNENA_A_TEMPLATE_MANAGER_COULD_NOT_WRITABLE="Could not make the
template parameter file writable"

**If you want a new line, write:**
`<br />`
For example:
COM_KUNENA_A_TEMPLATE_MANAGER_COULD_NOT_WRITABLE="Could not make the** `<br />` **template parameter file writable"

**_Make your translations to be valid XHTML_**
**Not** `<br>`, **not** `<br/>` - only `<br />` is valid.
If unsure, please use the same markup as we do.
**_Files must be saved in UTF-8_**
**_Please do not use Double Quotes (") in your translation, it will break the translation._**