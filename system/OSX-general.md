# Imagging

## ImageMagic

+ install: `brew install ImageMagick`

```sh
# horizontally join `a.png and `b.jpg` into `c.tif`
convert +append a.png b.jpg c.tif
# verticall join all images into `viber-vs-slack.png`
convert -append cpu.png mem-1.png mem-2.png energy.png viber-vs-slack.png
```

