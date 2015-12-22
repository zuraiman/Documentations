---
title: 'Internal Server Error and Kunena'
taxonomy:
    category:
        - docs
---

Sometimes the first indication that there is a HTTP 500 Internal Server Error may be no indication at all! Sometimes the only symptom is a blank page. Neither of these symptoms is very helpful and you may need to make a small change to the Kunena (and possibly Joomla) configuration. More about what to change in Joomla later. For now, the first thing that you should do is enable Kunena debug mode.

#### Enable Kunena Debug Mode:
**_Forum Configuration -> General -> Basic Settings -> Enable Debug Mode = Yes_**

Enabling Kunena debug mode also enables part of Joomla debug mode. When you enable Kunena debug mode you may then see more information that indicates what is causing the underlying problem. This additional information may give you some added clues as to what is causing the problem and where to look. The easiest way to look is to search the forum for the error message. It is possible that the error has been reported before and that it is a known problem with a specific solution.

In the cases of errors occurring with Kunena software (e.g. "Class 'KunenaClass' not found in components/com_kunena/kunena.php") the best thing to do, before reporting your problem on the forum, is to make sure that you are using the lastest version of Joomla and the most-recent public stable release of Kunena. You can save yourself a lot of time if you upgrade to the latest supported version of Kunena and, at the same time, upgrade to the latest version of Joomla.

#### Using Joomla debug mode

Because HTTP 500 Internal Server Errors arise from so many different sources, sometime enabling Kunena debug mode is not enough. In these more difficult cases it's also necessary to enable Joomla debug mode. This is achieved with the following settings:
**_Global Configuration -> System -> Debug Settings -> Debug System = Yes 
Global Configuration -> Server -> Server Settings -> Error Reporting = Maximum_**
These changes may give you more information. In addition, there will be other details recorded in the server logs and you can look at those to see what else is happening.
