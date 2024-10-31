# Entry 1
##### 10/28/2024

Hello everyone! Welcome to my first blog entry for my next **Freedom Project!** For those of you that don't know, we did something like this in our last Freedom Project back in SEP10 where we wrote blog entries for our Freedom Project. In this entry, we wil talk about how I tinkered with my tool.

## My Tool
Before we talk about the tool I chose, we have to go back to the context we had. Before we were assigned blog entries, we were already given a tool and idea to make out of a tool and Javascript. I chose to make a 2D Platformer using the tool: **Kaboom.js**. So far, on [my Learning Log](tool/learning-log.md), I took 2 days to log in my activity with the tool. And if you look at the date I did these logs in, they don't look that good as my recent log was almost a month from the first log. Now since we have the whole week to finish this entry, I'm just going to create another log. But that's enough blabbering let's go through my logs.

### Day 1
So, for Day 1 I decided to start off a little easy and just create a simple template from Kaboom. A Kaboom template displays a checkerboard background with a little tint of gray. So the way I did this was by using a CDN which gives me this code
```js
// import kaboom.js
import kaboom from "https://unpkg.com/kaboom@3000.0.1/dist/kaboom.mjs";

// initialize kaboom context
kaboom();

// add a piece of text at position (120, 80)
add([
    text("hello"),
    pos(120, 80),
]);
```
With script type being equal to "module". And that's how mI setup my Kaboom canvas. You may also notice there's a code that adds the text and position of said text. The reasoning for the bracket parenthesis group is undefined yet. What I did was change the text from "hello" to "Hello Javascript!" I also challenged myself by trying the set that text to the center using the `pos()` values.
### Day 2
On to day 2, which I learned to add images to the Kaboom checkerboard template. What I did was save an actual image of a bean and try to put it in my Kaboom template. But first I put that image in my sprites folder. Then, I took that setup from day 1 and added the `loadSprite()` function which loads in the sprite as long as you name it and put the link in the parenthesis.
It looks something like this:
```js
add([
    sprite("real-bean"),
    pos(500, 150),
])
```
Yeah, it's just the `sprite()` function being in action. You also may notice that inside `sprite()` says "real-bean". Yeah, I changed the name from bean to real-bean which works out a lot. You know what? Now that I think about it, the `loadSprite()` functionm is kind of like defining a function and using `sprite()` is like calling that function. I also tried centering the bean sprite that I got by tinkering with the position.
### Day 3
And now we've reached the most recent Day, Day 3. So, in here I added 2 elements to the javascript code from day2.

These values are:
* `color()` Lets you put in colors through RGB Code. (At least that's what I know so far)
* `scale()` Changes the size of an image.

With these two added, I was able to make my Kaboom practice a little more complex. I made a code that allows two bean sprites on top of each other in different colors. Here was how my code looked:
```js

<script type="module">

    // import kaboom.js
    import kaboom from "https://unpkg.com/kaboom@3000.0.1/dist/kaboom.mjs";

    // initialize kaboom context
    kaboom();

    loadSprite("real-bean", "sprites/beans.png")

// add something to screen
add([
    sprite("real-bean"),
    pos(525, 30),
    scale(0.75),
    color(155, 25, 255),
])

add([
    sprite("real-bean"),
    pos(525, 300),
    scale(0.75),
    color(25, 155, 255),
])


    </script>
```
## EDP
My first step of the Engineering Design Process is of course the defining part of the process. However, I'm also using research to figure out how to use Kaboom, so does that mean I'm also on the researching part of the process?
## Skills
The skill(s) I have acquired was **Debugging**, as I learned to tinker with the `pos()` values as well as tinkering with the `loadSprite()` function. Although it may not seem like that, by changing the image and renaming it to something else, I confirmed that I tinkered with this function.
#### Sources
[How I Made Kaboom Template](tool/day1.html)

[How I Put Images In The Template](tool/day2.html)

[My Learning Log](tool/learning-log.md)

[Next](entry02.md)

[Home](../README.md)
