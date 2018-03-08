# Documents

## Conversion - Pandoc

+ https://pandoc.org/
  + https://pandoc.org/demos.html
+ If you need to **convert files** from one markup format into another, pandoc is your **swiss-army knife**. 
+ HTML -> MD (Markdown)
  + `pandoc test.html -o test.md`
  + or with preserving non-MD HTML-tags: `pandoc test.html -o test.md --parse-raw`
+ EPUB -> PDF
  + `pandoc test.epub --toc -o test.pdf`
  + https://www.reddit.com/r/haskell/comments/26w2f5/pandoc_howto_for_epub_pdf_conversion/
  + https://askubuntu.com/questions/299747/converting-epub-files-to-pdf-format
  + https://github.com/jgm/pandoc/issues/2658

# Imagging

## Conversion - ImageMagic

### Info and install

install: `brew install ImageMagick`

```sh

```

Info

+ https://www.imagemagick.org/script/color.php
+ http://gd.tuwien.ac.at/graphics/ImageMagick/www/color.html

### appending images

```sh
# horizontally join `a.png and `b.jpg` into `c.tif`
convert +append a.png b.jpg c.tif
# verticall join all images into `viber-vs-slack.png`
convert -append cpu.png mem-1.png mem-2.png energy.png viber-vs-slack.png
```

### image info

+ https://www.imagemagick.org/discourse-server/viewtopic.php?t=10674

```sh
identify colabo-logo-url-square.jpg
```



### resizing canvas

#### Solution 1 -border (not working for some cases)

+ http://www.imagemagick.org/Usage/crop/#border

```sh
convert colabo-logo-url-square.jpg -border 10x5 colabo-logo-url-square.jpg
```

```sh
convert colabo-logo-url.jpg  -gravity center -background white -extent 100x80 colabo-logo-url-square.jp
```

an example of making a square image:

```sh
identify colabo-logo-url-square.jpg
# above gives: colabo-logo-url-square.jpg JPEG 780x914 780x914+0+0 8-bit sRGB 116076B 0.000u 0:00.000
# we need to:
echo '(915-780)/2' | bc # gives: 67
# add border of 67 on each size to make the image square
convert colabo-logo-url-square.jpg -border 67x0 -bordercolor white colabo-logo-url-square.jpg
identify colabo-logo-url-square.jpg
# now gives: colabo-logo-url-square.jpg JPEG 914x914 914x914+0+0 8-bit sRGB 127128B 0.000u 0:00.000
```

#### Solution 2 -extent

+ https://stackoverflow.com/questions/1787356/use-imagemagick-to-place-an-image-inside-a-larger-canvas

An example of making a square image:

```sh
identify colabo-logo-url-square.jpg
# above gives: colabo-logo-url-square.jpg JPEG 780x914 780x914+0+0 8-bit sRGB 116076B 0.000u 0:00.000
# we need to make it 914x914
convert colabo-logo-url.jpg  -gravity center -background white -extent 915 colabo-logo-url-square.jpg
# it centered image and added white at the empty space of a new canvas 915(x915)
identify colabo-logo-url-square.jpg
# now gives: colabo-logo-url-square.jpg JPEG 914x914 914x914+0+0 8-bit sRGB 127128B 0.000u 0:00.000
```



