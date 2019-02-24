---
title: "Cyber Security Awareness Training: Passwords"
categories: storyline
excerpt_separator: <!--more-->
---

I made a learning activity about choosing strong, complex passwords at work. It's part of an **E-learning Heroes' challenge** about web objects. I used the web objects to include activities that give feedback about password choices. I had a bit of trouble technically but learned new things about iframes. Read on to see my process I used and a bit of troubleshooting.

Or check out the project: [Get control over your passwords](http://jessicagrosman.ca/passwords101/story_html5.html).
<!--more-->

## Context
The reality is bad passwords let bad people do bad things: steal your identity, break into company's infrastructure, etc.

Cyber Security Awareness Training still covers passwords because people still choose bad passwords.

A coworker had always told me she had a password that was hard to guess. She was sure of it. One day she went home without an important file and I had to log in to her computer. Her password was *BOYFRIENDSNAME123.*

I was gobsmacked.

Password training is difficult because we are talking about preventative measures and  changing habits. And really who likes passwords anyways? 

Most training gives information about password strength and complexity: guidelines and things to avoid. But information alone rarely changes behaviour.

I have thought that interactions focused on increasing feedback could help change password choosing behaviour and habits. 

I had two idea to include: 
1. Password strength analyzer 
2. Pwned Password. 

To really solidify good password making habits, I think we would need to look at how to roll out password managers and help people book time to set them up.

*(If only they would actually listen to us about password managers! They really do make using the internet less frustrating!)*

### Password Strength Analyzer

I noticed during a company wide password manager implementation that people pay  some attention to password strength meters. Participants let out satisfied exclamations when their passwords were evaluated as strong.

There is some debate around password strength analyzers. Security experts argue they  do not accurately calculate complexity. 

For example, an analyzer might evaluate that *Passw0rd* is stronger than *bananacowgrease* because it includes a number and a capital letter. 

But the reality it is actually probably easier to crack *Passw0rd* than bananacowgrease because it uses a common password and a common way to incorporate capitals and special characters.

For technical reasons I couldn't use an analyzer that displayed password entropy, an estimate about how long the password would take to crack. That was the feedback I really wanted, e.g. *Your password would take 5 minutes to crack.*

At least the one I found had a simple UI, the right tone and gave feedback about popular choices. I would love if the password analyzer evaluated people's passwords based on the points on the *Dos and Don'ts slides*, then I wouldn't even need to include them!

### Pwned passwords

[Pwned Passwords](https://haveibeenpwned.com/Passwords) is a project Troy Hunt, a security expert, who started **Have I been Pwned?** and **Pwned Passwords**. 

Hunt collects information (hacked emails and passwords) from data breaches once they have now been made public. I thought the emotional resonance of realizing your password has been part of a data breach might help some people pay attention to the advice about choosing complex passwords and using a password manager. 

Many applications use the **Pwned Password API** to warn their users that their password is a bad choice.

A consideration with this type of activity is how safe it is to send your password to the 3rd party application. I am familiar with **Pwned Passwords** and don't have much worry about that. I kept the analyzer as is for this demo, but I would use a different one if this project goes further.

## Planning

With the above context swirling in my head for some time, I started the text-based story boards to plan the content. I like storyboards because it makes the actual development quicker. Check out [the storyboard pdf](/blog/assets/pdf/password_storyboard.pdf).

I also researched tabbed outlines and decided to go with one similar to [a Storyline Demo](https://www.youtube.com/watch?v=dI0Yy1d1Fb8). 

## Development 

I got hung up on some UX design this time.

The tabs or buttons were hard to get just right (they are still not there 100%). I especially had trouble with colours choices for different states etc. I spent a lot of time fiddling around in Storyline and using the format painter. 

It's stressful to play with the UI at a point when the course was already half created. There is just so much going on: layers, triggers, objects, etc. 

I think I am going to spend a little more time working on templating the design before I dive in. I just downloaded **Adobe Xd** to try out.

### Articulate Storyline - Web Objects

Pwned Passwords and the analyzer are included in the training through Web Objects.

I am not a huge fan of this feature for public websites, but I tried it for an [E-Learning Heroes challenge](https://community.articulate.com/articles/using-web-objects-for-performance-support-in-e-learning). My main frustration was with how web content is displayed. 

When I tested the links I wanted to use, 99% of the time Storyline warned me that the content had to be opened in a new browser window. 

If you open the content in a new browser window it is essentially the same as a hyperlink with *target="_blank"*. 

I really didn't want to include content in new browser windows.

#### The benefits of using a new browser window are few: 

&#10004; The learner can consult the document and not lose their place in the activity.

&#10006; The pop-up window might cause problems with the LMS.

&#10006; The design is not as elegant.

&#10006; The learner is -- at least momentarily -- leaving the world you have created.


#### Troubleshooting why your content won't load in the web object
Many websites block the public from using their content in an iframe for [security reasons](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options). You can check if a site will let you insert the page into a web object in Storyline by inspecting the page with Developer Tools in Google Chrome.

1. To open Developer Tools, press CTRL + SHIFT + I.
1. Click **Network**.
1. Enter "x-frame" in the **Filter** box.
1. If **x-frame** is set to Deny, the content will not load directly on the slide.

In the end, making custom html pages and hosting them on our own server seems like the best option for web objects.
 


