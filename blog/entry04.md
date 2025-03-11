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
The `pos()` alters in every other variable. Now I'll talk about how I made these two platforms move. So what I did was take all three of those variables that represent the platforms and use the `onKeyDown` concept to make them interactable when the user presses the keys "a" (left) & "d" (right). Since I wanted to make the platforms, I use the `.move()` concept to do so with the parameters being `-200` to move left and `200` to move right. These two numbers are always on the first number because in a way it represents x in x & y.


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
