---
id: 1
title: A Review of Mozilla Thunderbird 5.0
date: 2011-08-23T10:25:31-04:00
author: Sarmad Siddiqui
layout: post
guid: http://steadierfooting.com/?p=1
permalink: /2011/08/23/hello-world/
dsq_thread_id:
  - "339821443"
categories:
  - Uncategorized
---
<a href="{{baseurl}}/wp-content/uploads/2011/08/TbirdLogo200x200.png"><img class="aligncenter size-full wp-image-33" title="TbirdLogo200x200" src="{{baseurl}}/wp-content/uploads/2011/08/TbirdLogo200x200.png" alt="Thunderbird Logo" width="200" height="200" /></a>

The latest version of Thunderbird, the desktop email client by Firefox's parent company Mozilla was released recently. It is one of the few actively developed desktop email clients these days, and as such makes an interesting case study. In this review I’ll look at the notable changes in the latest version of Thunderbird and comment on things that Thunderbird needs to do well to stay relevant in a world where most consumers rely on cloud based services for email access and storage.

## UI Changes

Although the version number has jumped from 3.1 to 5.0, there aren’t any dramatic changes in store. In fact, in a side to side comparison of versions 3.1, and 5.0 (on both Windows and Linux) the UI looks exactly the same. The only visible difference is that Thunderbird's theme in Windows 7 matches the default Windows Aero theme. The transparency effect of this theme extends to the entire chrome, including the button icons and lettering, which is where a usability problem arises. If the user has a dark or patterned background, the menu buttons and text become quite illegible. So really, the only noticeable UI change comes at the cost of a usable user interface. It’s interesting to note that Firefox 4.0/5.0 uses a similar theme, however limits the transparency effect to the title bar. That results in a look consistent with the OS while still being functional.
<table>
<tbody>
<tr>
<td><a href="{{baseurl}}/wp-content/uploads/2011/08/tb_3.1.png"><img class="alignnone size-thumbnail wp-image-31" title="tb_3.1" src="{{baseurl}}/wp-content/uploads/2011/08/tb_3.1-150x150.png" alt="Thunderbird 3.1" width="150" height="150" /></a></td>
<td><a href="{{baseurl}}/wp-content/uploads/2011/08/default_transperent_chrome.png"><img class="alignnone size-thumbnail wp-image-28" title="default_transperent_chrome" src="{{baseurl}}/wp-content/uploads/2011/08/default_transperent_chrome-150x150.png" alt="Thunderbird 5.0 on Windows 7" width="150" height="150" /></a></td>
<td><a href="{{baseurl}}/wp-content/uploads/2011/08/linux2.png"><img class="alignnone size-thumbnail wp-image-30" title="linux2" src="{{baseurl}}/wp-content/uploads/2011/08/linux2-150x150.png" alt="Thunderbird 5.0 on Ubuntu 11.04" width="150" height="150" /></a></td>
</tr>
</tbody>
</table>
<span style="font-size: 12px;">From left to right: Thunderbird 3.1 on Windows 7, Thunderbird 5.0 on Windows 7, and Thunderbird 5.0 on Ubuntu 11.04</span>

<a href="{{baseurl}}/wp-content/uploads/2011/08/default_screen_small.png"><img class="aligncenter size-full wp-image-35" title="default_screen_small" src="{{baseurl}}/wp-content/uploads/2011/08/default_screen_small.png" alt="Default Transparency" width="480" height="64" /></a>

<span style="font-size: 12px;">Dark or textured backgrounds make the menu buttons illegible with Thunderbird 5.0’s default theme on Windows 7 / Vista. </span>

The good thing is that there are a couple of simple fixes to this problem. The first one is to limit the transparency effect to the title bar, similar to Firefox. This will not only solve the legibility problem, but will also draw parallels to Firefox, its sibling browser. It’s obviously not a high priority change, but it will bring some visual consistency between the product family.   The second solution is to simply introduce opaque toolbar buttons (with text). This will work great as far as usability is concerned, but the two products will continue to look very different –missing the polish, so to speak.  I’m well aware that as a user I can simply install a different theme, but I’m just pointing out flaws in the default design –the first thing that a new user will see when they install this software.

Other visible changes include an add-on manager integrated into the main window, and tear away tabs. Both these features are found in Firefox, and it’s good to see similar design philosophy propagate to Thunderbird. The features work as expected; the tear away tabs are particularly handy in separating a thread of emails from the main program window. Other than the above mentioned cosmetic changes, there aren’t any particular updates to highlight. Most of the changes are behind the scenes –according to the release notes, over 400 fixes are included.

## Email Set-Up and Use

Functionality wise, the browser is as stable it has always been.  There aren’t any noticeable changes in day to day usage. It’s quick to startup, and everything works as expected.  Things that are to be expected from a modern client are all there: keyboard shortcuts, powerful search, indexing with the system search. The only thing to mention here is that the new account setup is more streamlined – it is easier to import settings from common email providers (Gmail IMAP and Hotmail POP worked without a hitch for me). Importing from other email providers that use POP or IMAP is straight forward as well. Unfortunately, Microsoft Exchange is not supported, so those users will have to look elsewhere.

One deterrent that might prevent Gmail users from using Thunderbird might be the incomplete compatibility between the two systems. The problem arises due to Gmail’s unique approach to folders – it doesn’t use them. Instead, Gmail uses tags, which allows users to assign an email to multiple categories. An email with multiple tags is simply copied into multiple folders in Thunderbird. This won’t affect people who use tags as folders but it might prove to be a slight annoyance to power users. It would be nice if Mozilla implements a “fix” for this problem; however this is not an industry standard and as such probably against Mozilla's development policy – after all, their goal as a company is to develop software that strictly adheres to open standards.

Excluding Gmail’s unique quirks, IMAP syncing with other email providers works perfectly. There is no problem syncing, even with multiple clients. Emails can be archived locally or onto folders from the provider.  As far as email is concerned, things just work.

## Features in Need of an Update

The refrain of this review has been the lack of user noticeable changes, and it continues with implementation of threaded view: it has been unchanged since its introduction in version 3.0. A thread only shows a snippet of text from each email. In order to read the entirety of one message, it must be opened separately. It would have been nice if the implementation was similar to that of Gmail, but that’s not the case. The good news is that there is an experimental add-on trying to bring Gmail-like threaded view, and I’ll touch on that soon.

The address book is another feature that has remained unchanged. At the bare minimum it would have been nice to see it integrated into the main window similar to the add-on manager, but that’s not the case. Incidentally, the analogous bookmark manager in Firefox also exhibits the same behavior. It would have been nice to see some sort of importing and syncing feature with online address books (Gmail, Facebook, etc), but again Thunderbird 5.0 falls short; There is an experimental add-on to remedy this, but the project remains untouched for more than six months, and is incompatible with Thunderbird 5.0. As a result I chose not to review it.

This concludes the review of the default Thunderbird installation. It’s already a mature product, and unfortunately version 5.0 doesn’t bring anything revolutionary to the table. Old users shouldn’t hesitate to upgrade to it as the product is stable and most common add-ons are compatible with it. New users who have moved away from desktop clients to the web might not find anything new to entice them back. That being said, the greatest feature about Thunderbird is its add-on support. And that is where the excitement lies…

## Add-ons

### Lightening 1.0b4

Lightening is the calendar add-on for Thunderbird.  Although it is officially version 1.0 beta 4, it is a very mature product. Calendars from other services can be imported using CalDAV and iCal. Users using Google Calendar must install an additional add-on, called ‘ Provider for Google Calendar’ to enable bidirectional syncing. Without the second add-on, the calendar only has read-only access.  The calendar does support importing information from an email, but parsing the information fields is hit or miss. Altogether it makes Thunderbird into a decent calendaring application, supporting reminder notifications, emails, alarms, etc.

### Conversations 2.03

The other exciting add-on that is being developed is called Conversations. Currently it is an experimental add-on; usually Mozilla releases features as experimental add-ons before integrating them into the main program. Firefox’s Sync, Panorama, and F1 were all experimental add-ons before they were integrated into the main program. Conversations is a replica of the Gmail-style threaded view –it hides reply quotes, minimizes headers and has a quick reply feature exactly like Gmail. The implementation works fairly well, but isn’t perfect. Most threads are rendered fine. However on occasion it has trouble showing emails from the ‘sent’ folder. Instead of showing the emails chronologically, the ‘sent’ emails are aggregated before the incoming replies are displayed.  A few emails here and there aren’t rendered at all either. Both these problems are rare, but still important to know for those thinking of installing the add-on.

All that being said, the biggest problem with the Conversations add-on is the UI –it looks like a web interface and not a native desktop application. The rendering is very similar to Gmail. Functionality wise this is fine, but it’s not great UI design.  It would be preferable to design the add-on so that it meshes with the existing Thunderbird UI. As it stands, the client’s top half looks like a native desktop client, and the bottom half looks like a web application. Call it Mozilla’s monster if you will. It would be far more appealing to have a fixed quick reply box, and use the middle pane to display information related to the currently expanded  email  (from an opened thread). This is a native desktop client, there is no need to imitate a web application’s design. The good thing is that this is still a work in progress, and hopefully Mozilla will address these concerns in the future.
<table>
<tbody>
<tr>
<td><a href="{{baseurl}}/wp-content/uploads/2011/08/threaded.png"><img class="alignnone size-medium wp-image-34" title="threaded" src="{{baseurl}}/wp-content/uploads/2011/08/threaded-271x300.png" alt="Threaded View" width="271" height="300" /></a></td>
<td><a href="{{baseurl}}/wp-content/uploads/2011/08/conversations.png"><img class="alignnone size-medium wp-image-26" title="conversations" src="{{baseurl}}/wp-content/uploads/2011/08/conversations-280x300.png" alt="Conversations View" width="280" height="300" /></a></td>
</tr>
</tbody>
</table>
<span style="font-size: 12px;">The default threaded view (left) and the Conversations add-on (right) </span>

## Wrap-Up

Although this update brings Thunderbird from version 3.1 to 5.0, there are no revolutionary updates with this jump in number. In fact, the only reason the number jumped was to keep it in sync with the development cycle of the underlying rendering engine (Gecko). That being said, there have been numerous bug fixes and slight UI changes, most of them for the better. The default Windows 7/ Vista theme, though nice, is problematic. There is definitely room for improvement here. However, existing users should have no reason not to upgrade. Unfortunately, new users will have little to entice them to the platform.

------


<span style="font-size: 12px;">
<strong>Sources</strong></span>
<span style="font-size: 12px;">
<br />Download Mozilla Thunderbird (<a href="https://www.mozilla.org/en-US/thunderbird/">link</a>)
<br />Thunderbird 5.0 Release Notes (<a href="https://www.mozilla.org/en-US/thunderbird/5.0/releasenotes/">link</a>)
<br />Lightening 1.04b Add-on (<a href="https://addons.mozilla.org/en-US/thunderbird/addon/lightning/">link</a>)
<br />Conversations 2.08 Add-on (<a href="https://addons.mozilla.org/en-US/thunderbird/addon/gmail-conversation-view/">link</a>)
<br />Thunderbird Logo obtained from MouseRunner (<a href="http://www.MouseRunner.com">link</a>)
</span>