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

var request = require('request');
gm(readStream, 'img.jpg')
.write('/path/to/reformat.png', function (err) {
  if (!err) console.log('done');
});

var request = require('request');
var url = "www.abc.com/pic.jpg"

gm(request(url))
.write('/path/to/reformat.png', function (err) {
  if (!err) console.log('done');
});

gm('/path/to/my/img.jpg')
.resize('200', '200')
.stream(function (err, stdout, stderr) {
  var writeStream = fs.createWriteStream('/path/to/my/resized.jpg');
  stdout.pipe(writeStream);
});

var writeStream = fs.createWriteStream('/path/to/my/resized.jpg');
gm('/path/to/my/img.jpg')
.stream('png', function (err, stdout, stderr) {
  var writeStream = fs.createWriteStream('/path/to/my/reformatted.png');
  stdout.pipe(writeStream);
});

var writeStream = fs.createWriteStream('/path/to/my/reformatted.png');
gm('/path/to/my/img.jpg')
.stream('png')
.pipe(writeStream);

var readStream = fs.createReadStream('/path/to/my/img.gpg');
fm(readStream)
.resize('200', '200')
.straem(function (err, stdout, stderr) {
  var writeStream = fs.createWriteStream('/path/to/my/resized.jpg');
  stdout.pipe(writeStream);
});

var readStream = fs.createReadStream('/path/to/my/img.jpg');
gm(readStream)
.size({bufferStream: true}, function (err, size) {
  this.resize(size.width / 2, size.height / 2)
  this.write('/path/to/resized.jpg', function (err) {
    if (!err) console.log('done');
  });
});

var buf = require().readFileSync('/path/to/image.jpg');

gm(buf, 'image.jpg')
.noise('laplacian')
.write('/path/to/out.jpg', function (err) {
  if (err) return handle(err);
  console.log('Created an image from a Buffer!');
});

gm('img.jpg')
.resize(100, 100)
.toBuffer('PNG', function (err, buffer) {
  if (err) return handle(err);
  console.log('done!');
})

gm "convert" "label:Offline" "PNG:-"

gm()
.label('Offline')
.stream();

gm "convert" "-label" "\"Offline\"" "PNG:-"

gm()
.out('label:Offline')
.stream();

gm "convert" "label:Offline" "PNG:-"

gm('img.png').format(function (err, format) {
})

gm('img.png').identify('%m', function (err, format) {
})

gm.compare(path1, path2, [, options], callback)

gm.compare('/path/to/image1.jpg', '/path/to/another.png', function (err, isEqual, equality, raw, path1, path2) {
  if (err) return handle(err);
  
  console.log('The images ware equal: %s', isEqual);
  
  console.log('Actual equality: %d', equality);
  
  console.log(raw);
  
  console.log(path1, path2);
})

gm.compare('/path/to/image1.jpg', '/path/to/another.png', 1.2, function (err, isEqual) {
})

var options = {
  file: '/path/to/diff.png',
  highlightColor: 'yellow',
  tolerance: 0.02
}
gm.compare('/path/to/image1.jpg', '/path/to/another.png', options, function (err, isEqual, equality, raw) {
})

gm.composite(other, [, mask])

gm('/path/to/image.jpg')
.composite('/path/to/second_image.jpg')
.geometry('+100+150')
.write('/path/to/composite.png', function(err) {
  if(!err) console.log("Written composite image.");
});

gm.montage(other)

gm('/path/to/image.jpg')
.montage('/path/to/second_image.jpg')
.geometry('+100+150')
.write('/path/to/montage.png', function(err){
  if(!err) console.log("Written montage image.");
})
```

```
```


