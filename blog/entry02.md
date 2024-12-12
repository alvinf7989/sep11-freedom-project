# Entry 2
##### 12/11/2024

Welcome back to our second blog entry of our Freedom Project. Here, I will talk about how much I tinkered with the tool of Kaboom for the following two days after the end of November. In fact, I'll also be sharing out my goal for this project when January 2025 hits. But without further ado, let's get to Day 5:

## Day 5
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
Which added the sprite, but before the code was when I put in the `setGravity()` method and tinker with the value. This worked, but without the platform the bean just fell off screen. I noticed when I make the gravity value lower, the sprite falls very slowly, but when I made the value higher than 2000, the bean fell faster. After I added the platform, the bean fell safely onto it. Also I had to use `const play =` in order for the bean to jump because without it, everytime I pressed spacebar, it gave me a screen saying that "reallyBean" isn't defined. "reallyBean" is the name of the coffee bean sprite.

## Day 6
On the next day, it was lying on the 10th of December originally, but I also updated it on the 11th. Now that I had my ground placed, I wanted to add an obstacle to it, so I wen t

## My Goal

## EDP

## Skills

## Sources
[The Kaboom Website](https://kaboomjs.com/)

[The Part of the Website I Mostly Followed](https://kaboomjs.com/doc/intro)

[How I made my Bean Jump on a Platform](tool/day5.html)

[How I made my Bean stand on an Obstacle](tool/day6.html)

[My Learning Log](tool/learning-log.md)


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
