# Tool Learning Log

## Tool: **Kaboom**

## Project: **tbd**

---

### 9/29/25:
* Looked through [Kaboom's official website](https://kaboomjs.com/doc/setup) documentary
   * Learned that `kaboom()` starts the game
   * Learned how to add movements to kaboom games.
* Played around with the [Kaboom's playground examples](https://kaboomjs.com/play?example=movement)
  * `onKeyDown` allows the website to detect what key you press.
* While playing around, how the keywords work with kaboom sometimes confuses me as it's sort of complicated.
* How do I create objectives for games?
  * Is the objective made by specific coding or is there templates?
* Next steps
  * Probably creating a mini-project game about movement and any side tasks.
  * Look through more specific tutorials for my future main project.

### 11/1/25:
* Implemented Kaboom using CDN:
 ```js
    <script type="module">

// import kaboom.js
import kaboom from "https://unpkg.com/kaboom@3000.0.1/dist/kaboom.mjs";

// initialize kaboom context
kaboom();

// add a piece of text at position (120, 80)
add([
    text("hello"),
    pos(120, 80),
]);

</script>
```
* Tested around with Kaboom's baseplate
  * I added some new features, such as gravity and jumping.
  * I tinkered around with the logic of kaboom, like trying to add restrictions such as not being allowed to jump when in the air.
* While playing around with Kaboom, how the body parts functioned confused me a little bit, as each body part contained different features.
* How would I order the codes?
  * How should the code be worked and ordered?
* Next Steps
  * Temp side tasks project containing each body feature.


### 11/17/25:
* Looked through [Kaboom's official website](https://kaboomjs.com/doc/setup) documentary
  * Started learning about more codes I could use
    * `isGrounded()`, this allows me to check if my sprite is on the platform so it wouldn't do anything against the logics I want such as unable to jump while in the air still.
    * `move()`, this allows me to add movements to my sprite, such as when you are pressing down d it moves you to the right.
      ```js
      const speed = 200;
      onKeyDown("d", () => {
	    bean.move(speed, 0)
      })
      ```
* Played around a bit with adding stuff into my game, it required some actual patient as you are to create objects such as trees yourself using shapes.
* A bit confused on the logics,
  * How does the arrows suh as `=>` work in these statements?
    ```js
    onKeyPress("space", () => {
    if (bean.isGrounded()) {
        bean.jump();
    }
    });
    ```
  * How should I implement the basic JS into Kaboom?
* Next steps
  * Learn and tinker more about codes that could help my game.

### 11/24/25:
* 

<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
