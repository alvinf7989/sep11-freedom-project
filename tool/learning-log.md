# Tool Learning Log

## Tool: **Kaboom**

## Project: **2D Platformer**

---

### 9/30/24: Day 1
* Welcome to Day 1 of the learning log. My tool for the freedom project I'm going to make will be Kaboom. To start off I created an html file and created a fullscreen Kaboom canvas using this screenshot below![](screenshots/screenshot1.png)
After checking using `http-server` it was showing the right thing. I also learned that that's the easier way to get started with setting up Kaboom.

We're in the same day, but I changed the text and position of the text that's shown which is "Hello Kaboom". I tried challenging myself by trying to make the text centered in the middle.
### 10/21/24: Day 2
We are in Day 2 and I'm learning to add images to the kaboom background. How I tinkered with this was that I added an image of an actual bean like this![](sprites/beans.png)
And then I put in the `loadSprite` function which loaded the sprite correctly. Just as long as you put "bean" in the `add[()]` function as well. But the problem was, the bean image was a **fake** png, those evil twerps. Like the last day, I challenged myself by centering the image of the bean. It was a little easier this time.

### 10/31/24: Day 3
So, I took the code from day 2 and added `scale()` and `color()` values to the `add([])` function. Like this:
```js
add([
    sprite("real-bean"),
    pos(525, 300),
    scale(0.75),
    color(25, 155, 255),
])
```
I also cloned this `add([])` and give different `color()`, `scale()`, & `pos()` values for them so the template could show the sprites on each other with different colors like this below ![](screenshots/daythree.png)

### 11/18/24: Day 4
Onto day 4, I made a coffee bean fall today. So, on day 4 I followed a gravity example from [this Javascript Example](https://kaboomjs.com/play?example=gravity). And that's not the only thing I did. I also made the bean finally be able to jump. Here were the changes I put to the code.
```js
const play = add([
    sprite("reallyBean"),
	pos(center()),
    scale(0.25),
    area(),
    body(),
])

onKeyPress("space", () => {
	if (play.isGrounded()) {
		play.jump()
	}
})
```
So, what I did was try adding `area()` and `body()` to `add([])` function. However, it turns out I had to name that a variable like play for the sprite to work properly. You see, originally I was planning on making the bean jump, but when I pressed space, I got an error message saying that "reallyBean" isn't defined. That's why I used `const play =`.

Now, that I added the Gravity to the bean, it fell off screen. Probably because I didn't put the ground yet. I tinkered with the values of `gravity()` by changing them. When I set the value to 200, the bean fell very slow. But when I set the value higher than 2000, the bean fell very fast.

### 12/2/24: Day 5
Ahh, nothing like Day 5 on December. So, I left off with a coffee bean falling off screen because I didn't set the ground yet. Today is the day I do that. I simply took the code from Kaboom to make the ground:
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
First off `rect()` makes a rectangle, `outline()` speaks for itself (it makes an outline) and the `isStatic` that's inside `body({})` makes it so that the platform has no movement and any object that does move will in fact interact with the platform. A way I tinkered this was by uncommenting certain characterisitcs inside the `add([])` like the `body()` and `pos()`. After uncommenting those, my ground was on the top which still lead the coffee bean to fall off screen. Turns out if you include the `body()` and `pos()`, the ground will be normal and be on the bottom.

### 12/10/24: Day 6
For the next day, I learned to add an obstacle to my kaboom by following along. What I did first however was make that object go in the middle, so the bean can stand on top of it. This wasn't my initial plan. The first thing I did was take the code from day5.html and add this code from Kaboom:
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
What this did was make the platform move from right to left. After this, I tinkered with the values and uncommented the `move()` method, so it wouldn't move. But the issue was that the platform was no longer there. It must've had something to do with the position, so I tinkered with the position, by changing it to be at the center. I then afterwards used `body({ isStatic: true })` to make the obstacle interactable with the bean. This was my tinkered code:
```js
add([
     rect(50, 150),
     area(),
     outline(4),
     pos(705, 595),
     anchor("botleft"),
     body({ isStatic: true }),
     color(255, 180, 255),
     // move(LEFT, 240),
 ]);
```
I also changed the `rect()` value and made the rectangle size smaller. Now when this code was placed in `http-server` it showed the rectangle being a block that the coffee bean sprite is standing on.

### 12/16/24: Day 7
We are now on Day 7 and I gotta say I've been having the problem with my results. For some reason whenever I'm using my personal computer to find a result, it isn't the same as my chromebook result. This is the day that I learned something.
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
 Here you'll see a code from my previous day and the problem that I discovered was with the `pos()` values. You see, the first value of the positioning determines which side from left to right the obstacle goes on while the second value determines where in terms of top to bottom the obstacle goes. These both vary depending on what size screen of device you're using. I learned how to make the x value of positioning centered on any screen. To do this, I simply divided the `width()` by 2 because to find the middle value you must divide the wideness of something in half to find the quotient which will be your middle value. After doing this it worked successfully, but the height was different when I tested it on my chromebook. So, I thought what if I divided the `height()` by 2 as well to balance out the height. Well first off, that did work as well, but it was directly at the center and I wanted to be somewhere in the bottom. So I tried dividing by 4, but that got my obstacle higher, so I then thought maybe if I multiply it by the fraction of 4 it will be brought down. This was my code after the changes.
 ```js
 add([
     rect(64, 64),
     area(),
     outline(4),
     pos(width()/2, height()*0.75),
     anchor("botleft"),
     body({ isStatic: true }),
     color(255, 180, 255),
     // move(LEFT, 240),
 ]);
 ```
 This was able to work correctly and go somewhere in the bottom
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
