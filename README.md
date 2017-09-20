#  CLAHE (Contrast Limited Adaptive Histogram Equalization) implementation for OpenCV

Requires [OpenCV](http://www.opencv.org) - 2.x or 3.x

A fork and update that is based on my original 2009 code for teaching.

_Pre-dates the inclusion of this filtering approach in the main branch of OpenCV._
---

### History (pre-git):

```
// Original CLAHE implementation by Karel Zuiderveld, karel@cv.ruu.nl
// in "Graphics Gems IV", Academic Press, 1994.
//-----------------------------------------------------------------------------
// Converted to OpenCV format by Toby Breckon, toby.breckon@cranfield.ac.uk
// Copyright (c) 2009 School of Engineering, Cranfield University
// License : LGPL - http://www.gnu.org/licenses/lgpl.html
//-----------------------------------------------------------------------------
// Improved by Shervin Emami on 17th Nov 2010, shervin.emami@gmail.com
// http://www.shervinemami.co.cc/
//-----------------------------------------------------------------------------
// with 64-bit fix added from: Shashank Kulkarni
// by Toby Breckon, toby.breckon@cranfield.ac.uk (May 2013)
//-----------------------------------------------------------------------------
// _this_ git version
// forked from Emami version, updated build etc - toby.breckon@durham.ac.uk
//*****************************************************************************
```

---

### Background:

If I taught you between 2006 and 2013 at [Cranfield University](http://www.cranfield.ac.uk) or [ESTIA](http://www.estia.fr) - this is the CLAHE example from class.

Used for the CLAHE examples in:

 [Dictionary of Computer Vision and Image Processing](http://dx.doi.org/10.1002/9781119286462) (R.B. Fisher, T.P. Breckon, K. Dawson-Howe, A. Fitzgibbon, C. Robertson, E. Trucco, C.K.I. Williams), Wiley, 2014.
 [[Google Books](http://books.google.co.uk/books?id=TaEQAgAAQBAJ&lpg=PP1&dq=isbn%3A1118706811&pg=PP1v=onepage&q&f=false)] [[doi](http://dx.doi.org/10.1002/9781119286462)]

---

### How to build and run:

```
git clone https://github.com/tobybreckon/opencv-clahe.git
cd opencv-clahe
cmake .
make
./adapthistequal
```
---

If you find any bugs report them to me (or better still submit a pull request, please) - toby.breckon@durham.ac.uk

_"may the source be with you"_ - anon.

---

### Known Issues
- the resizing fix inside clahe.cpp for cell sizes that are not multiples of the image size does not work under all cases
