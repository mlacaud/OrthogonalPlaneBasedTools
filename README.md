# OrthogonalPlaneBasedTools

Description
===========
Algorithms implemented thanks to the [DGtal Library](http://dgtal.org/)

On tubular volumes:

* Orthogonal plane estimation
* Pruning algorithm using orthogonal planes
* Recentering procedure
* Curve-skeleton extraction



Quick Build Instructions
========================
The main instructions on linux/unix-based systems are the following:

```shell
git clone https://github.com/fgrelard/MyDGtalContrib.git
cd MyDGtalContrib ; mkdir build ; cd build
cmake ..
make
```

Minimum system requirements: C++11 enabled compiler, [cmake](http://cmake.org), [DGtal](http://dgtal.org/), [boost](http://boost.org) (>= 1.46), [Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page) (>=3.2.0)

In order to compile, the following additional libraries are necessary:
* [QGLViewer](http://libqglviewer.com/) (>=2.5.0)
* Optionally, [ITK](https://itk.org/)

DGtal needs to be compiled with these libraries as well (checkout WITH_QGLVIEWER, WITH_EIGEN, and WITH_ITK options with CMake)


Usage
========================
Executables are located in the build directory. 
They all provide a self-contained description on how to use them, available with the option -h.

* OrthogonalPlaneEstimation and OrthogonalPlaneEstimationWithCurve allow to estimate orthogonal planes directly from the volume and from the curve respectively.
* PruningSkeletonOrthogonalPlanes allow to remove spurious branches on an existing skeleton
* RecenterSkeletonPoints is dedicated to the recentering of an existing non-centered skeleton
* SkeletonOrthogonalPlanes is the skeletonization algorithm on tubular volumes: tracking + postprocessing (junction detection and processing).


Data
========================
The input format data is .vol (DGtal file format). Converters from vol to any ITK format (vol2itk) and from ITK to vol (itk2vol) are available assuming DGtal has been compiled with ITK.
The data folder contains the data which has been used to generate and compare the skeletons at (https://fgrelard.github.io/GeometryTubularOrgans/#).
