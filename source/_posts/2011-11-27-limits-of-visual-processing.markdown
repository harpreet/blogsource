---
layout: post
title: "Limits of Visual Processing"
date: 2011-11-27 11:18
comments: true
categories: 
---

Normally it's difficult to get to a question and answer it on StackOverflow before it already has plenty of responses, but with some of the less visited StackExchange sites questions last longer.  I came across this one on programmers.stackexchange:   

_**[How much information can a user reasonably process from a UI](http://programmers.stackexchange.com/questions/1877/how-much-information-can-a-user-reasonably-process-from-a-ui)**_  

This happens to be a topic I've done some work on and was able to post an answer before the page was saturated.  

My answer reproduced with minor edits:  

{% blockquote %}
There is research into this topic but it will give you a complex answer. You can increase how much a person can take in from a UI if you use different sensory modalities rather than just one. For example using sights and sounds you may be able to pump more information into a user than using just sight or just sound. There are also findings that suggest that if your user has to really process or think about the inputs there are more significant bottlenecks that are more difficult to avoid even if you cross sensory modalities. Training helps. Expert users can process more but in the typical cases you will run into limits.

But to get down to your question of how fast you can change the display in particular table: You can look into the Psychology literature on the topic of "Attentional Blink" and "Psychological Refractory Period (PRP)" but the general advice that I can give you from that is don't push faster than changes every 500ms for a single watched location. Typical users can need that much time to process even simple single location changing input. If you're doing it continuously 500ms is a speedy but perhaps roughly workable rate. You may be able to push down to 250ms but this will depend on what percentage of your users you're willing to put off. Also if your users are having to scan multiple locations for possible changes you may have to slow down even from a 500ms change rate. This doesn't necessarily mean 1000ms if you have two locations. It's not a linear relationship but the answer for that is going to be more complex and depend a lot more on what your UI looks like exactly.  

{% endblockquote %}

<em>[http://en.wikipedia.org/wiki/Attentional_blink](http://en.wikipedia.org/wiki/Attentional_blink)</em>

Even though this is technically correct information I provided, the answer to go with in a practical setting is: "Complicated. Requires exploratory testing."

