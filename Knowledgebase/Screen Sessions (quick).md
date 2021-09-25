# Screen Sessions

This is an example of how screen sessions work in Linux Ubuntu 20.04.

```js
screen -S bot // This creates a NEW screen session called "bot"

screen -r -d bot // This allows you to reconnect to a screen session called "bot"

CTRL + D // This will terminate a screen session when in it

screen -list // View all screens

killall screen // Terminates all screen sessions
```
