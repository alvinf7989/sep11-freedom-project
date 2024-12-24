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

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
