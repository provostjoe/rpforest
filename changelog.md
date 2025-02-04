# Changelog

## [1.4][2019-12-16]
### Changed
- pinned libraries to python2 friendly versions.
- removed stdint include to allow compiling with MSVC

## [1.3][2016-01-22]
### Changed
- all interior nodes of a tree at a given depth now share their hyperplane. This drastically reduces the memory footprint
  of the tree without affecting the guarantees of the data structure (which relies on the hyperplanes being independently drawn
_ between_ the trees in the forest
- this changes the structure of the model pickles, but pickles of older versions should continue to deserialize correctly

## [1.2][2016-01-06]
### Changed
- `fit` can be safely called multiple times on the same model instance.
- `shrink_to_fit` removed, reducing dependency on C++11 stdlib.
- not calling `float` on the Cython version any more.
