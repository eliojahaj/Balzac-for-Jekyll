---
layout: post-no-feature
title:
description: Attention Spam
category: articles

---

Ever so often, I anxiously click on the spam folder of my Bennington College issued Gmail account, both in the hope and fear that I will find something that has ‘slipped through.’ The horror of missing out on something potentially important, can be offset by the child-like joy of opening a ‘surprise egg’ that was somehow within reach, but out of sight. This past year, I began noticing that my unexceptional spam folder was particularly unexceptional: it was home to emails that came from senders that often infiltrated right into my inbox. Newsletters, ticket aggregator websites, clothing stores and meal delivery apps, were likely to be seen both in my spam folder and in my inbox. If these are not what we usually think of as spam (the scam like imposition of the Nigerian prince has perhaps captured the spam imaginary more tightly), then why do they, ever so often make their way into the spam folder? And from the opposite angle, if they are in fact spam that defies this imaginary, why do they pass through the spam filter into my inbox? This tension, located within the confines of my own email records, compelled me to look at the history of spam in greater detail. 

I was guided and compelled to begin with the work of Finn Brunton and honed in on his essay Roar so wildly: Spam, technology and language,  in which he provides a synthesized, yet rich history of spam. Brunton begins by locating the origins of spam within the imaginary of initial internet users ‘locked in basements,’ that “resort[ed] to quoting song lyrics and verbatim Monty Python routines -- of which the most useful is the restaurant
sketch where Terry Jones recites an interminable menu (‘egg, bacon and Spam, egg, bacon, sausage and Spam, Spam, bacon, sausage and Spam…’).” These repetitious movements were useful for early internet chat room users because of the technical ease of their deployment, a simple copy-paste or or use of the up-arrow key. In a sense, this was the inaugurating act of early spammers. However, the tension that endured for generations of spammers to follow was that they could not escape the confines of language. Much like trust was of paramount importance for the establishment of online payment systems in the early days of eBay, spammers had to convince the user at the other end to act — “to reply, click a link, download an attachment.” Spammers were, and in many ays continue to be, the used car salesman of the internet. They both have to call for attention and consequently, compel someone to act. 

Art critic Hito Steyerl has taken up many of Burton’s insights in her 2011 essay Digital debris: Spam and scam. Central to her formulation however, is the concept of digital wreckages, think toxic hardware landfills in China, that at once come embedded with both a material and symbolic reality. This is the main even of the concept of digital debris, that they are both material and immaterial: “it is data-based debris with a tangible physical component.” For her, spam is a digital debris par excellence. Following Brunton’s work, spam calls for attention and tries to convince, but this attention needs to be materialized through a click, i.e. a nervous signal that finds home within the entangled repositories of the net. Another major point of Burton’s upon which Steyerl builds upon is that 80-90% of daily email communications can be categorized as spam (these findings are based on the empirical studies of MessageLabs/Symantec and can vary wildly globally, but without damaging the main point to be articulated here). As such, spam is in no way the exception at the margins of our email communication systems, but rather is their constitutive language. Spam has no coherent definition (nor a need for it), for its definition is always chaining and unravelling as we interact with it. This is part and parcel of why the spam filter fails, for near perfect success can only be achieved through training viz-a-viz the individual user. Moreover, an initial act of ‘agency,’ such as signing for a newspaper, does not account for the ways in which our very own acts of agency come back re-energized to haunt us as spam. 

There are two main points here. Steyerl holds digital spam to be a highly apt symbolic for our subject position in the 21st century: namely, we are these very wreckages. Much like spam is superfluous, everywhere and discardable, human-subject of capitalist post-modernity are very well superfluous and discardable. Not only is God dead, but so is the industrial worker. Our position within the world is that of superfluous populations, easily modulated, discarded and expelled. This is why 80% of email communication comes in the form of spam; this is why spam is the language of the internet at the present moment. The second point comes back in the form of repetition, for all our superfluousness, attention is still an imperative.   “Contemporary electronic spam tries to extract an improbable spark of value from an inattentive crowd by means of inundation.” The formula that renders the Nigerian prince successful has expanded to comprise the whole of the language games of email combinations and more, wiki blogs etc. As such, spam continues to shape us and is shaped by us. Perhaps akin to the functioning of artificial intelligence, it gets smarter as we interact with it, but once in a while it finds itself incapable of escaping the spam folder. These theoretical and empirical observations, which I cannot treat with the full justice they deserve here, have inspired me to look into my own email records and make a quite modest intervention. 

I began by downloading my email records through the Google data archive. This was fairly easy to do, but the resultant filetype was coded within the .mbox format. I then turned to github where I found a script that aided me with the converstion of .mbox files into legible and analyzble .csv files. The repsitory was made available by user jarrodparkes. My resultant .csv was organized under three columns: Subject, Sender and Date & Time received. I had then, data for nealry 2005 emails. I proceded to parse through these emails and designate the ones which I deemed as spam on a fourth column. This was somewhat of a challenging process, for I did not have a coherent defintion of spam and I belived jsutifaibly so, because the lines between spam, marketing and 'non-spam' were presented as ever more arbitrary. I had some guding principles however: emails that called for my specific attention, but that seemed mass generated were a guiding criteria, and moreover if the purpose of these emails was to make me click or soncume in any way they seemed worthy of automatic inclusion. As such, mass generated emails that asked me to attend school events do not fit both criteria, although spam can and does come from real lfie acquintances as well. Moreover, even if had once granted accses to these newsletter or sites, it seems sensible to think of agency as a continuos process of granting a certain right or authority and not an inagurating and endless act. I ended up with around 460 spam emails, about 25% of my initial data set. 

At this point, my intervention is quite modest, leaves room for growth, yet compelled me beacuase of its simple storytelling potential. I went through the subect lines of these emails and extrapolated words or whole phrases that seemed to galvanize my attention towards certain productive ends, such as clikcing, reading, or visiting a website. I sorted the .csv file according ot he sender and then merley compiled on top of each other the results. I ended up with a poem generated by my spam data, as much as by my digital traces past and present, which I call a "Spoem." Although I would very much like to present it as an anmiated narrative story, through which both I and the viewer/reader can understand certain things about my internet history (however modest they might be and they are modest because the data set is small and could even be broken up into shorter "chronolgical poems"). The following and very simple Python script is what I have used to begin the delivery of this poem. 

```
import time

string = """Alert,
Alert!, Alert!!,
Alert!!!,
Alert
Alert!!!"""

for line in string.splitlines():
    print(line)
    time.sleep(0.5)

string = """how to get the most,
discount now,
unique,
just for you,
best of the best,
FINAL HOURS!!,
Welcome to the family!,
Elio, love what you got?,
Now what?,
OWN YOUR CAREER!,
offer is inside!,
LAST DAY!, 
You can't handle the new,
We're UNIQLO. Nice to meet you!,
We're social butterflies, aren't you?,
Can't stop - won't stop - innovating.,
today only,
better together,
worth more than you think,
Get cash,
You're missing out on cash,
protect yourself against fraud,
protect what's yours,
score brownie points with mom,
gift of cash,
Last chance, 
Take your chance,
action required,
Chances to Win,
Raise Awareness,
VIP discount inside,
Don't share,
Scary Discount,
Get paid,
Did you know?,
Are you getting the most,
Last Chance,
come together,
confronting change,
Times of Change,
Final hours!,
it's time to sell,
something's coming, something good,"""
for line in string.splitlines():
    print(line)
    time.sleep(1.7)


string = """How much do you love us?"""
for line in string.splitlines():
    print(line)
    time.sleep(7) 

```

