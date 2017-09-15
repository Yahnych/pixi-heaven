# pixi-color-transform

WORK IN PROGRESS, IT IS NOT IN WORKING CONDITION YET

Allows to use advanced color modes.

It can affect performance. 
Though what is performance, when you game looks like s@#$? 
Spawn fewer objects but make it prettier!

Just add ".js" file in your build and start using

```js
var sprite = new PIXI.color_transform.SpriteColored();
// good old sprite tint
sprite.color.setLight(0.5, 1.0, 0.5);

// dark tint - new feature
sprite.color.setDark(0.2, 0.2, 0.2);

// change single component, useful for tweening
sprite.color.darkG = 0.1;
```

Or convert PIXI sprite

```js
var sprite = new PIXI.Sprite(someTexture);

// pixi vanilla way, optional
sprite.tint = 0x80ff80;

// activate the plugin!
sprite.convertToColored();
```

Note that if you are using TS, sprite type will be changed

```ts
let coloredSprite : PIXI.color_transform.SpriteColored = sprite.convertColors();
```

## Building

You will need to have [node][node] setup on your machine.

Make sure you have [yarn][yarn] installed:

    npm install -g yarn

Then you can install dependencies and build:

```bash
yarn
yarn build
```

That will output the built distributables to `./bin`.

[node]:             https://nodejs.org/
[typescript]:       https://www.typescriptlang.org/
[yarn]:             https://yarnpkg.com
