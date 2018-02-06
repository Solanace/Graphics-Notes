Penn Wu  
Mr. Dyrland-Weaver, Period 5  
Computer Graphics  
Spring 2018

Note to self: Look at https://github.com/orgs/mks66/invitation

## Table of Contents
| Date  | Aim                                                                        |
| ----- | -------------------------------------------------------------------------- |
| 01/31 | [Peering into the Depths of Color](#0131-peering-into-the-depths-of-color) |
| 02/01 | [Peering into the Depths of Color](#0131-peering-into-the-depths-of-color) |
| 02/02 | [Useful Terminal Commands](#0202-useful-terminal-commands)                 |
| 02/05 | [Bresenham's Line Algorithm](#0205-bresenhams-line-algorithm)              |

```
Sample header (copy-paste, future self)
## <a name="02/06/18">02/06/18: </a>
```

## 02/05: Bresenham's Line Algorithm

* In CS, we need to approximate values of y into integers.
* We don't care about the grid lines, we care about the boxes!
* Each box is represented by a single pixel.
* Instead of quadrants, we use octants.

#### Bresenham's Line Algorithm
* Goal: find the pixels that best approximate a target line.
* Assume that:
	1. (x<sub>0</sub>, y<sub>0</sub>) -> (x<sub>1</sub>, y<sub>1</sub>) ϵ Z
	2. For lines in octant I, 0 < m < 1
	3. x<sub>0</sub> < x<sub>1</sub> (can just swap their values, but make sure you swap the y-values too!)
* Because of these assumptions, we can take any colored pixel and move either right or right and up, never just up (slope is restricted).
* But which of those two is it?
* Find the value of the line at x + 1, and evaluate whether it is above or below (x + 1, y + 0.5).
	* If above, color the upper pixel.
	* If below, color the lower pixel.
	* If on, arbitrarily pick and stick with one.
	
---

## 02/02: Useful Terminal Commands

#### Commands for ImageMagick
* `$ display image.ppm`
* `$ convert image.ppm image.png`

---

## 01/31: Peering into the Depths of Color

**Color Depth** - Amount of data used to represent a single pixel.

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
P3 (file type, P3 is ASCII and P6 is binary)
4 3 (x-y dimensions)
255 (maximum value)
255 0 0  255 0 0  255 0 0  255 0 0
0 255 0  0 255 0  0 255 0  0 255 0
0 0 255  0 0 255  0 0 255  0 0 255
```
### Use the terminal command `convert file.ppm file.png` to compress your work!

---
