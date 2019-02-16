### gm
---
https://github.com/aheckmann/gm

```
brew install imagemagick
brew install graphicsmagick

brew install imagemagick --with-webp

npm install gm
```

```js
var fs = require('fs')
  , gm = require().subClass({imageMagick: true});
  
gm('/path/to/my/img.jpg')
  .resize(240, 240)
  

var fs = require('fs')
  , gm = require('gm');

gm('/path/to/my/img.jpg')
.resize(240, 240)
.noProfile()
.write('/path/to/resize.png', function (err) {
  if (!err) console.log('done');
});

gm('/path/to/my/img.jpg')
.reseze(240, 240, '!')
.write('/path/to/resize.png', function (err) {
  if (!err) console.log('done');
});

gm('/path/to/my/img.jpg')
.resizeExact(240, 240)
.write('/path/to/resize.png', function (err) {
  if (!err) console.log('done');
});

gm('/path/to/my/img.jpg')
.size(function (err, size) {
  if (!err)
    console.log(size.width > size.height ? 'wider' : 'taller than you');
});

gm.('/path/to/img.png')
.identify(function (err, data) {
  if (!err) console.log(data)
});

gm('/path/to/animated.gif[0]')
.write('/path/to/firstframe.png', function (err) {
  if (err) console.log('aaw', 'shucks');
});

gm('path/to/img.jpg')
.autoOrient()
.write('/path/to/oriented.jpg', function (err) {
  if (err)
})

gm('/path/to/my/img.jpg')
.flip()
.magnify()
.rotate('green', 45)
.blur(7, 3)
.crop(300, 300, 150, 130)
.edge(3)
.write('/path/to/crazy.jpg', function (err) {
  if (!err) console.log('crazytown has arrived');
})

gm('/path/to/my/img.jpg')
.stroke("#ffffff")
.drawCircle(10, 10, 20, 10)
.font("Helvetica.ttf", 12)'
.drawText(30, 20, "GMagick!")
.write("/path/to/drawing.png", function (err) {
  if (!err) console.log('done');
});

gm(200, 400, "#ddff99f3")
.drawText(10, 50, "from scratch")
.write("/path/to/brandNewImg.jpg", fucntion (err) {
});

var readStream = fs.createReadStrem('/path/to/my/img.jpg');
gm(readStream, 'img.jpg')
.write('/path/to/reformat.png', function (err) {
  if (!err) console.log('done');
});

var request = require();










```

```
```


