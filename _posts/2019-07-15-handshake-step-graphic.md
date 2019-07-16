---
title: "Visualizing a 3 Way Handshake"
categories: storyline
excerpt: "Playing with ways to make step-by-steps procedures visually appealing in  Articulate Storyline."
---

[Elearning heroes ran a challenge to make a step graphic](https://community.articulate.com/series/e-learning-challenges-complete-list/articles/using-step-graphics-in-elearning). A step graphic visualizes the steps in a procedure so a learner can easily understand the process and how the steps fit together.

I made a 3 step graphic about how computers open a connection over a network. 

![Screenshot from 3 Way Handshake learning activity](/blog/assets/images/handshake_stepper.png)<br>
### [Explore the 3 Way Handshake](http://jessicagrosman.ca/3-way-handshake/story_html5.html)

The steps are presented as a mini-animation. The actual data transmission is abstracted. I wanted to see if there was a way to show the transfer of data without resorting to the usual _Visio-esque_ diagrams. Are you able to imagine how the data is  transmitted without computer and fibre optic network icons?

As the challenge was about visualization, I decided to focus on another design experiments.

### Make the slide area feel bigger

#### Card design
I tried two different layouts to play with making the slides feel bigger letting the learner have more room to breathe. 

![Screenshot from 3 Way Handshake learning activity](/blog/assets/images/cards_l_r.png)<br>

I was inspired by [Mel Milloway's card design](https://www.linkedin.com/pulse/developing-customer-service-game-part-1-melissa-milloway/). She puts the ends of the "next" slide at the edge of the current slide in order to give the illusion that the card continues off the page. I liked how I could change the right and left cards into big next buttons.

![Screenshot from 3 Way Handshake learning activity](/blog/assets/images/syn_card.png)<br>

I also tried making a stack of cards. This is inspired by [Google Primer](https://medium.com/google-design/designing-a-ux-for-learning-ebed4fa0a798). I wish I knew how to put a trigger to let users swipe to get rid of a card! Maybe a future project. Mark it _**to do**_

#### Change the background of the player
In Storyline, the slide background and the player background colors are often different. This cuts down on the feeling of space. It puts a border around the slide and we never get a full screen feeling.

In this project [I changed the background color of the Modern Player](https://community.articulate.com/discussions/articulate-storyline/can-we-change-background-color-in-modern-player-storyline-360) to match the slide background color.

On the first slide or the slide master add an **Execute javascript** trigger for the slide. 

Enter the following code:

Slide background area:

    $(".cs-slide-container").css("background-color", "#005E78");

Player colors (you can see what part of player in first set of brackets):

    $(".top-ui-bg").css("background-color", "#005E78");
    $(".area-primary").css("background-color", "#005E78");
    $(".sidebar-contents").css("background-color", "#005E78");

There are ways to change the background with classic player too. I prefer to do it in Modern player because the menu and controls are less finicky to work with. Remove all buttons and menus if you are going for the full screen effect.
