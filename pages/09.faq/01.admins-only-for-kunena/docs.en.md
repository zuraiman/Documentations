---
title: ' Admins only for Kunena'
---

#### Introduction

This tutorial will show you to how to create administrators only for Kunena.

>>>> Important! Create a database backup before. There is no reset option in Joomla to undo it if incorrect permissions are set.

### Step 1: Add New User Group

**_Backend -> Users -> Groups -> Add New Group_**

![](new_group_g5.png)

### Step 2: Group Title

Now you'll see a new window User Group Details.
* Enter a Group Title
* Click **Save & Close**

![](group_title_66.png)

The new Group has been created.

![](kunena_admin.png)

### Step 3: Add Users to the Group

* Go back to the user management
* Mark your desired users
* Use the Batch function

![](add_users_to_the_group_22.png)

* Select User Group
* Click **Process**

![](add_656.png)

### Step 4: Permission Setting for this Group

* **_Global Configuration -> (Tab) Permissions_**
* Site Login - **Allowed**
* Administrator Login - **Allowed**
* Offline Access - **Allowed** 
* Save & Close

![](permissions_settings_33.png)

### Step 5: Permission Setting for Kunena

* Go to **_Kunena Dashboard -> Options_**

![](options_m332.png)

* Select - (tab) Kunena Admins
* Access Administration Interface - **Allowed**
* Save & Close

![](admin_access_3.png)

If everything was done correctly. then have Kunena Admins backend access but no access to Joomla features.

![](backend_control_panel.png)