#  Contrast Limited Adaptive Histogram Equalization (CLAHE) for OpenCV

Requires [OpenCV](http://www.opencv.org) - 2.x or 3.x

A fork and update that is based on my original 2009 code for teaching.

_Pre-dates the inclusion of this filtering approach in the main branch of OpenCV._

---

### History (pre-git):

```
// Original CLAHE implementation by Karel Zuiderveld, karel@cv.ruu.nl
// in "Graphics Gems IV", Academic Press, 1994.
//-----------------------------------------------------------------------------
// Converted to OpenCV format interface by Toby Breckon
// Copyright (c) 2009 School of Engineering, Cranfield University
// License : LGPL - http://www.gnu.org/licenses/lgpl.html
//-----------------------------------------------------------------------------
// Improved by Shervin Emami on 17th Nov 2010, shervin.emami@gmail.com
// http://www.shervinemami.co.cc/
//-----------------------------------------------------------------------------
// with 64-bit fix added from: Shashank Kulkarni
// by Toby Breckon, toby.breckon@cranfield.ac.uk (May 2013)
//-----------------------------------------------------------------------------
// this git version - forked from Emami version, Kulkarni fix added,
// updated build etc - toby.breckon@durham.ac.uk
//*****************************************************************************
```

---

### Background:

If I taught you between 2006 and 2013 at [Cranfield University](http://www.cranfield.ac.uk) or [ESTIA](http://www.estia.fr) - this is the CLAHE example from class.

---

### How to build and run:

```
git clone https://github.com/tobybreckon/opencv-clahe.git
cd opencv-clahe
cmake .
make
./adapthistequal [<video_name>]
```
Runs from an optional video file or a connected web camera.

---

### Known Issues
- the resizing fix inside clahe.cpp for cell sizes that are not multiples of the image size does not work under all cases it appears

---

If you find any bugs report them to me (or better still submit a pull request, please) - toby.breckon@durham.ac.uk

_"may the source be with you"_ - anon.
