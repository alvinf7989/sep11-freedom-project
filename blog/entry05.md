# Entry 5
##### 4/21/2025

We are close to an end as I'm writing this 5th blog entry after completing my Freedom Project. Here, I will discuss the three final working days on my Freedom project and discuss how I did.

## Working On Project (Day 3)
Day 3 was when I noticed something off about my sprite. It seems that when I move the platforms using the direction keys (A, D), The sprite can't help, but move a little along with them. This is because of a friction problem involved with the process. I tried looking up every possible solution, but none of them work. In the end, I just ignored it and later used the friction as a method to get to a goal. We'll talk about the goal later.

Right now, I have managed to add two platforms and later removed one, the next day.
```js
var movePlatform4 = add([
            rect(49, 49),
            area(),
            outline(4),
            pos(width()/1.3, height()*0.75),
            anchor("botleft"),
            body({ isStatic: true }),
            color(250, 0, 0),
            // move(LEFT, 240),
 ]);
 ```
 In this platform, one property is different from the other platforms. And _that_ is **Rectangle Size**. In the `rect` value, I made the shape size much smaller than the other platforms, and you'll see why soon.

 Another thing I did was also set a temporary background, for my Freedom Project because later on, I'd use Adobe Photoshop to create my own. For now, I changed the background to a blue-ish green color by using `setBackground()`. I also did some tweaking with the controls of what key the user should press for the snail sprite to jump. It used to be spacebar, but now the user must press 'w' to jump.

 Also because of the friction issue with my sprite, my objective is now different. Instead of moving the platforms while the sprite stands still, the user must try to have the sprite not fall by moving the platforms enough for the snail to move and be able to jump and land on platforms.

## Working On Project (Day 4)
Day 4 was the day I learned to import my own background. First off, in day 3, I added a platform that had the same properties as another platform. That meant they were overlapping. So, I removed that platform and after doing so, I created a unique background to Kaboom using a software called Adobe Photoshop. For the background, I wanted to represent a snowy mountain type background and was successfully able to do so. If you wish to see what this background looked like, check the sources on the bottom.

Now the way I put this background in my project was by using `loadSprite()` function to load something like this:
```js
loadSprite("snow-bg", "snailroll-bg.png")
```
Along with using `add([])` to add the sprite as a background like this.
```js
add([
            sprite("snow-bg"),
            // pos(0, 0),
            // scale(width() / 1000, height() / 1000),
            ]);
```
## Working On Project (Day 5)
This day, wasn't much for me. All I did was tinker with a few features and color code the platforms. First, I changed the stroke of one moving platform. This platform will also move up and down using the function below:
```js
onKeyDown("d", () => {
    movePlatform4.move(0, 200)
})

onKeyDown("a", () => {
        movePlatform4.move(0, -200)
})
```
Another thing I did was color code it by making it green and alsing having a smaller stroke with these properties:
```js
outline(2),
color(0, 100, 0),
```
The reason I made the one square green was because it will represent the finish goal when the user lands on it.

Finally, the last thing I did was fix the properties of the background. It used to show only one mountain top, but I wanted it to show the rest of the mountains. So, I uncommented the `pos(0,0)` and messed around with what the width and height of the `scale()` property would be divided by.
```js
scale(width() / 2000, height() / 1500)
```

## Working On Project (Day 6)
Even though this wasn't stated on my learning log, I have done my final touches on my freedom Project. See, what I did was create two screens and I used new functions called `scene()` & `go("scenename")`. Inside the `scene` function I created a game over screen using conditions for when the sprite would fall off screen. This game over screen was orange and it told the user to refresh the window to start again.
```js
scene("gameover", () => {
    add([
        text("GAME OVER!", { size: 48 }),
        pos(center()),
        anchor("center"),
    ]);

    add([
        setBackground(255, 100, 10),
        text("Refresh to start over", { size: 24 }),
        pos(center().x, center().y + 60),
        anchor("center"),
    ]);
});
```
As seen, I had to add two different `add([])` functions just to place lines of text. I then put this in an `onUpdate()` function which updates the status of anything. I chose my sprite and put an if statement like this.
```js
        if (player.pos.y > height()) {
            go("gameover");
        }
```
The `go()` function sends the user to the scene that's inside the parenthesis.

Now that that was done, I needed to add a congratulations screen for when the user made it to the green square. I used the sae `scene()` and `go()` methods, but instead of using `onUpdate()` to create a conditional for the sprite, I used a `.onCollide()` function. Inside the parenthesis is where you would put the platform the sprite is on and have it do something special when on it. This time, there was no `if` statement because the `.onCollide` function was a conditional on its own. Here's how I used it:
```js
player.onCollide("movePlatform", () => {
    go("congrats");
});
```
In the "congratulations" screen, it was blue and it displayed a line of text saying, "CONGRATULATIONS! You've completed the level!".

And that wraps up my Freedom Project! But, we are not done yet, because I have to adress the EDP I'm in & my Skills.

## EDP
After completing my Freedom Project, I have also been testing it to make sure that it works just like the way I wanted it to. So, now that I have been Testing this project, that means I'm on the **Testing** part of the Engineering Design Process. Now, all that's left is to make some improvements and then communicate the results.

## Skills

* **Growth mindset**: Growth mindset is a new skill that I have obtained. Basically, this skill is when I act patient and am able to ask for help, I used the Growth mindset in my MVP, when trying to fix the friction issue on my sprite when it was on the platforms. Sure, that didn't work, but that was when **Embracing Failure** came in and I used this as I startegic way foor my sprite to go to platforms.

* **How to Google** Now, this one was a little strange because I mostly looked back at Kaboom to look at all the ways to solve these problems with my sprite & platform movements. My question was if this counts as a "How to Google" skill becuase I looked up Kaboom tutorials and how to fix things. Another thing I did on Google was watch a few videos. One thing I should've mentioned earlier was that I watched videos on how to draw a background and add it for Kaboom. I even saw a pixel art tutorial, which helped me create my snail sprite. The video link is in the Sources.

<hr>

And that has just wrapped up my Freedom Project. I do feel that this isn't the final entry because there's still time to improve and present our project to (I assume) Seniors like last time. But thank you for reading the blog entry all the way down and I'll hopefully be here on Entry 6. So, until next time. Bye!

## Sources

[Pixel Art Tutorial](https://www.youtube.com/watch?v=q2IxC0odOkU&t=2s)

[My Learning Log](../tool/learning-log.md)

[My Freedom Project Code](../index.html)

[The Snowy Background](../snailroll-bg.png)

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
