---
title: 'Frequently Asked Questions'
---

### What version of Kunena should I use (and does it matter what version of Joomla I use, either)?

We always recommend that people should use the latest stable version of Kunena available from the Download page. If you are using an older version of Kunena we recommend that you upgrade to the latest version and, at the same time, upgrade to the latest version of Joomla.before you ask for support.

### What do I need to know to install or upgrade Kunena?
Please read the [installation guide](../../../basics/installation) and/or [upgrade guide](../../basics/upgrade) for the answers to this question. You should also familiarise yourself with the technical requirements and any specific last-minute details included with the version [release notes](../../troubleshooting) documentation.

### What information should I include when I ask for help?

>>>>> Include your configuration report when you ask questions on the forum. If you include your unedited configuration report you will improve the chances of a quick solution to your problem! This can save you hours, days or even weeks waiting for a solution.

To help you to help us to help you solve your forum questions (particularly if you are reporting a defect or a serious problem that you're having with Kunena) please include your [Kunena configuration report](../../faq/configuration-report). Some of the information contained in the report remains confidential so as to ensure that only you and the forum moderators/administrators can see it. Please do not edit that report. By including your original, **unedited** configuration report you will save your time and our time in answering your questions.

If your website is not accessible on the internet (or if you have prevented non-registered users from accessing the site) we may not be able to help you directly. In cases like these we can only provide general answers that may, or may not, relate to your specific issues. Please be aware that those who offer their help may not experts in everything and they will try to answer your questions as soon as possible. To help us to understand your problem better, please try to include as much information as you can (or post a picture or two) that you think demonstrates your problem.

### "Confidential information" - what does that mean?

The configuration report contains some information that identifies your site, the Joomla software platform on which your site is built - web server software (e.g. Apache) software, database (e.g. MySQL) software, server-side scripting (e.g. PHP) software among other things - that, under normal conditions, could be used by other people in ways that would be against your interests. The members of the Kunena team take these matters seriously and we value the trust that members of the community place in us when they offer that information. The Kunena BBcode [confidential] tags help protect you from disclosing that kind of information to others whom you would not want to know about such things. The Kunena BBcode [confidential] tags are there for your protection. Removing those sections from your configuration report is not to your benefit if you want members of the Kunena team to be able to help you with questions you ask on the forum. Editing your configuration report, by removing the "confidential sections" will only slow down the resolution of your problem. However, if you decide to remove those parts from your configuration report because, in your opinion, do not think we should know such things we will respect your decision to do so. If you remove or edit parts of your configuration report you should do so in the knowledge that Kunena team members may be unable to help. We respect your right to edit your configuration report. Please respect our right not to respond to questions if we do not have information that we need to help us.

The Kunena website does not have a private message facility. Kunena team members also will not reply to questions sent to them, privately, by email. If you have a matter that you wish to discuss privately with a specific Kunena team member, it is entirely a matter between you and that team member to make some private arrangement to do this. The Kunena team does not encourage nor discourage the private exchange of information. The forum is the best place to obtain help and the Kunena BBcode [confidential] tags are there to protect your privacy.

If you think that we should have access to your site in order to analyse and diagnose your problem, it is your responsibility to organise a test account. In most cases a non-privileged user account will be quite sufficient. You should post this information by using the Kunena BBcode [confidential] tags, like this: `[confidential]Username Password[/confidential]`
We remind all users that the Kunena forum is a community-driven, self-help resource that relies on community involvement. Kunena is not-for-profit; there is no company behind the product. Kunena will always remain freely-available open source software that is free to download, free to install with no hidden licensing charges. We ask that people to remember these things and to extend the same courtesy to those who offer their help to you voluntarily and without payment for their time.

### Javascript-related problems

#### Why can't I see the BBcode toolbar to insert Kunena BBcode?

The reason this happens is because you have another Joomla extension (a component, template, module, plugin or language) that uses a Javascript library that conflicts with Joomla's Mootools Javascript library.

#### Why can't I edit my Kunena user profiles (including setting forum preferences, avatar image, etc.)?

You have another Joomla extension (a component, template, module, plugin or language) that uses a Javascript library that conflicts with Joomla's Mootools Javascript library.

#### Why can't I use the Quick Reply feature and, in some cases, the Quote feature?

You have another Joomla extension (a component, template, module, plugin or language) that uses a Javascript library that conflicts with Joomla's Mootools Javascript library.

#### Why can't I use the "smiley selector" to insert emoticons into Kunena messages?

You have another Joomla extension (a component, template, module, plugin or language) that uses a Javascript library that conflicts with Joomla's Mootools Javascript library.

#### Why can't I use the expand/collapse feature used on various sections of Kunena pages?

You have another Joomla extension (a component, template, module, plugin or language) that uses a Javascript library that conflicts with Joomla's Mootools Javascript library.

### Kunena menu issues

#### How do I change the "default view" of the forum from Recent Topics to Index?

Go to **Kunena Menu** (in Joomla Menu Manager) and change the first entry. There's option that allows you to select a different the default "entry" page.

#### How do I restore my Kunena menu?

The Kunena menu is a set of tabs that appears across the top of the forum pages. In some cases, this menu does not appear for a variety of causes (see also [Menu issues](../../troubleshooting/menu-issues)).

**The Kunena trash-burn-build technique:**

1. Trash all existing menus and menu items that relate to your Kunena forum.
2. Empty the menu trash.
3. Use the Kunena Control Panel: **_Dashboard -> Tools -> Menu Manager -> Restore Kunena Menu_** facility.
4. Publish the menu item created for you in your top-level/main menu.

#### How do I edit, hide, disable or translate menu items in Kunena (e.g. rules, help, search)?

The menu items (the text contained in the Kunena menu tabs) can easily be edited by using the Joomla Menu Manager **_Menus -> Kunena Menu -> Menu Item_**.

#### This webpage has a redirect loop

The problem only affects Joomla websites that have enabled Search engine optimisation [SEO(../../SEO) where two Joomla menu items have the same menu alias but point to different targets. In some cases this problem also goes hand-in-hand with the issue of a missing or unpublished Kunena menu. The correct way to resolve this issue is to understand how Joomla menus work.
In most cases, the issue can be addressed by ensuring that each menu item has a unique menu alias.
A simple solution can also be to use the [Kunena trash-burn-build technique](../../faq/frequently-asked-questions#how-do-i-restore-my-kunena-menu).

### Template and layout-related issues

#### How to insert banner advertisements (e.g. Google AdSense) in Kunena

Kunena templates incorporate [module positions](../../faq/module-positions) within which you can place any Joomla module (e.g. Joomla Google Ads module) but are not limited to modules for advertising purposes. Anything that can be displayed inside a module can be shown inside Kunena through these positions.
Sizing and available space should be considered carefully as large modules can consume significant portions of your screen real estate.

#### How do I change the colours of my template in Kunena?

If you want to change colours, text sizes or fonts, you should make those changes in the custom.css or custom.less. **_Backend -> Kunena Forum -> Templates -> mark your template -> Edit CSS (or LESS) -> mark custom.css (or custom.less) -> Edit CSS (or LESS)_**. In this way, when you upgrade Kunena, your forum template will apply the customised changes that you've made from one version to the next.
Some changes can be achieved by using the template options that come with the Kunena templates. To change those things, go to **_Backend -> Kunena Forum -> Templates_**  and click the template link.
Other customised changes can easily be achieved by defining your own CSS rules for the individual Kunena page elements. We recommend that you use a web design tool like Firebug for Firefox (other browsers have their own developer's tools).

### General Joomla issues

#### How do I implement Search Engine Optimisation - SEO - in Joomla?

See [Search engine optimisation (SEO).](../../faq/SEO)

#### How do I register new users to my website and where should they login to use my website?

We need to be quite clear on this matter: **Kunena is not responsible for user registration or login to your website.** These are Joomla issues (that may or may not be assisted by third-party extensions like JomSocial or Community Builder if you have such products installed).
If your users are unable to register at your website, check **_Users -> Manage -> Options -> Allow User Registration = Yes / No_.**
You can provide your users with a place to login (in Kunena) with the forum setting: **_Kunena Forum -> Plugins -> Kunena - Joomla Integration -> Enable Joomla Login = Yes_**.

Kunena is also not responsible for
* sending out "confirm this message" emails when people register
* the format or details of "confirm this message" emails when people register
* making sure that people actually use the forum; or
* making sure that all the user's registration details are correct or checking that the user has a valid email address.

### General website construction and forum management issues

#### Which comes first: the template or the forum?

Good planning for your website is what comes first. Ask yourself the question: What outcome am I looking for and what objectives am I hoping to achieve by building a website? If the answer to this question is that you want to maximise the involvement of your users in your site - and you want Kunena to be the mechanism to achieve this goal - then, obviously, the forum comes first and all the other trappings are secondary. If, on the other hand, "looks" is all-important and you don't really care what kind of forum you want to use, then it really does not matter ... but it also might mean that integrating Kunena into your plans will not go as smoothly as you would like.

Sort out your priorities first. Plan how you intend to build your website and choose carefully the components that you need to achieve your goals. It's important that you have a test site where you can trial new ideas and different approaches to meeting your goals. If Kunena is what you have decided is the most important piece of your website puzzle, then keep your focus on that. Implement a solution built around Kunena rather than add it on as an after-thought.

#### How do I protect my forum from spam?

This is an all-time favourite question asked about every web-based discussion forum and the problem is not confined to Kunena or to any specific version of it. There is no simple cure for this issue although many recommendations have been offered in the forum topic [How to I protect my forum from spam?](http://www.kunena.org/forum/154-Miscellaneous-off-topic-and-general-Joomla/37183-how-to-protect-my-forum-from-spam?limitstart=0)

Some websites (and their forums) are more susceptible to spam attacks than others. Certain sites (those that deal with online games or anime, for example) seem to be more attractive to spam postings than others and that's just the way things go. There are many strategies that you can employ to minimise the extent of spam messages, such as limiting the ability for spam-related accounts to register on your site, but in the end the only effective remedy against spam is vigilance. This means that you need to remain alert to what happens on your forum and deal immediately when problems like these arise. No forum is immune to the problem but the effort you make will keep the problem under control or, at least, manageable.

We recommend that you do not give unrestricted posting access to your forums (unless that is your intention to do so). For every decision that you make there are consequences of those decisions and costs involved in maintaining your forum so as to minimise the ill-effects that spam messages will have on your web community. If you want to maintain a healthy, spam-free forum you need to be alert and make effective use of the [forum moderation tools](../../troubleshooting) included in Kunena.
