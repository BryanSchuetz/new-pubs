---
title: I Made a Facebook Chatbot (And You Can, Too)
date: 2017-02-14 14:46:00 -05:00
tags:
- Innovation
- Think Piece
Author: Adam Fivenson
---

I've been excited about using chatbots in our work since Facebook's F8 Developer conference last  April, when the company announced that [Messenger would begin to support them](https://techcrunch.com/2016/04/12/agents-on-messenger/).

![pixabey.PNG](/uploads/pixabey.PNG)

> [What is a Facebook chatbot?](https://blog.hubspot.com/marketing/facebook-bots-guide)

Our [Digital Insights](https://dai-global-digital.com/tags/?tag=digital-insights) work in [Indonesia](https://dai-global-digital.com/where-whatsapp-is-just-another-bbm-clone-digital-insights-indonesia.html), [Honduras](https://dai-global-digital.com/mobiles-in-central-america-digital-insights-honduras-part-2.html), and [Palestine](https://dai-global-digital.com/consumer-insights-palestine-e-governance-readiness.html) has shown that Facebook and FB Messenger are hugely popular in the places DAI works. In Indonesia, 77 percent of the people we interviewed said they use Facebook on their phones; in Palestine the number was **95 percent**. In Honduras, 80 percent of our respondents across urban and rural areas said they are Facebook users. If DAI projects want to reach people with messages and services, we must meet people where they already are: on Facebook (and no, not exclusively and not always—if you read our [Indonesia post](https://dai-global-digital.com/where-whatsapp-is-just-another-bbm-clone-digital-insights-indonesia.html), you'll find out a surprising fact about which messaging app is king there (bet you can't guess!). Failing to meet users where they are—in this case, on Facebook—when on-the-ground evidence shows it to be popular would be a major missed opportunity.

<!--more-->

## Why Chatbots?

Chatbots present some distinct advantages as an outreach and engagement tool:

1. As users move [from traditional broadcast social media to private messaging apps](http://www.businessinsider.com/the-messaging-app-report-2015-11), the challenge for the Facebooks of the world (OK, there's only one) is how to stay relevant in a Snapchat world. Facebook's answer, as of April 2014, was to grandfather Messenger in as a replacement to the traditional Facebook private messaging function on mobile phones, pushing users to download Messenger or miss messages. The result is that *a* *lot* of people got Messenger on their phones: more than a billion, in fact. Only WhatsApp rivals Messenger in terms of global uptake (Coincidentally, WhatsApp is also owned by Facebook).

2. As many appmakers have discovered, the need to download and install apps is a barrier to entry for people who don't have the technical capability to do so (maybe their phone came pre-loaded with Facebook and Whatsapp, as it does in many places), access to mobile data, or storage space on the hard drive. As [The Economist duly notes,](http://www.economist.com/news/business-and-finance/21696477-market-apps-maturing-now-one-text-based-services-or-chatbots-looks-poised) "Building apps and promoting them is getting more costly. Meanwhile, users’ enthusiasm is waning, as they find downloading apps and navigating between them a hassle. A quarter of all downloaded apps are abandoned after a single use."

3. Chatbots generally require less bandwidth than loading a typical web page on your phone, and mobile data is expensive! According to [A4AI's 2015 Internet Affordability Report](http://a4ai.org/affordability-report/report/2015/#the_affordability_drivers_index_(adi)), people in some countries pay upwards of 40 percent of their income for mobile access. In that context, unlike ours, every megabyte counts! Lighter data usage lowers the cost of [ordering food](https://www.facebook.com/messages/t/pizzahutus), [checking the weather](https://www.facebook.com/messages/t/hiponcho), or [diagnosing an illness](https://www.facebook.com/HealthTap/).

4. If they're well designed, they can be a more intuitive form of interaction than a web page. From the perspective of a citizen, it's probably easier to chat in your native language with the municipality's chatbot to report a downed telephone pole than it is to visit the municipality, call, or email. From the perspective of a busy municipality, a chatbot would help answer citizens' questions and free up staff to focus on their work.

## Building a Bot

During [App-a-Thon 2016](https://dai-global-digital.com/tags/?tag=appathon-2016) we looked at how [Kik incorporates chatbots](https://dai-global-digital.com/appathon-2016-kik-for-development.html). Immediately after the F8 announcement, I looked for a way to build an FB Messenger chatbot via a simple, graphical user interface (GUI) and easy integration with Facebook. I soon realized that the options available at that time still required some coding ability. Lacking that, I was out of luck.

Today, a year later, the situation is very different. [Chatfuel](http://www.chatfuel.com), [Botsify](https://botsify.com/), and [OnSequal](https://www.onsequel.com/) among others, all make the process of creating a chatbot very simple for the code-challenged, as a recent posting in Social Media Examiner—[How to Create Facebook Messenger Chatbots-](http://www.socialmediaexaminer.com/how-to-create-facebook-messenger-chatbot/)showed. I chose Chatfuel because the tutorial in Social Media Examiner used Chatfuel, but I will eventually try the other two as well for comparison's sake. 

## Siti, Job Search Bot for Indonesia

So what did I build? This chatbot uses natural language (OK it's English, not Bahasa) to make it quick and easy for Indonesians to scan three popular job web sites: 1) [JobStreet](http://www.jobstreet.co.in), 2) [Jobs in Jakarta](http://www.jobsinjakarta), and 3) [JobRank](http://www.jobrank.org/id/). It asks the user to enter a location and job interest, which it turns into a Google query of the above-mentioned job sites. It presents the results in order as a gallery of clickable sliders, which take the user directly to the job listing. Check it out:
<iframe width="560" height="315" src="https://www.youtube.com/embed/LS32bAUT1CM" frameborder="0" allowfullscreen></iframe>
## [Now, Try Siti Live (click here)](https://www.messenger.com/t/1276881939061378)

How did I make Siti? It was surprisingly easy for a non-coder like myself.

1. I linked [Chatfuel](http://www.chatfuel.com) to my Facebook account.

2. I made a [Facebook page](https://www.facebook.com/Siti-1276881939061378) for my chatbot.

3. I learned how to design a simple chatbot by setting up a few choose-your-own-adventure style bots and testing them. I won't embarrass myself by sharing them, but Chatfuel's GUI is excellent, very intuitive, and they have [tutorials](https://help.chatfuel.com/facebook-messenger/) that walk you through the process step-by-step. It's a relatively easy system to learn once you start to play around a bit.

4. I checked Google to figure out which job sites were most popular in Indonesia and built them into my search engine (see step 7).

5. I categorized the jobs and and selected the most popular locations based on what I found on the job sites. This became the job and location taxonomies, as they're presented in the app. I chose to provide categories instead of just leaving those questions open because I wanted popular searches to be easily replicable. I also wanted to ensure that the options' syntax (which becomes the Google search string) was consistent to what the job pages I included used.

6. The most difficult part was setting up the Google search function within the chatbot. But, once again Chatfuel provided an [excellent tutorial](https://help.chatfuel.com/facebook-messenger/plugins/google-search/) on how to handle it.

7. Lots of user testing! I spent a lot of time running through the app to make sure that its responses actually made sense throughout the conversation. I also reviewed the job results provided and removed a few of the pages I had initially included for the search engine because they provided poor results. Finally, I finagled a few friends into trying it out, helping me suss out typos and non-natural language, and general errors in flow. 

## Relevance to ICT4D

Chatbots are a rapidly growing medium as companies, governments, civil society organizations, and businesses come to understand the their potential. Meanwhile, citizens/customers/constituents are becoming more comfortable communicating with the concept of chatbots through Facebook's active efforts to promote successful bots. This rapid confluence of interest and opportunity is the reason why big companies like Barclays are [taking risks and developing chatbots](http://www.bankingtech.com/483822/barclays-africa-to-trial-first-bank-chatbot-in-africa/) for their overseas audiences.

While Siti is simplistic, it's a useful minimum viable product for the type of innovations—grounded in local tech use patterns and easy to design and update—that will likely dominate the nexus of technology and international development during the upcoming years.

*Got an idea for a cool chatbot for international development? Seen a cool chatbot in action? Let us know on [Twitter](http://www.twitter.com/DAIGlobal) or [Facebook](https://www.facebook.com/DAIGlobal/).*