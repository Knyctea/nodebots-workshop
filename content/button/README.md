# Digital Input - Push Button

## Circuit

![Button](http://i.imgur.com/46o9Mb9.png)

## Code

``` js
var five  = require('johnny-five'),
    board = new five.Board(),
    button;

board.on('ready', function () {
  button = new five.Button(8);

  button.on('down', function () {
    console.log('down');
  });

  button.on('hold', function () {
    console.log('hold');
  });

  button.on('up', function () {
    console.log('up');
  });

});
```

## Run

```
$ node button.js
```

### [Go to Next Lesson >>](../servo/)
