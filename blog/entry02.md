# Entry 2
##### 12/11/2024

Welcome back to our second blog entry of our Freedom Project. Here, I will talk about how much I tinkered with the tool of Kaboom for the following two days after the end of November. In fact, I'll also be sharing out my goal for this project when January 2025 hits. But without further ado, let's get to Day 5:

## Day 4 to 5
Day 5 started on the second of December 2024, this was the first day that I learned to make my coffee bean sprite move. How did I do it? Well I saw [this Javascript Example](https://kaboomjs.com/play?example=gravity) from Kaboom which basically gave the bean the ability to fall. However, I didn't use the whole code because I just wanted to tinker with the gravity at first. So I put the following code:
```js
const play = add([
    sprite("reallyBean"),
	pos(center()),
    scale(0.25),
    area(),
    body(),
])
```
Which added the sprite, but before the code was when I put in the `setGravity()` method and tinker with the value. This worked, but without the platform the bean just fell off screen. I noticed when I make the gravity value lower, the sprite falls very slowly, but when I made the value higher than 2000, the bean fell faster. After I added the platform, the bean fell safely onto it. Also I had to use `const play =` in order for the bean to jump because without it, everytime I pressed spacebar, it gave me a screen saying that "reallyBean" isn't defined. "reallyBean" is the name of the coffee bean sprite. Also, you may be asking, how did you make the platform? Well I simply took this code:
```js
add([
    rect(width(), 48),
    pos(0, height() - 48),
    outline(4),
    area(),
    body({ isStatic: true }),
    color(127, 200, 255),
])
```
and did some tinkering by changing the color values and outline thickness and I'll define some of the functions in here. `body({ isStatic: true })`, will make the obstacle interactable with the coffee bean sprite. (Looks at learning log.) Oops, I think I summarized Day 4 _&_ 5.

## Day 6
On the next day, it was lying on the 10th of December originally, but I also updated it on the 11th. Now that I had my ground placed, I wanted to add an obstacle to it, so I went back to Kaboom after copying my code from day5.html. This was the code that I added:
```js
add([
    rect(48, 64),
    area(),
    outline(4),
    pos(width(), height() - 48),
    anchor("botleft"),
    color(255, 180, 255),
    move(LEFT, 240),
]);
```
This on its own created a platform that moved from left to right, but I did a good old-fashioned thing called tinkering and changed the values as well as uncommenting the `move()` function because I just wanted a platform to go on the ground and have the bean land on it. I did do some changes to the rectangle shape and positioning. For example `pos()` no longer has a complex value, as I gave it a simpler one. After using `http-server` this successfully worked and my bean fell on the obstacle that I created. I also did a small feature and made it so you would press the W key to jump instead of the spacebar.
## My Goal
Now we get to the goal that we all should have by the end of December, as we could be talking about it on the next blog entry. What I plan to have complete by the end of this year is to at least know how to make obstacles and sprites move the way I want to using Kaboom. And if I have enough time, I can try to fully understand all the functions in the Kaboom.js website or make the dinosaur jump type game example as shown in Kaboom.js.
## EDP
I am now fully into the **Researching** Part of the Engineering Design Process. I used a lot of Kaboom.js to learn how to make obstacles and make my coffee bean move from the user control. The thing that I'm wondering is, what do I have to do to get to the Brainstorming part of the process?
## Skills
* **Embracing Failure & Debugging:** When I had these coding issues with the practices on my Kaboom files, I took one step at a time and learned that that one mistake could be helpful for me to learn. For example, when I had an error that my sprite name wasn't defined I learned that I actually forgot to declare a variable called play and set it equal to the added sprite. This enhanced by skill of Debugging as well.
* **Attention To Detail:** While, I noticed some mistakes on my code, it was also because I need to look closely at the codes. That's how I forgot `const play =` in the first place when making my coffee bean sprite work properly when I hit space or w. UPDATE: When I tested `http-server` it was no longer showing the correct rectangle, so I changed my code some more on day6.html. Here's how the code looks now.
```js
add([
     rect(64, 64),
     area(),
     outline(4),
     pos(780, 647),
     anchor("botleft"),
     body({ isStatic: true }),
     color(255, 180, 255),
     // move(LEFT, 240),
 ]);
 ```

I think that wraps this blog entry. If only I could do these as I make progress on my learning log and Freedom Project. If I can do that on the wrteups, surely I can do it on the blog entries. You know what? That's another goal of mine. I do have to say that I've learned a lot with Kaboom, but sometimes that can be difficult, but not if you acquire the skill of embracing failure, debugging and problem decomposition. I have had 6 days of practice with Kaboom, and I want to fond out how I can find ways to practice. At least, Christmas Break is coming, so maybe I can do that then. But until next time. Goodbye & Have a Happy Holiday!
## Sources

[The Part of the Website I Mostly Followed](https://kaboomjs.com/doc/intro)

[How I made my Bean Jump on a Platform](tool/day5.html)

[How I made my Bean stand on an Obstacle](tool/day6.html)

[My Learning Log](tool/learning-log.md)


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
