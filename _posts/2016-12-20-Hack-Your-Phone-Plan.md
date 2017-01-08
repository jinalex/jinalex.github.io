---
layout: post
title: Halving my Phone Bill by Making my Own Phone Plan
categories:
- Tips and Tricks
- Frugal
- Hack
- Twilio
published: true
---

One thing I couldn't bring with me on my trip around the world was my phone number. 

Prior to leaving I had to make a decision about what to do with my plan. With Wind Mobile I had unlimited talk, text, and spotty data for $35 a month. Not bad. But there was no way I would be paying that for the better part of a year just to hold on to a number.

Instead I decided to port my phone to <a href="https://goo.gl/E0KMdb" target="_blank">Twilio</a>. The process was straight forward though it did take a month to complete the port.

1. Create a Twilio Account
2. Submit a port request to Twilio along with documents
3. Nag customer support to speed up your request
4. Begin managing your number on Twilio

This worked well because for a dollar (USD) a month, I get to keep my existing number and I can even continue to view call and text logs for the number on my dashboard on Twilio's website.

![Many Months Later](/images/months-later.jpg)

Now that I'm back, Wind Mobile had <a href="http://www.theglobeandmail.com/report-on-business/wind-mobile-to-become-freedom-mobile-launch-faster-network-in-toronto-vancouver/article32954738/" target="_blank">changed it's name</a> to Freedom Mobile but what didn't change was my number :grinning:. The new problem was my lack of phone plan. Conveniently, Fido was offering a data only plan of 3GB for only $15 (<a href="https://goo.gl/0N3Bf9" target="_blank">limited time offer</a>) and no contract. Unlimited data to 3GB may sound like a downgrade but Fido is far superior in terms of coverage and data speeds making it an improvement from Wind. I also rarely exceed 1.5GB of monthly data so switching from unlimited to 3GB was not an issue&mdash;in fact I find myself using data more now with reliable connection. 

To complete my custom phone plan, I downloaded the VOIP <a href="https://goo.gl/M5AD9Q" target="_blank">Fongo</a> app, for a free Canadian number that can be used with internet connectivity. Fongo allows you to make and receive calls for free but it's $2 extra per month to send texts. Don't worry, there's a way.

But first, I had to link everything together, I followed a couple Twilio guides to forward <a href="https://support.twilio.com/hc/en-us/articles/223179908-Setting-up-call-forwarding" target="_blank">calls</a> and <a href="https://support.twilio.com/hc/en-us/articles/223134287-Forwarding-SMS-messages-to-another-phone-number" target="_blank">texts</a> from Twilio to my Fongo number using TwilML Bins. Finally for the finishing touch I need to be able to send texts from my phone. To do this I took advantage of the REST API exposed by Twilio and installed an <a href="https://play.google.com/store/search?q=http%20client&c=apps" target="_blank">HTTP Client</a> on my phone. After looking over the <a href="https://www.twilio.com/docs/api/rest/sending-messages">documentation</a> for sending a text, I formulated a POST request on my HTTP Client app and with that I had a working phone plan.

Admittedly I could have just stopped at Fongo and ported my number from Twilio to Fongo ($25 porting fee) but $1 USD and $0.0075 per text (using messaging apps more than texting now) is cheaper than $2 a month. Or maybe I just wanted to see how far I could go with my hacked together phone plan. For usability sake, I would recommend saving yourself the trouble and port over to Fongo completely.

**Before**
Unlimited Smartphone Plan from Wind
$40 + Tax


**After**
High Speed 3GB Data Only Plan from Fido
$15 + Tax

Twilio Number
$1 USD

Twilio Text
$0.0075 USD per text ($1 gets you 133 texts)

Unlimited Calls, Voicemail, Receive Texts from Fongo
Free

Satisfaction from Unnecessarily Complicating my Phone Plan to Save on my Phone Bill
\**Priceless*\*
