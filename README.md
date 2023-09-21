

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Caveat&size=30&pause=1000&color=F70000&center=true&vCenter=true&width=435&lines=Hellow+I+Am+Hyper+Mod;Let's+Go+Dino+Game+Hack;Useing+Inspect+Element)](https://git.io/typing-svg)

<p align="center">
<img src="https://i.ibb.co/grrwRTk/FB-IMG-1695300469802.jpg" alt="animated" />
</p>

<p align="center">
Don't Froget to follow
</p>

<p align="center">
<a href="https://youtube.com/c/HYPERMOD"><img title="Size" src="https://img.shields.io/badge/Tutorial-Video-green"></a>
</p>

-------

## ```Connect With Me```
<p align="center">
<a href="https://wa.me/94767043432"><img src="https://img.shields.io/badge/Contact Hyper Mod-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
<a href="https://chat.whatsapp.com/DNUr9fAAaTq6YW3SFQHX7Q"><img src="https://img.shields.io/badge/Join Official GC-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
<a href="https://youtube.com/c/HYPERMOD"><img src="https://img.shields.io/badge/Subscribe Hyper Mod-ff0000?style=for-the-badge&logo=youtube&logoColor=ff000000&link=https://youtube.com/c/HYPERMOD" /><br>
</p>

## ```Donate Me```

- [`Binance`](Wa.me/94767043432)

<p align="left">
Send A Massage Get payment Address.
</p>

## ```Read This```

- [`1st Go to Chrome dino game`]
- [`2nd Right click anywhere on the page and select Inspect.`]
- [`3rd Go to Console tab. This is where we will enter the commands to tweak the game.`]

# Setup For Deployment 👇

- Frist go to the dino game [Here](Chrome://dino)

<br>

## Immortality (God mode)
Follow the commands to make the dino un-killable.

We store the original game over function in a variable. This step is **IMPORTANT** if you want to stop the game later and needs to be done before you reset the gameOver function.
```js
var original = Runner.prototype.gameOver
```

Then, we make the game over function empty:
```js
Runner.prototype.gameOver = function(){}
```

#### How to stop?
When you want to stop the game, Revert back to the original game over function. This would only work if you had entered both commands in order for **Immortality**.
```js
Runner.prototype.gameOver = original
```
<br>

<h1 align="center">Or !<br></h1>

<br>

```js
Runner.instance_.gameOver = function(){};
```

```js
Runner.instance_.gameOver = original
```

<br>

## Tweaking Speed
Type the following command in Console and press enter.
You can use any other speed in place of **1000**.

```
Runner.instance_.setSpeed(1000)
```

To go back to normal speed:
```
Runner.instance_.setSpeed(10)
```

<br>

## Setting the current score
Let's set the score to 12345. You can set any other score less than 99999.
The current score is reset on game over.

```js
Runner.instance_.distanceRan = 12345 / Runner.instance_.distanceMeter.config.COEFFICIENT
```

<br>

## Jumping height
You can control how high the dino jumps by using the below function. Adjust the value as necessary.

```js
Runner.instance_.tRex.setJumpVelocity(10)
```

<br>

## Walk in air

<h1 align="center">0 or 10 add you like anything🌸<br></h1>

```js
Runner.instance_.tRex.groundYPos = 0
```

Back to ground:

```js
Runner.instance_.tRex.groundYPos = 93
```

<br>

## Auto-play

This code periodically checks for the closest obstacle (cactus or pterodactyl) and then jumps or ducks based on the obstacle's position.

```js
function dispatchKey(type, key) {
    document.dispatchEvent(new KeyboardEvent(type, {keyCode: key}));
}
setInterval(function () {
    const KEY_CODE_SPACE_BAR = 32
    const KEY_CODE_ARROW_DOWN = 40
    const CANVAS_HEIGHT = Runner.instance_.dimensions.HEIGHT
    const DINO_HEIGHT = Runner.instance_.tRex.config.HEIGHT

    const obstacle = Runner.instance_.horizon.obstacles[0]
    const speed = Runner.instance_.currentSpeed

    if (obstacle) {
        const w = obstacle.width
        const x = obstacle.xPos // measured from left of canvas
        const y = obstacle.yPos // measured from top of canvas
        const yFromBottom = CANVAS_HEIGHT - y - obstacle.typeConfig.height
        const isObstacleNearby = x < 25 * speed - w / 2

        if (isObstacleNearby) {
            if (yFromBottom > DINO_HEIGHT) {
                // Pterodactyl going from above, do nothing
            } else if (y > CANVAS_HEIGHT / 2) {
                // Jump
                dispatchKey("keyup", KEY_CODE_ARROW_DOWN)
                dispatchKey("keydown", KEY_CODE_SPACE_BAR)
            } else {
                // Duck
                dispatchKey("keydown", KEY_CODE_ARROW_DOWN)
            }
        }
    }
}, Runner.instance_.msPerFrame);
```

<br>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Caveat&size=25&pause=1000&color=007FFF&center=true&vCenter=true&width=435&lines=Now+Let's+Go+Change+Custome+Character+And+Map)](https://git.io/typing-svg)

## ```Follow these steps:```

- [`1st Press the space key to start the game.`]
- [`2nd Right click anywhere on the page and select Inspect.`]
- [`3rd Select the tab Elements and click on the grey arrow next to offline-resources.`]
- [`4th Next, two options will be displayed. In the second one, **"offline-resources-2x"**, double-click on the text after **"src="** and the existing code will be highlighted.`]

<h1 align="center">Read This Down image<br></h1>

<p align="center">
<img src="https://i.ibb.co/855vBCZ/hyper-dino-elements-png-change.webp" alt="animated" />
</p>

<h1 align="center">Chose you like any image🌸<br></h1>

## Images add 

**Batman**

```js
https://chromedino.com/assets/batman2x.png
```

**Mario Boss**

```js
https://chromedino.com/assets/offline-sprite-2x-mario.png
```

**Naruto**

```js
https://trex-runner.com/img/offline-sprite-2x-naruto.png
```

**More Images**

[Here](https://trex-runner.com/img/)

<br>