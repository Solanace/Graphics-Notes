Penn Wu
Mr. Dyrland-Weaver, Period 5
Computer Graphics
Spring 2018

## Table of Contents
| Date     | Aim                                                                  |
| -------- | -------------------------------------------------------------------- |
| 01/31/18 | <a href="#01/31/18">Peering into the Depths of Color</a>             |
| 02/01/18 | <a href="#01/31/18">Peering into the Depths of Color (continued)</a> |

```
Sample header (copy-paste, future self)
## <a name="02/01/18">02/01/18: </a>
```

## <a name="01/31/18">01/31/18: Peering into the Depths of Color</a>

* Color Depth - Amount of data used to represent a single pixel.

| Size   | Color Options                           |
| ------ | --------------------------------------- |
| 1 bit  | 1 color, on \| off                      |
| 2 bit  | 1 color, on \| off, 1 bit for intensity |
| 3 bit  | RGB, on \| off                          |
| 4 bit  | RGB with intensity                      |
| 6 bit  | RGB, _each_ color has its own intensity |
| 3 byte | RGB, each with 256 possible intensities |

#### Other Color Spaces
* RGBA - Red, Green, Blue + Alpha (transparency)
* HSB - Hue, Saturation, Brightness

![alt text](http://www.tomjewett.com/colors/hsb.jpg "Nifty!")

#### Image File Formats
* Raster vs. Vector
	* Vector formats represent images as a series of drawing instructions and are infinitely scalable.
		* SVG (Scalable Vector Graphics)
	* Raster formats represent images as a grid of pixels.
* Uncompressed vs. Compressed (Raster)
	* Uncompressed formats contain data for each pixel.
		* Examples include BMP, TIFF, and RAW files.
	* Compressed formats use a compression algorithm to minimize file size.
	* Lossless vs. Lossy
		* Lossless compression algorithms contain enough information to exactly recreate the original image.
		* Lossless algorithms include PNG and GIF.
		* Lossy compression algorithms don't retain all the details of the original image.
		* The most commonplace lossy algorithm is JPEG.

#### PPM (Portable PixMap)
* Uncompressed raster format.
* Pixel data is represented by RGB triplets in either ASCII or binary.
* All whitespace is equivalent.
* Example:
```
P3
4  3
```

---
