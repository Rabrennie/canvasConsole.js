# canvasConsole.js
canvasConsole.js is a simple library to add a console to your canvas.

the tilde/hash key opens the console.

####[Live Example](http://rabrennie.github.io/canvasConsole/)

####Functions:

.init(canvas object ,canvas context) : initialises a new WindowsXp object. 

.render() : should be called at the end of your render loop;

.newCommand(string, callback) : creates a new command. String should be the command. Callback is the function that will run when the command is typed.

####Example Usage:

```javascript
<canvas id="c" width="300" height="300"></canvas>
			
		<script src="canvasConsole.js"></script>
		<script>

			var c = document.getElementById('c');
			var ctx = c.getContext("2d")
			var cc = canvasconsole.init(c,ctx);

			cc.newCommand("test", function(s){console.log(s)})

			var render = function()
			{
				this.ctx.fillStyle = "rgba(255,255,255,1)"
				this.ctx.fillRect(0,0, c.width, c.height)
				cc.render()
			}

			window.setInterval(render, 33)
		</script>
```

*Please note this is a work in progress.
