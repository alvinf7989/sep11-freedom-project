# Entry 3
##### 12/19/2024

Hello, and welcome back to another blog entry for my Freedom Project. This is my 3rd entry and what I'll do is go through all the days that I have made progress in, as well as talking about what I did to try and achieve my goal so far.

## Day 7
Onto day 7, I had this issue where the obstacle on my kaboom template would be in a different position depending on what device you are in, that's why I was getting different results from my personal laptop and my chromebook. I paid very close attention to the `pos()` value for this one.
```js
pos(780, 647)
```
The 1st value of the `pos()` value determines which side from left to right the obstacle goes on while the second value determines where in terms of top to bottom the obstacle goes. The problem I discovered on my previous days was the fact that the values will give different results depending on the screen.

Then I got some help from my teacher about how to make the positioning centered for any screen. It's called dividing `width()` by 2 and what this does is finds the middle value for any screen which will also be the quotient from splitting the width in half. Now I put this for my first value, the height which is the second value is still different on my other screens.

So I thought to myself, what if I divide the `height()` by 2 as well? Well, that worked, but the obstacle is now fully in the center when I actually wanted it to touch the ground. So, the next was dividing by 4, that took my obstacle to a higher height. So, I needed help from my teacher to figure out how to make obstacles go down. Turns out, I either have to divide the `height()` by a fraction or multiply it by a decimal. I chose to multiply it by a decimal, which was equivalent to the fraction of 4, 0.75 and this worked successfully because the obstacle was now on the bottom.

I realize that when dividing the height by bigger numbers over 1, it will make the obstacle's height increase up and when dividing the height by 1 over big numbers, it will make the obstacle's height decrease down.

## Day 8
Day 8 was known as the last tinkering day of 2024. But, that doesn't mean this is my final day because I continued in 2025. For this one, while the platform was touching the floor centered on all devices, the same didn't go for the coffee bean sprite. Not to mention, it also disappears or falls off the obstacle when tested in my personal laptop. So, I thought to myself, what if I can just give the `pos()` the same values as the obstacle position value and have `width()` & `height()` values be divided by values that are different from the obstacle positions. Here's how this looks:
```js
const play = add([
    sprite("reallyBean"),
	pos(width()/2.05, height()/4),
    scale(0.25),
    area(),
    body(),
])
```
So, first things first, I divided the height by 4 to make the bean sprite a lot higher than it was before and farther from the obstacle to prevent disappearance or falling off. However, I decided to do more and increase what the `width()` value was being divided by from 2 to 2.05. Afterwards, it was successful and the object landed on the obstacle for any screen.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
