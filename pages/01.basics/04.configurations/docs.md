---
title: Configurations
taxonomy:
    category: docs
---


The Kunena Configuration feature allows users to tailor Kunena's functions to their specific site needs.  This feature allows, for example, users to decide what they will call their forum page, whether forum messages can be posted by anonymous users or only by registered users of the site, and whether other third-party components (like [[:Wikipedia:Private Messaging|private messaging]]) are to be used.  Many of the choices can be made according to individual tastes; some, however, may cause unexpected consequences if they're not handled correctly.

As a general guide, the default settings that ship with Kunena's installation kit will be adequate for most purposes.  However, some suggested tips are offered in the article [[Configuration Tips]]

#### Basics
This article describes how to change the Kunena configuration parameters.

##### Accessing the Kunena Configuration feature
[[Image:configTools.jpg|left|Ranks Management Menu]] Go to the [[Beginners#Kunena_Backend|Kunena Backend]] and select the Kunena Configuration feature.

##### Configuration Menu
There are two basic functions:  Settings (see below) can be changed; before they can be effective they must be saved.

===[[Image:functionSave.gif‎|left|Save]]Save function===

Any changes become effective by pressing the '''Save''' button located at the top right of the page.

===[[Image:functionBack.gif|left|Back]]Back function===

The back button returns you to the Kunena [[Control Panel]].

#### List of settings
The settings are arranged in the groupings listed below.  The ''default/initial values'' are settings that are supplied with a clean installation of Kunena.  If a previously-installed version of Kunena or Fireboard had been installed on the user's site, the old values will be preserved.<br>

{{vrs|1.0}}New versions of Kunena may add or remove items in the list below.  Please check your version of Kunena.

==Basics==
===Basic Settings===
=====[[Board Title]]=====
''Initial/default value:''  Kunena
=====[[Board E-mail Address]]=====
''Initial/default value:''  change@me.com
=====[[Forum Offline]]=====
''Initial/default value:''  No
=====[[Board Time Offset]]=====
''Initial/default value:''  0
=====[[Session Lifetime]]=====
''Initial/default value:''  1800
=====[[Forum Offline Message]]=====
''Initial/default value:''  &lt;h2&gt;The Forum is currently offline for maintenance.&lt;/h2&gt; Check back soon!
=====[[Enable RSS feed]]=====
''Initial/default value:''  Yes
=====[[Default RSS type]]=====
''Initial/default value:''  By Thread
=====[[RSS History]]=====
''Initial/default value:''  1 Month
=====[[Enable PDF creation]]=====
''Initial/default value:''  Yes
{{vrs|1.5.8}}===SEO Settings===
=====[[Search Engine Friendly URLs]]=====
''Initial/default value:''  Yes
=====[[Do Not Use Category IDs]]=====
''Initial/default value:''  No
=====[[Enable UTF8 Support]]=====
''Initial/default value:''  No

==Frontend==
===Look and Feel===
=====[[Threads Per Page]]=====
''Initial/default value:''  20
=====[[Messages per page]]=====
''Initial/default value:''  6
=====[[Search Results]]=====
''Initial/default value:''  15
=====[[Show History]]=====
''Initial/default value:''  Yes
=====[[History Limit]]=====
''Initial/default value:''  6
=====[[Show New posts]]=====
''Initial/default value:''  Yes
=====[["New" indicator]]=====
''Initial/default value:''  NEW!
{{vrs|1.0}}=====Joomla Mambot Support=====
This setting is a legacy from Fireboard and has no use in Kunena 1.0.x
''Initial/default value:''  Yes
=====[[Disable emoticons]]=====
''Initial/default value:''  No
=====[[Template]]=====
''Initial/default value:''  default_ex
=====[[Image Sets]]=====
''Initial/default value:''  default_ex
=====[[Default Kunena Page]]=====
''Initial/default value:''  Recent Discussions
=====[[Use Joomla Style?]]=====
''Initial/default value:''  No
=====[[Show Announcement]]=====
''Initial/default value:''  Yes
{{vrs|1.5.10}}===== Show Avatar on Categories list?=====
This option does not feature in K 1.5.10 because it was replaced by a new and extended option.  See next item.<br>
''Initial/default value:''  No
{{vrs|1.5.10}}=====[[Show avatars in Category view, Recent Discussions and My Discussions?]]=====
''Initial/default value:''  Hide

=====[[Category Image Path]]=====
''Initial/default value:''  category_images/
=====[[Number of child board columns]]=====
''Initial/default value:''  0
=====[[Show Child Category Image]]=====
''Initial/default value:''  Yes
=====[[Announcement Moderator IDs]]=====
''Initial/default value:''  62
=====[[Textarea Width]]=====
''Initial/default value:''  450
=====[[Textarea Height]]=====
''Initial/default value:''  300
=====[[Enable Rules Page]]=====
''Initial/default value:''  Yes
=====[[Show rules in Kunena]]=====
''Initial/default value:''  Yes
=====[[Rules Content ID]]=====
''Initial/default value:''  1
=====[[Rules external page link]]=====
''Initial/default value:''  http://www.kunena.com/
=====[[Enable Help Page]]=====
''Initial/default value:''  Yes
=====[[Show help in Kunena]]=====
''Initial/default value:''  Yes
=====[[Help Content ID]]=====
''Initial/default value:''  1
=====[[Help external page link]]=====
''Initial/default value:''  http://www.kunena.com/
=====[[Enable Forum Jump]]=====
''Initial/default value:''  Yes
=====[[Message Reporting]]=====
''Initial/default value:''  Yes

===User Related===
=====[[Username]]=====
''Initial/default value:''  Yes
=====[[Require E-mail]]=====
''Initial/default value:''  No
=====[[Show E-mail]]=====
''Initial/default value:''  No
=====[[Show User Stats]]=====
''Initial/default value:''  Yes
=====[[Use Posts Statistics Bar]]=====
''Initial/default value:''  Yes
=====[[Color number for Stats Bar]]=====
''Initial/default value:''  9
=====[[Show Karma indicator]]=====
''Initial/default value:''  Yes
=====[[User Edits]]=====
''Initial/default value:''  Yes
=====[[User Edit Time]]=====
''Initial/default value:''  0
=====[[User Edit Grace Time]]=====
''Initial/default value:''  600
=====[[Show Edited Mark Up]]=====
''Initial/default value:''  Yes
=====[[Allow Subscriptions]]=====
''Initial/default value:''  Yes
=====[[Post-subscription checked by default?]]=====
''Initial/default value:''  Yes
=====[[Allow Favorites]]=====
''Initial/default value:''  Yes

===Various Length Settings===
=====[[Wrap Words Longer Than]]=====
''Initial/default value:''  250
=====[[Max. Subject length]]=====
''Initial/default value:''  50
=====[[Max. Signature Length]]=====
''Initial/default value:''  300

==Security==
===Security Settings===
=====[[Registered Users Only]]=====
''Initial/default value:''  No
=====[[Allow Name Change]]=====
''Initial/default value:''  No
=====[[Public Read/Write]]=====
''Initial/default value:''  No
=====[[Flood Protection]]=====
''Initial/default value:''  0
=====[[E-mail Moderators]]=====
''Initial/default value:''  No
=====[[E-mail Administrators]]=====
''Initial/default value:''  No
=====[[Spam protection system]]=====
''Initial/default value:''  No
=====[[Include complete post content in the e-mail sent to subscribers]]=====
''Initial/default value:''  Yes
{{vrs|1.5.10}}
=====[[Hide the IP in messages from moderators]]=====
''Initial/default value:''  Yes

==Avatars==
===Avatar Settings===
=====[[Allow Avatars]]=====
''Initial/default value:''  Yes
=====[[Allow Avatar Upload]]=====
''Initial/default value:''  Yes
=====[[Use Avatar Gallery]]=====
''Initial/default value:''  Yes
=====[[Image Processor]]=====
''Initial/default value:''  GD2
=====[[Small Image Height]]=====
''Initial/default value:''  50
=====[[Small Image Width]]=====
''Initial/default value:''  50
=====[[Medium Image Height]]=====
''Initial/default value:''  100
=====[[Medium Image Width]]=====
''Initial/default value:''  100
=====[[Large Image Height]]=====
''Initial/default value:''  250
=====[[Large Image Width]]=====
''Initial/default value:''  250
=====[[Max. Avatar Filesize]] ''in Kbytes''=====
''Initial/default value:''  2048
=====[[Avatar Quality]] (%)
''Initial/default value:''  65

==Uploads==
===Images===
=====[[Allow Public Upload for Images]]=====
''Initial/default value:''  No
=====[[Allow Registered Upload for Images]]=====
''Initial/default value:''  Yes
{{vrs|1.5.12}}
=====[[Visibility of images for guests]]=====
''Initial/default value:''  Hide
=====[[Max. Image Height]]=====
''Initial/default value:''  800
=====[[Max. Image Width]]=====
''Initial/default value:''  800
=====[[Max. Image Filesize]] ''in Kbytes''=====
''Initial/default value:''  150

===Files===
=====[[Allow File Upload for Public]]=====
''Initial/default value:''  No
=====[[Allow File Upload for Registered]]=====
''Initial/default value:''  Yes
{{vrs|1.5.12}}
=====[[Visibility of attachments for guests]]=====
''Initial/default value:''  Hide
=====[[File types allowed]]=====
''Initial/default value:''  zip,txt,doc,gz,tgz
=====[[Max. File size]] ''in Kbytes''=====
''Initial/default value:''  120

==Ranking==
===Ranking Settings===
=====[[Ranking]]=====
''Initial/default value:''  Yes
=====[[Use Rank Images]]=====
''Initial/default value:''  Yes

==BBcode==
===BBcode Settings===
=====[[Show spoiler tag in editor toolbar]]=====
''Initial/default value:''  Yes
=====[[Show video tag in editor toolbar]]=====
''Initial/default value:''  Yes
=====[[Show eBay tag in editor toolbar]]=====
''Initial/default value:''  Yes
=====[[eBay widget language code]]=====
''Initial/default value:''  en-us
=====[[Trim long URLs]]=====
''Initial/default value:''  Yes
=====[[Front portion of trimmed URLs]]=====
''Initial/default value:''  40
=====[[Back portion of trimmed URLs]]=====
''Initial/default value:''  20
=====[[Auto embed YouTube videos]]=====
''Initial/default value:''  Yes
=====[[Auto embed eBay items]]=====
''Initial/default value:''  Yes
=====[[Enable Code Highlighting]]=====
''Initial/default value:''  No

==Integration==
Changes to these settings are dependent upon the installation of other third-party components.
===Avatar Integration===
=====[[Use avatar picture from]]=====
''Initial/default value:''  Kunena

===Profile Settings===
=====[[Profile]]=====
''Initial/default value:''  Kunena

===Private Messaging Component===
=====[[Enable private messaging]]=====
''Initial/default value:''  No

{{vrs|1.5.7}}===Alpha User Points===
=====[[Enable Points in profile]]=====
''Initial/default value:''  No
=====[[Enabled Rules for points]]=====
''Initial/default value:''  No
=====[[Minimum characters on reply]]=====
''Initial/default value:''  0

{{vrs|1.0}}{{vrs|1.5.7}}===Bad Words filtering===
This setting is a legacy from Fireboard and has no use in Kunena 1.0.x. This option does not feature from V 1.5.7
=====Use Bad Word Filtering
''Initial/default value:''  No

===Discussbot===
=====[[Enable the Discuss Bot]]=====
''Initial/default value:''  No

{{vrs|1.5.10}}===Enable the JomSocial Activity Stream Integration===
=====[[Enable the JomSocial Activity Stream Integration]]=====
''Initial/default value:''  No


==Plugins==
===Userlist===
{{vrs|1.5.12}}
=====[[Enable the userlist]]=====
''Initial/default value:''  Yes
{{vrs|1.5.12}}
=====[[Number of userlist rows]]=====
''Initial/default value:''  30
=====[[Online Status]]=====
''Initial/default value:''  Yes
=====[[Display Avatar]]=====
''Initial/default value:''  Yes
=====[[Show Real Name]]=====
''Initial/default value:''  Yes
=====[[Show Username]]=====
''Initial/default value:''  Yes
{{vrs|1.5.10}}=====Show User Group=====
This option does not feature from V 1.5.10
''Initial/default value:''  No
=====[[Show Number of Posts]]=====
''Initial/default value:''  Yes
=====[[Show Karma]]=====
''Initial/default value:''  Yes
=====[[Show E-mail]]=====
''Initial/default value:''  No
=====[[Show User Type]]=====
''Initial/default value:''  No
=====[[Show Join Date]]=====
''Initial/default value:''  Yes
=====[[Show Last Visit Date]]=====
''Initial/default value:''  Yes
=====[[Show Profile Hits]]=====
''Initial/default value:''  Yes

===Recent Post Settings===
=====[[Show Recent Posts]]=====
''Initial/default value:''  Yes
=====[[Number of Recent Posts]]=====
''Initial/default value:''  10
=====[[Count Per Tab]]=====
''Initial/default value:''  5
=====[[Show Category]]=====
''Initial/default value:''
=====[[Show Single Subject]]=====
''Initial/default value:''  Yes
=====[[Show Reply Subject]]=====
''Initial/default value:''  Yes
=====[[Subject Length]]=====
''Initial/default value:''  100
=====[[Show Date]]=====
''Initial/default value:''  Yes
=====[[Show Hits]]=====
''Initial/default value:''  Yes
=====[[Show Author]]=====
''Initial/default value:''  1

===Stats Plugin Settings===
=====[[Show Stats]]=====
''Initial/default value:''  Yes
=====[[Show Who is Online]]=====
''Initial/default value:''  Yes
=====[[Show General Stats]]=====
''Initial/default value:''  Yes
=====[[Show Popular User Stats]]=====
''Initial/default value:''  Yes
=====[[Number of Popular User]]=====
''Initial/default value:''  5
=====[[Show Popular Subject Stats]]=====
''Initial/default value:''  Yes
=====[[Number of Popular Subject]]=====
''Initial/default value:''  5

===My Profile Plugin Settings===
=====[[Allow username change]]=====
''Initial/default value:''  No

