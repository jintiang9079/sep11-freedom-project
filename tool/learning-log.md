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
* Looked through [Kaboom's official website](https://kaboomjs.com/doc/setup) documentary
	* Started learning about more codes I could use
		 * `.onCollide`, checks when something is touching or colliding with something.
		* `shake()`, shakes the screen.
    	```js
		bean.onCollide("tree", () => {
   		 addKaboom(bean.pos);
    	shake();
		});
     	```
		* This makes it so that when `bean` collides with `tree` it adds Kaboom effect to `bean`'s position and also shakes the screen.
* I was implementing these codes but it gave me errors as I used `("tree"), () => {` instead of `("tree", () => {`, this confused me a bit, as it would make sense for me to use `("")`.
* Can `bean.` be used as a if statement?
  * What type of code will it allow for the if statement?
* Next steps
	* Keep learning and tinkering more about code that could help my game.

### 12/01/25:
* Looked through [Kaboom's official website](https://kaboomjs.com/doc/setup) documentary
	* Started learning about more codes I could use
   		* `rect`, adds a block into the game.
       		* Could be combined with other codes such as `move`, and more.
           ```js
			add([
       		rect(48, 64),
        	area(),
        	outline(4),
        	pos(width(), height() - 48),
        	anchor("botleft"),
       		color(255, 180, 255),
       		move(LEFT, 240),
       		"tree",
    		]);
           ```
           * This makes it so that the block is anchored to a certain degree on the baseplate, and also moves constantly to the left.
* I was messing around with adding squares into my games and positioning them, but sometimes it ended upside down, so to fix that, I had to use `anchor("botleft")`.
* Can functions, loops and any other external features such as functions be used for these?
  * Can I add more shapes?
* Next steps
	* Keep learning and tinkering more about code that could help my game, and look at more templates of games.
  
 ### 12/08/25:
* Looked through [Kaboom's official website](https://kaboomjs.com/doc/setup) documentary
	* Started learning about more codes I could use
 		* `rand(x, y)`, `wait()`.
     		* `wait()` will wait `x` time, while random will give a random input between `x` and `y`
         ```js
         function spawnTree() {
   		 add([
                rect(48, 64),
        area(),
        outline(4),
        pos(width(), height() - 48),
        anchor("botleft"),
        color(255, 180, 255),
        move(LEFT, 240),
        "tree",
	    ]);
   		 wait(rand(0.5, 1.5), () => {
        spawnTree();
   			 });
			}
         ```
         * This makes it so that the function `spawnTree` will wait between the time 0.5 to 1.5 using `rand` and `wait`, then spawn the tree.
* I was messing around with wait and rand, the `spawnTree` wasn't working as I had put it **outside** of the wait block, so it wasn't waiting; instead, it just spawned trees as normal, so in order to fix this, I had to put `spawnTree()` inside the wait block for it to work.
* How can I utilise `wait` better? Like, how can I make it execute at a specific time?
	*  What's the maximum random number we can get?
 *  Next steps
	* Keep learning and tinkering more about code that could help my game, and look at more templates of games.
<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
