# Simple-CT
This repository aims to provide an easy, python-only access CT projection and reconstruction.

## Coordinate Systems

We define three coordinate systems: the volume index coordinate system `(i, j, k)`, the world coordinate system `(x, y, z)` and the detector index coordinate system `(u, v)`.

By definition, the units of the world system are millimeters (mm), the rotation axis is the z-axis with the origin as iso-center of rotation

The two index coordinate systems describe the discretized Volume of interest (VOI) and projection images by integer coordinates. Both can be anchored in the real world by setting the appropriate offsets and trajectory parameters.


### Projection Matrices

`TODO Describe how to generate matrices from geometry parameters`

### Using DICOM Matrices (Siemens)

`TODO Add Flips and Convention differences to Siemens Geometry`

## Dependencies

To implement the ray-tracing forward and backprojection, we use [Numba](https://numba.pydata.org/numba-doc/latest/cuda/index.html)'s CUDA interface.

## Development

To use Numba's Cuda Programming without a GPU, set this evironment variable `export NUMBA_ENABLE_CUDASIM=1`

## Resources

- Good intro to Numba Cuda: [Open NYU Course](https://nyu-cds.github.io/python-numba/05-cuda/)
