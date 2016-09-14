# png-to-ico

[![Build Status](https://travis-ci.org/steambap/png-to-ico.svg?branch=master)](https://travis-ci.org/steambap/png-to-ico)

> convert png to windows ico format

Based on [jimp](https://github.com/oliver-moran/jimp):
 An image processing library written entirely in JavaScript for Node, with zero external or native dependencies.  
In other words, this library is written purely in JavaScript, which is great for windows user.  
This library will generate different sizes based on the input png file and output an windows ico file.

## usage
npm script:
```
png-to-ico electron.png > app.ico
```

programming usage:
```JavaScript
const fs = require('fs');
const pngToIco = require('png-to-ico');

pngToIco('electron.png')
	.then(buf => {
		fs.writeFileSync('app.ico', buf);
	})
	.catch(console.error);
```

## Why use png-to-ico?
When I work on an electron project, it's always a nightmare to create ico for windows.  
There're so many options out there like apps that make icon for you, photoshop plugin. But none of them satisfy me requirement.  
I want a JavaScript module that works like the .NET ico tool, which automatically generate different sizes of ico.

## license
[MIT](LICENSE)
