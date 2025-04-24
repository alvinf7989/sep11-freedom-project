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
Even though this wasn't stated on my 

## Sources

[My Learning Log](../tool/learning-log.md)

[My Freedom Project Code](../index.html)

[The Snowy Background](../snailroll-bg.png)

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
