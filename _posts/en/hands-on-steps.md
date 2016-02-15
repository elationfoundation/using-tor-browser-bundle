---
title: Tor Browser Bundle Hands-On Steps
creator:
    - Lindsay Beck
    - Chris Walker
id: hands-on-steps
location: en/hands-on-steps.md
last_updated: 04/2015
---

Tor Browser Bundle Hands-On Steps:
==================================

In this exercise, participants will use the Tor Browser Bundle to create an anonymous connection, confirm that it is working, and change their Tor "exit relay."

1. Show the public IP address of the training room's Internet connection
------------------------------------------------------------------------

-   In a browser, visit [whatismyip.com](https://whatismyip.com/) (https) or [whatismyipaddress.com](http://whatismyipaddress.com/) (which includes a map)

-   Explain the concept of sites like whatismyipaddress.com. (And, if necessary, explain the concept of an IP address)

-   Invite participants to visit the site themselves, using their own devices.

2. Show the public IP address of the Tor "exit relay"
-----------------------------------------------------

-   Close all web browsers

-   Launch the Tor Browser Bundle by running "Start Tor Browser.exe" and clicking "Connect"

-   Wait until a Tor connection is established and a new browser window has opened (this could take several minutes)

-   Tor Browser should load a page that says: "Congratulations. This browser is configured to use Tor.” (If for some reason your Tor connection fails, it will say: "Something Went Wrong! Tor is not working in this browser.")

-   In Tor Browser, visit [whatismyip.com](https://www.whatismyip.com/)  or  [whatismyipaddress.com](http://whatismyipaddress.com/) and show that the IP address has changed.

3. Show how to select a new path through the Tor network
--------------------------------------------------------

-   Explain that Tor could conceivably select an “exit relay” in the same country as the user. (An "exit relay" is the Tor server from which one's outgoing traffic leaves the Tor network, and through which one's incoming traffic enters it.) This is not good for anonymity. It is also one reason why a Tor Browser user might want to select a new exit relay. This can be done by clicking on the green onion to the left of the browser's address field and clicking “New Identity”.

-   Request a new identity, then refresh the webpage ([whatismyip.com](https://www.whatismyip.com/) or [whatismyipaddress.com](http://www.whatismyipaddress.com/)). The IP address should change.

6. Ask participants to repeat this exercise, until they demonstrate that they can use the Tor Browser Bundle successfully. Then, explain that:
----------------------------------------------------------------------------------------------------------------------------------------------

-   Though Tor encrypts your traffic on its way to the first Tor relay, and while it travels through the Tor network, **it cannot automatically encrypt your connection between the "exit relay" and the website you are visiting.** So, if you are visiting a site that does not support HTTPS, the exit relay operator (who could be *anybody*) can see everything you send and receive. They might know who you are—unless there are hints in the traffic itself, which is not uncommon—but they can see everything else. So, it is still important to use secure, HTTPS Web services. You might want to use the [EFF visualization](https://www.eff.org/pages/tor-and-https) to help explain this concept.

-   In order to take advantage of Tor's anonymity and circumvention properties, you must launch the Tor Browser Bundle and **use the special version of Firefox that comes with it.** Your other browsers (such as Google Chrome, Firefox or Internet Explorer) will not automatically use the Tor network.

-   Unlike with a VPN, non-browser Internet traffic (from email clients like Thunderbird and Outlook, for example, or instant messaging programs like Pidgin and Adium) **does not benefit** from Tor's anonymity or circumvention properties. 

-   When using Tor Browser, you might want to visit [check.torproject.org](https://check.torproject.org/) (which is similar to the [whatismyip.com](https://www.whatismyip.com/) website) and **verify that Tor is working.**

-   ​As with all security software, it is important that you **use the latest version of the Tor Browser Bundle.** When Tor Browser opens, the page it displays will tell you if a newer version is available.
    It will not update itself automatically, however, so you will have to do that yourself. See the **[Secure Software Updating](https://www.level-up.cc/leading-trainings/training-curriculum/secure-software-update)** **module here on LevelUp** for supporting training material on this topic.
