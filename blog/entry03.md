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

## Day 9
This day was the first day I worked on my tool in 2025. This was when I learned a new event function: `onKeyDown`. This function allowed the user to commit an action on the sprite whenever a key on your keyboard was held down. This function was what I put in the sprite and it looked something like this:
```js
onKeyDown("left", () => {
    play.move(-100, 0)
})

onKeyDown("right", () => {
    play.move(0, 100)
})
```
In case you forgot, `play` is the name of my coffee bean sprite. What this would do was allow the user to make the sprite move left and right by pressing the left and right arrow keys. The one problem, when I tried `http-server` on my IDE, the sprite only seemed to just move left. Then I said to myself, "I must embrace failure, it's one of my skills." After seeing the values next to `.move()` in `onKeyDown("right")`, I noticed that because both values were zero, the sprite doesn't have the speed to move to the right, when the user holds down on the right key.

This is when I learned that making the first value negative will more likely move left. After changing the first value to be positive 100 an the last value at zero. The sprite successfully moved left and right. In addition, to make things organized, instead of pressing w to make the sprite jump, I had it press the up arrow key to jump. Now, how did I do that? Simple, I just put the word up in the `onKeyPress`.

## UPDATE:
This header means that I will discuss an update on how my FP Goal I stated on Winter Break went. So, my goal was to at least make obstacles and sprites move the way I want to. Well, I was able to make the movement of my sprite the way I want it to by letting the users move the sprite with arrow keys. And remember, when I said I wanted to understand all the functions displayed at Kaboom? Well I learned `onKeyDown` which was a function that lets users make a sprite commit an action whenever a key was held down.

I also said I wanted to use other websites than Kaboom, which makes no sense considering that's my only tool. I should've said I plan to watch Youtube tutorials on Kaboom.

## EDP
I am currently Brainstorming my goals and figuring out what to do to complete them. Previously, I was wondering what I had to do in order to reach the Brainstorm part of the Engineering Design Process and here we are now, where I have no clue if this is the **Brainstorm** part of the process.

## Skills
**Time Management**: This is a skill I actually did use on some days of working on my tool weekly. Sometimes, I work on my tool two times a week. There was a time during Winter Break where I did practice my tool and that was when I was learning how to make `width()` & `height()` the same for my bean when it falls off the starting point in any screen size.

**UPDATE on Embracing Failure**: 

## Sources

[The Part of the Website I Mostly Followed](https://kaboomjs.com/doc/intro)

[How I made the obstacle responsive on any screen](tool/day7.html)

[How I made my sprite responsive on any screen](tool/day8.html)

[How I made my sprite move left & right](tool/day9.html)

[My Learning Log](tool/learning-log.md)


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
