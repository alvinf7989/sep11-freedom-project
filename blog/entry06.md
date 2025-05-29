# Entry 6
##### 05/27/2025
This is it people! This is the final blog entry of my Freedom Project. Here I will explain the things I did Beyond MVP to my Freedom Project as well as the presentation and the elevator Expo, which I did not know was the day I started writing this blog entry.

## My Final Touches on Freedom project
Okay, so recently there has been an activity where students from our class walk around our laptops and test out our freedom projects. They would offer feedback which helped me improve. Some students said that in my game, it was not clear of how they would be able to win in it. This is because of the snail's friction issues and that there was no clear instructions.

To improve, I added an `alert()` that tells the users all the instructions they need to win the game and that they "must be strategic". Another thing I did was brighten the color of my green square. I also thought that because of how dark the green square was, it blended in with the background a little bit.

And the final thing I did was put an `alert()` on the left square where it tells the user a tip on how to win the game. The way you have to press and hold these keys are very strategic. The way I did this was by using `onCollide` like I did when making the user win when the snail lands on the green square.

```js
player.onCollide("movePlatformTip", () => {
    alert("When on a red square, press D until the snail is at the back of the red square, press the spacebar to jump & while the snail is mid air, hold a to move the red blocks, so he's at the front of the red square. And then, Rinse & repeat. This way, you can be able to move forward to the green square.")
});
```
This was the final touch of my Freedom Project and that's when I started my presentations.

## My Presentation
So, for my presentation, I had to create a plan on how I should plan out everything. Starting with the hook, I said I would talk about how normal 2d platformers have you moving the character, but never the platforms unlike my 2D Platformer project. In that part of the slides I'd insert 2 mario platformer gifs and a question mark to ask "what If you could move something else?"

That's the hook, but now we get to the product. For this one, I chose to put in a link and place a screenshot of what the user should expect to see when they're about to click on the project.

After the project link slide I put in a few important code screenshots that I thought the audience should mostly know about. These codes were for the following:
* How I made the platforms
* How I made the controls
* How I made the win & lose screens

After all those slides were created I put in a challenging part of my project which was the issue with the snail's friction and the platforms. I put the words "Friction Strategy" to describe how I made this issue a feature of my Freedom Project. After, putting all those slides I finsihed the presentation off with a few takeaways about Consideration. And even though this isn't on the slide, i also said to try and turn your mistakes into unique features on your project.

This wraps up the portions of my presentation. I do feel that when demonstrating the project on a different computer was frustrating because my game wasn't responsive on different screen sizes, or at least it was, but the speed of the platforms weren't fitting right. This was recent feedback. I was also told that I was saying "like" too much, which is a struggle to control. But this is it for all the current feedback; now we get to the expo.

## Elevator Expo
So, this is going to be short because it was just the expo. While I was at an AP Exam on Friday, that was the day that the Elevator Expo information was given. No one told me _anything_ about the Expo being on Monday, so I had to rush to the cafeteria on 1st period and show my project.

So, how I did this was that on my personal laptop, I would show the project screen where the sprite is at the beginning of the game. I'd show visitors & judges how to play my Freedom Project with the A & D keys along with the spacebar. I found this easier, so I can show them how to strategically win the game. Also, I can mention that I used Kaboom.js as the tool. I forgot to mention this in the presentation.

And that is just about it for everything I've done in this freedom Project, It's amazing how we've gone through learning all the basics in Kaboom.js and I like the idea of using special tools like Adobe Photoshop to make the sprite and background and import it in my terminal.

The current problem is that next year, we're supposedly not allowed to use our personal laptops, which makes it harder for students to share creative ideas in special tools only accessed in our personal devices. (seriously the NYCDOE should reconsider).

## Skills

## Sources
[Presentation](https://docs.google.com/presentation/d/1AlaNYsT6wpVIKgw1E3pqW6uN0OmTnKSJNq2D0T91fFk/edit?slide=id.p#slide=id.p)

[Product](https://alvinf7989.github.io/sep11-freedom-project/)


[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)
