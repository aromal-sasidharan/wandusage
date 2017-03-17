# wandusage

Installing Wand Version: 0.4.4

pip install wand


dependencies Install


===== MAC ====
```sh
$ brew install freetype imagemagick ghostscript
```
Note : 
when using wand 0.4.4 in python you may see error like below even if you have installed  "imagemagick"
  "ImportError: MagickWand shared library not found.
You probably had not installed ImageMagick library."

in Such Case install an olderversion of imagemagick 

```sh

$ brew install imagemagick@6  //version 6
$ export MAGICK_HOME=/usr/local/opt/imagemagick@6
```



==== example =====
```sh
from wand.image import Image

with Image(filename='./sample.pdf', resolution=300) as img:
    img.alpha_channel = False
    img.save(filename='sample.png')
````