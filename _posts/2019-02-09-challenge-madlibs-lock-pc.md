---
title: "Storyline Challenge: MadLibs - Computer Security"
categories: storyline
---

### Madlibs Challenge
Over at E-Learning Heroes they had [a challenge to use Madlibs](https://community.articulate.com/articles/using-mad-libs-to-create-elearning-word-games?page=1) in an elearning activity. With the original Madlibs, players choose different word types (e.g. adjective, animal) and insert them into sentences without knowing the larger context.

I immediately had a flash when I saw the challenge. I could use it to make a funny little activity about leaving your computer unlocked at work. 

### Security 101
Locking your screen when you step away from your desk is cybersecurity 101. It might be a low hanging fruit in the security world but it turns up again and again at training.

#### Most training includes:
- instructions and regulations not to leave computers unlocked
- spot the mistake activities
- verbal reminders at meetings
- officially sanctioned or vigilante penalties to offenders

The **instructions and regulations** might work with employees who don't like to break rules. Most people seem to zone out and go *"straightforward I know how to do that."*

The **spot the mistake activities** might help people notice when they are in the wrong.

The **verbal reminders**, well people are forgetting to do it. Maybe it helps form the habit?

The **embarrassing penalties** meted out by colleagues? Let's say posting embarrassing status updates or changing their wallpaper or buying the team donuts. [It's popular and social pressure works](https://www.troyhunt.com/40-inappropriate-actions-to-take/), sometimes. But there is also backlash--some employees are demotivated by these antics because they find them cruel and unfair.

### Office Antics - Lock your computer elearning activity
This activity falls into the reminder category. It uses humour and the threat of embarrassment to make a point. Hopefully people can connect the dots.

The first slide invites the learner to fill in the blanks and learn about some office antics.

![The First Slide prompts for words and hopefully piques curiosity](/blog/assets/images/lockscreen1.PNG)


In the second slide it's revealed the person left their computer unlocked and the words they just filled in describe their new computer wallpaper.

![The second slide has the punch (your colleagues are probably more creative) and the reminder](/blog/assets/images/lockscreen2.PNG)

There is also some info about keyboard shortcuts (i.e. a faster way to lock their screen). I didn't start with the information because I don't think the actual issue is a knowledge or skills gap. Instead I wanted to focus on creating interest through creativity and humour. It's a way to help people remember what they are supposed to do.

![Know your keyboard shortcuts: Win+L or CTRL+CMD+Q](/blog/assets/images/screenlock_shortcuts.PNG)

If I took this further I would find some info about what type of bad things have actually happened from unlocked computers and find a way for people to share their creativity with others, maybe through Slack or other corporate instant messaging.

#### EDIT (14/02/2018): 
I tested the game out on a couple people. I was reminded that not everyone fills in forms entirely! So the person who skipped fields was confronted with a confusing story with a bunch of blanks.

I originally thought I would make the text fields required with some conditionals. Then I thought *locked down Submit buttons* and *All fields are required pop-ups* are demotivating. That wasn't the point of this exercise--it's supposed to be fun! 

Instead I decided that if people left input blank I would supply the answers. This way they would see the point and hopefully go back and try themselves. Plus the catch (your colleagues are probably more creative) is amply true in this case. 

It took a little bit of experimenting to be able to supply my own answers if someone didn't fill out the input fields. The way I got it to work was to a trigger on each data entry field. This trigger adjusts the variable to my word choice provided the person left the field blank.

#### How to set up the trigger

**Action**: **adjust variable to**

**Value**: the word you suggest

**Condition: if <%variable%> == to [blank].**

![An example of the trigger I made to fill in blanks for learners](/blog/assets/images/trigger_changevariable.PNG)

I chose to make the change when the person clicked **Submit**. So I had 7 triggers associated with the **Submit** button: 6 triggers to fill in input left blank and one that jumps to the next slide. It is critical to put the 6 triggers before the trigger that jumps to the next slide. Other wise it won't work.


### See the whole project [here](http://jessicagrosman.ca/lock/story_html5.html).



