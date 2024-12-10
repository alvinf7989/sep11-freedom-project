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
Onto day 4, I made a coffee bean fall today. So, on day 4 I followed a gravity example from [this Javascript Example](https://kaboomjs.com/play?example=gravity). And that's not the only thing I did. I also made the bean finally be able to jump. Here were the chanegs I put to the code.
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
For the next day, I learned to add an obstacle to my kaboom by following along.


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
