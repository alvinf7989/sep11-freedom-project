# Entry 4
##### 3/10/2025

We are so back with another entry from yours truly, Alvin Frias! In my 4th entry, prepare to hear me talk about my two days that I was working with my Freedom Project because Practice files are over. I even created my own sprite.

## Plan
As we all know, there are no more days to practice your tool because as of March 2025, we should know how to work on our Freedom Project. As you guys know, my idea was a 2D Platformer and what made this different was that the user can move the platforms and just have the sprite jump to avoid any gaps or obstacles.

Before I got to working, I created a plan for my project on MVP & Beyond. The plan was simple and it was to create one level using my ideas of this 2D Platformer. I broke this into 4 steps:
* [x] Create Obstacles using Kaboom (deadline: 3/20)
* [x] Create a Sprite in Photoshop (deadline: 3/8)
* [ ] Make my sprite be interactable by user (deadline: 3/15)
* [ ] Create background (deadline: 4/1)

The first two of these steps are currently done, that's why those two are checked with an x. But I do have steps for beyond MVP:
* Create Background Music using Ableton Live
* Create Unique Obstacles in Photoshop
* Create Background in Photoshop

Yeah, I wanted to use a lot of other apps to put into my project. Now that I'm done with talking about my plan, let's get to those two days on my Freedom Project.

## Working On Project (Day 1)
So on day 1 of working on my project I wrote that I decomposed my plan. Now in the creating process I created three big red square platforms. I put all these platforms in variables because I wanted them to move which we'll get to later on. Here's the properties of all those platforms:
```js
 var movePlatform1 = add([
            rect(104, 104),
            area(),
            outline(4),
            pos(width()/3.5, height()*0.75),
            anchor("botleft"),
            body({ isStatic: true }),
            color(250, 0, 0),
            // move(LEFT, 240),
 ]);
```
The `pos()` alters in every other variable. Now I'll talk about how I made these two platforms move. So what I did was take all three of those variables that represent the platforms and use the `onKeyDown` concept to make them interactable when the user presses the keys "a" (left) & "d" (right). Since I wanted to make the platforms, I use the `.move()` concept to do so with the parameters being `-200` to move left and `200` to move right. These two numbers are always on the first number because in a way it represents x in x & y. This is the code I just explained:
```js
 onKeyDown("a", () => {
		movePlatform1.move(-200, 0)
        movePlatform2.move(-200, 0)
        movePlatform3.move(-200, 0)
})

onKeyDown("d", () => {
		movePlatform1.move(200, 0)
        movePlatform2.move(200, 0)
        movePlatform3.move(200, 0)
})
```
Maybe on the next workday, I can learn to use the y value on `.move()` to make my sprite jump. Speaking of which...
## Working On Project (Day 2)
Another workday on my project was the first day I finally created my sprite. Now unlike my practice tool files, I didn't use a ranodm image to set as a sprite. Instead, I created my own sprite from scratch using Adobe Photoshop. This sprite is a snail that has a colored shell and has legs which have wheels on them. Now I saved this sprite and put it in my freedom project directory. That way I can load my sprite like this:
```js
loadSprite("snailroller", "mysprite.png")
            setGravity(1650)
```
Keep in mind, the 1st value is the what I name the sprite, and the second value is the name of the photo file.

I had to set the gravity to a number that's good enough for the sprite to fall at. Then, I did the same thing with the platforms and put the properties of the sprite in the variable using `add([])`. The property values are like the coffee bean sprite from my practice tool but the `pos()` value is different, see:
```js
            var player = add([
            sprite("snailroller"),
            body({ isStatic: true }),
            pos(width()/2.25, height()/4),
            scale(0.25),
            area(),
            ])
```
This concludes all the current workdays for this blog entry, I hope to see more in the 5th entry.

## EDP
My apologies for how short these workdays were. But, at least we can talk about the Engineering Design Process I'm currently in.

I'm currently in the **Creating** Process where I create my Freedom Project which was a 2D Platformer to begin with. The idea that I had in mind as well from Brainstorming was that the user had to move the platforms and only have the sprite jump to avoid obstacles. Another thing is that I have been testing how it works using `http-server`.

## Skills
**UPDATE on Problem Decomposition**: For Problem Decomposition this was used very efficiently in my plan as it was to simply create one 2D Platformer Level. This plan of course was broken down into four parts and they each have my created deadlines for them. I'll show them again:
* [x] Create Obstacles using Kaboom (deadline: 3/20)
* [x] Create a Sprite in Photoshop (deadline: 3/8)
* [ ] Make my sprite be interactable by user (deadline: 3/25)
* [ ] Create background (deadline: 4/1)

Like I said earlier, two of the steps are already completed. I just need to do two more and complete the level and I'm good to go beyond MVP.

**Creativity**: I was very creative when I created this sprite for my Freedom Project on different software like Adobe Photoshop. I used pixel art to create a snail character and gave it personality by coloring its shell and giving it legs on wheels. I called this sprite "Snailroller".

<hr>

And that just about wraps up our 4th entry. I will try to put more days into my freedom project work. I just have to add more obstacles and then a bakcground and my level is able to go beyond MVP. But until, next time. Bye!


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
