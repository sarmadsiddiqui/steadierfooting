---
id: 166
title: How To Minimize Tracking On The Web
date: 2012-03-25T23:08:02-04:00
author: Sarmad Siddiqui
layout: post
guid: http://steadierfooting.com/?p=166
permalink: /2012/03/25/how-to-minimize-tracking-on-the-web/
dsq_thread_id:
  - "624204348"
categories:
  - Uncategorized
---
These days a lot of web activity occurs behind the users’ back. Any link we click, any site we visit, is tracked and recorded by companies that we are completely unaware of. However, using some tools made by folks who are worried about our privacy and security, we can see and minimize the amount of tracking that is done as we traverse the web.

The web works on advertising. Most websites have some sort of advertisement. Closely associated with advertising is the concept of tracking cookies. These are small text files that an ad company leaves on users’ computers to collect information about them: the sites visited, the articles clicked on, etc[^1]. These tracking cookies allow advertisers to build a personalized profile of any user based on their browsing behavior to tailor ads according to their apparent preferences.

It’s not just advertising companies that like to track users’ movement across the web. Data collection companies use cookies to track movement across the web for analytics. Data collection by analytics companies can be used for two purposes. The first purpose is to provide website developers with more information about their audience: how a visitor landed on the page, what keyword search landed them there, was it through Facebook, etc. An example would be the service provided by Google Analytics, something I have deployed myself. The second purpose is to track the user himself: just like an ad company, tracking user movement across the web can be valuable data. An example would be the tracking done by Facebook on any site where a "Like!" button can be seen.

In and of itself, this behavior seems like a fairly reasonable compromise. A person visits a set of sites, and an ad company or data company collects some information that helps both advertisers and the end-user: the user might see ads relevant to their interests, and the ad company might attract a better click-through rate. However, one can quickly see how this behavior can be exploited by any company. If the collection company (ad or analytics) chooses to keep the data for long-term usage, it can become a privacy and security risk for the user. And that is exactly what has happened.

Companies &mdash; like Facebook and Google &mdash; have pushed the pendulum a bit too far towards their side by trying to collect every possible iota of user information on the web. They already have a lot of user data: emails, private messages, favorite bands, TV shows, etc. In one sense or another we as users have given them explicit permission to take and use this data. However, the practice of collecting data through a user’s browsing behavior seems a bit more sinister: most users are unaware of the practice, no one really knows how long the information is kept, or who this information is sold off too &mdash; of course it’s being sold, that’s why information is collected, to be sold to the highest bidder. I’ve only pointed out Facebook and Google, but there a plenty of other, less well-known companies that are in the same business.

The good news is that as users we can take some simple steps to minimize this tracking. The (more) bad news is that we have to be proactive about it. There are plenty of browser add-ons that claim to reduce tracking and increase privacy and security. Using a Firefox add-on called <a href="http://collusion.toolness.org/">Collusion</a> (by Atul Varma) we can actually visualize this tracking behavior, and see if these add-ons provide any tangible benefit.

## Visualizing Tracking

In order to do these tests, I visited particular articles on 18 fairly common sites[^2] using Firefox 10.0. I set up separate profiles for each configuration, and repeated each run 3 times.  The Collusion add-on uses information on known trackers from <a href='http://privacychoice.org/companies/all'>privacychoice.org</a> to construct a connectivity map showing sites that collect and store your information. Known trackers are shown with red dots, other connected sites are shown in grey; it’s unknown whether they collect and store information.  I visited the websites using several different settings and add-ons in Firefox to see how the tracking behavior is modified.

My first run was using the default installation of Firefox 10.0. The results can be seen in Figure 1 below.  There were an astonishing 66 trackers collecting information from the 18 visited sites. The largest tracker (largest red dot) was ‘Scorecard Research’ with 28 connections, followed by ‘doubleclick.net’ (Google) with 25 connections, and 'Nielsen Netratings’ with 21 connections. I was expecting a large number, but 66 confirmed trackers are still a bit too much from just 18 sites.

![No Privacy]({{baseurl}}/wp-content/uploads/2012/03/noprivacy.png)

<p style="text-align:center"><span style="font-size:small">Figure 1: Connectivity map of the default Firefox 10.0 installation.</span></p>

As most of the trackers were associated with advertisement firms, I decided to use the popular add-on <a href='https://adblockplus.org/en/'>Adblock Plus</a> (by Wladimir Palant) for my next run. As Adblock Plus prevents the actual third-party site code from loading, I assumed that it would suppress tracking cookies. And that’s exactly what happened. Loading the same 18 sites/ articles produced a very different connectivity map this time. Only 9 trackers were detected (Figure 2, below). The largest tracker was again ‘Scorecard Research’, followed by ‘Nielsen’ and then ‘Quantcast’. The number of connected sites for each was 14, 9 and 7, respectively. So just using Adblock Plus drops tracking by seven fold. Quite impressive results from just one add-on.

![Adblock]({{baseurl}}/wp-content/uploads/2012/03/adblock.png)

<p style="text-align:center"><span style="font-size:small">Figure 2: Connectivity map of Firefox with the Adblock Plus add-on.</span></p>

After installing Adblock Plus, I installed a spate of add-ons that don’t target non-advertising networks in particular, but are still useful for privacy and security. They were <a href='https://www.eff.org/https-everywhere'>HTTPS-Everywhere</a>, <a href='https://addons.mozilla.org/en-US/firefox/addon/beef-taco-targeted-advertising/'>Beef Taco</a>, and <a href='https://addons.mozilla.org/en-US/firefox/addon/betterprivacy/'>Better Privacy</a>. HTTPS-Everywhere (by the EFF) forces a secure connection on sites that provide that option. Better privacy deletes ‘supercookies’ on exiting the browser. Supercookies can be a number of different things, but Better Privacy deletes Flash based objects (called <a href='https://en.wikipedia.org/wiki/Local_Shared_Object'>LSO</a>). One caveat though, by default it deletes all stored Flash objects, so if you play Flash games, you’ll have to manually whitelist that site. The last add-on, Beef Taco (by John Hobbs), sets permanent opt-out cookies for ad networks. Because it doesn't target other types of tracking cookies, I didn’t run Collusion to visualize how it changes the connectivity map. In hindsight, it would have been a good idea.

The next anti-tracking add-on I installed was <a href='https://disconnect.me/'>Disconnect</a>. It’s a fairly new add-on compared to the rest and I had heard good things about it, but it was a bit disappointing. As it can be seen below (Figure 3), the number of confirmed trackers increased to 12. The top three trackers were the same as Adblock Plus, but their connected sites were now read 12, 8, and 6. It seems that Disconnect only focuses on social networks in particular, and perhaps that’s why it isn’t particularly effective. Maybe Disconnect interfered with the above mentioned add-ons and caused an increase in trackers from 9 to 12.

![Disconnect]({{baseurl}}/wp-content/uploads/2012/03/disconnect.png)

<p style="text-align:center"><span style="font-size:small">Figure 3: Connectivity map of Firefox with the Adblock Plus, HTTPS-Everywhere, Beef Taco, Better Privacy, and Disconnect add-ons.</span></p>

For my next run, I used an older add-on called <a href='http://www.ghostery.com/download'>Ghostery</a> (by David Cancel) instead of Disconnect (the other add-ons were still in place). Ghostery has a very large blacklist of third-party cookies that isn’t enabled by default. I enabled the entire blacklist, some 850 sites or so before visiting the same 18 sites. The results were fantastic. Only 1 confirmed tracker remained. It was outbrain.com, connected to cnn.com. So a 66 fold decrease from the default Firefox installation!

![Several adblockers]({{baseurl}}/wp-content/uploads/2012/03/ghostery.png)

<p style="text-align:center"><span style="font-size:small">Figure 4: Connectivity map of Firefox with the Adblock Plus, HTTPS-Everywhere, Beef Taco, Better Privacy, and Ghostery add-ons</span></p>

After the Ghostery run, I did another run with all the aformentioned add-ons enabled simultaneously (the “kitchen sink” if you will). The results were similar to that of of the Ghostery configuration: only 1 tracker remained. My last run was with a very old piece of software, something I’ve been using since the dinosaur days called <a href='http://www.javacoolsoftware.com/spywareblaster.html'>SpywareBlaster</a>. It’s a blocklist that stops many browsers from loading known malware. It didn’t affect the connectivity graph either, but in this case that just might be because the 18 sites I visited were well maintained, safe sites. It’s blocklist is probably very useful when visiting the dark corners of the internet (I’m sure everyone ends up at a strange unheard link every now and then).

Here’s a summary of the results:

<p>
<table>
    <tr>
        <th style='text-align:center'>State</th>
        <th style='text-align:center'># of Trackers </th>
    </tr>

    <tr style='background-color:#F5F5F5; color:black'>
        <td style='text-align:left'>Default Installation</td>
        <td style='text-align:center'>66</td>
    </tr>

    <tr style='background-color:#F5F5F5; color:black'>
        <td style='text-align:left'>Adblock Plus 2.03</td>
        <td style='text-align:center'> 9</td>
    </tr>

    <tr style='background-color:#F5F5F5; color:black'>
        <td style='text-align:left'>Disconnect*</td>
        <td style='text-align:center'>12</td>
    </tr>

    <tr style='background-color:#F5F5F5; color:black'>
        <td style='text-align:left'>Ghostery*</td>
        <td style='text-align:center'>1</td>
    </tr>

    <tr>
        <td colspan=2 style='background-color:#F5F5F5; color:black; text-align:left'> *With other add-ons installed (see text)</td>
    </tr>
</table>
</p>

## Conclusions and Recommendations

For most of my recommendations to actually work, you’ll have to be using Firefox. I’ll come back to other browsers in a bit.

Based on my results, at a minimum, I’d recommend installing the following add-ons for blocking tracking cookies: Adblock Plus & Ghostery. Installing Adblock Plus comes with a warning though. After installing it, the amount of ads you’ll encounter will drop pretty close to zero. In alot of cases this improves the browsing session greatly, but it directly affects the money the site owners make. As such I’d recommend whitelisting sites that you visit frequently. It can be done by clicking on the adblock plus icon in the menu as selecting ‘Disable on sitename…’:

![Adblock Menu]({{baseurl}}/wp-content/uploads/2012/03/adblockmenu.png)

<p style="text-align:center"><span style="font-size:small">Figure 5: How to whitelist frequently visited sites in Adblock Plus.</span></p>


By default Ghostery just shows the trackers, it doesn’t actually disable them. This can be changed by going to the 'Firefox' button &#62; Add-ons &#62; Ghostery &#62; 'Options' button. In the general tab, click the ‘3pes’ tab and check all the categories to disable all third-party cookie communcaiton with their respectve servers. In practice, I keep ‘Google Analytics’ and ‘Disqus’ enabled as I use those services often. Most folks would probably want to enable (keep unchecked) Facebook and Twitter plugins as well. These social plugins are found in the ‘Widgets’ category under the ‘3pes’ tab. More astute folks will notice a ‘Cookies’s tab next to the ‘3pes’ tab. This has similar functionality to the earlier mentioned Beef Taco add-on. I haven’t experimented with it, but I expect it to serve the same purpose. You can choose to disable all the cookies, or install Beef Taco to accomplish the same goal. While in the Options menu, you might as well hit the ‘Advanced’ tab and change the ‘Show Alert Bubble’ to less than 5 seconds from the default 15 seconds. I find the default setting a bit too long for my tastes:

![Ghostery Menu]({{baseurl}}/wp-content/uploads/2012/03/ghosterymenu.png)

<p style="text-align:center"><span style="font-size:small">Figure 6: Ghostery Advanced Options.</span></p>

Adblock Plus and Ghostery do a very good job of blocking tracking cookies by themselves. Browsing will be much safer just with these two add-ons installed. The other add-ons I used in this post’s runs provide other benefits that are useful, but not necessary for blocking tracking cookies. I’d still recommend installing them, but for other reasons.

Lastly a note on browsers. I’m partial to Firefox myself, and I think it holds up well against most other browsers. The only other browser worth using (at least in Windows/ Linux) is Google Chrome. In my opinion it has two great features that Firefox doesn’t: sandboxing and individual process per tab. On the other hand, it gives the user much less control, and it’s a bit of a laggard in add-ons for privacy and security. It does have Adblock Plus[^3] and Ghostery add-ons, which is great. But I’d still say use Firefox. Either way, install some of these add-ons, and start browsing safely!

-------

### Footnotes

[^1]: It's actually a two way process: first a cookie is left on the computer, then it can communicate with a server. A good summary is on Wikipedia [(link)](https://en.wikipedia.org/wiki/HTTP_cookie#Privacy_and_third-party_cookies).

[^2]: Well the definition of common depends on where your interests lie I suppose. Either way, they are popular sites: amazon.com, apple.com, cnet.com, cnn.com, cricinfo.com, espn.com, facebook.com, gmail.com, huffingtonpost.com, imdb.com, lifehacker.com, microsoft.com, nyt.com, rottentomatoes.com, slate.com, si.com, theverge.com, twitter.com. You can download the links to the exact articles by downloading this [html file]({{baseurl}}/wp-content/uploads/2012/03/eighteen_sites.html) if you want to reproduce these results.

[^3]: The Chrome version is not exactly the same as Firefox's version. It might affect tracker blocking; it's something I don't know. You can download it here [(link)](https://adblockplus.org/en/chrome).