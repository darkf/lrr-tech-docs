# Textures

The game stores textures for [models](Models.md) as 8-bit paletted [BMPs](https://en.wikipedia.org/wiki/BMP_file_format).

They do not support an alpha channel, so alpha is done in one of two ways:

- Chroma keying by filename
- Additive blending through the LightWave surface

## Chroma Keying

In this method, the filename of the BMP itself indicates the color used for transparency.

The files are named in the format `A###_foo.BMP` where `###` is a 3-digit number which corresponds to an index into the BMP's color palette. <sup>[1](#note1)</sup> <sup>[2](#note2)</sup>
That color is then considered transparent in the BMP.

## Additive Blending

For the more subtle *transluscency* used in lighting (e.g. in the model `Buildings/Powerstation/spangleY.lwo`), [additive blending](https://en.wikipedia.org/wiki/Blend_modes#Addition) is used. <sup>[2](#note2)</sup>

This is specified in the LightWave surface, in the "Advanced" tab. See the screenshot at <sup>[2](#note2)</sup>.

I am currently unaware of how this is stored in the model itself, although my current hypothesis is that it is in either the `DIFF` or `LUMI` sub-chunks (in `SURF`), when bit 9 ("Additive") is set in the value for the `FLAG` sub-chunk.

## Footnotes

<b name="note1">1</b>. http://www.rockraidersunited.com/topic/6957-invisible-color/?do=findComment&comment=120744

<b name="note2">2</b>. http://www.rockraidersunited.com/topic/7770-a-few-questions-on-modelsanimations/?do=findComment&comment=130304