---
title: 'Menu Tips'
---

#### Restore Kunena Menu

A simple remedy for the problem is to use the trash-burn-build technique (see also [Menu Issues](../../troubleshooting/menu-issues)):

1) Trash all existing menus and menu items that relate to your Kunena forum
2) Empty the menu trash.
3) Use the Kunena Control Panel: Forum Tools -> Menu Manager -> Restore Kunena Menu facility.
4) Publish the menu item created for you in your top-level/main menu.

#### Changing URL / Menu Alias

If you want to change menu alias `www.domain.com/forum` to something like `www.domain.com/discussions`, you cannot change it by just renaming your own menu item. In order to do that, you need to change menu alias directly from the Kunena Menu:

1) Go to Menu Item Manager: **_Menus -> Kunena Menu_**
2) Edit the menu item **Forum**
3) Change Alias

#### Rename or translate Menu Items in Kunena (e.g. Index, Recent Topics)

The menu items (the text contained in the Kunena menu tabs) can easily be edited by using the Joomla Menu Manager.
**_Menus -> Kunena Menu -> Menu Item -> To alter the Menu Title_**

#### Changing Default Landing Page in Kunena

**Kunena** allows you to change default landing page in your menu. This allows you to have control on what people will see when they enter to the forum.

1) Go to Menu Item Manager: **_Menus -> Kunena Menu_**
2) Edit the menu item **Forum**
3) Change Default Menu Item

#### Showing and Hiding Menu Items

Just publish and unpublish your menu items in Kunena Menu. You can also restrict access to certain pages by changing Access Level of the menu item.

>>>> Hiding different views from the menu do not hide them from resourceful users. Users can still find a way to access all the different views, but they cannot see posts in restricted categories.

#### Menu Types

Kunena provides a few different views that can be added to Kunena Menu. Those are:

* **Rules / Help** - Show forum [rules or help pages](../../faq/rules-or-help-pages).
* **Entry Page** - Entry page for Kunena instance. 
* **Recent Topics** - Show recent topics or posts.
* **Index** - Show category index page.
* **New Topic** - Create new topic.
* **Profile** - Show user profile.
* **Search** - Advanced search.
* **Category** - Show topics in a category.

#### Recent Topics

Shows a list of recent topics or posts. There are many different layouts to pick from:

* **Recent Topics** - Shows recent topics
* **My Topics** - Shows topics from the current user (My Favorites and My Posts)
* **No Replies** - Shows topics which haven't been answered
* **My Subscriptions** - Shows subscriptions from the current user
* **My Favorites** - Shows favorites from the current user
* **My Posts** - Shows posts from the current user
* **Unapproved Posts** - Shows unapproved posts
* **Deleted Posts** - Shows deleted posts

#### Index

Category index page showing all the categories in the forum.

* **Parent Category ID** - Can be used to show only part of the category tree.

#### New Topic

Start new topic either in any category (defaults to first option) or only in one category.

#### Profile

Menu item to users own profile. If you want to restrict access only to registered users, use **Access Level** to do it.

* **Use Integration** - Yes, if you want to get redirected to another component.

#### Category

Show topics in one category. This can be used to show categories in your menu.