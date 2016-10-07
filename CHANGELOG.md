# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/) 
and this project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]
### Added
  - `DelaunayTriangulation`: `estimate_normal`, `estimate_normals`, `estimate_gradient`, `estimate_gradients`
  - Added Sibson's c1 interpolant, `DelaunayTriangulation::nn_interpolation_c1_sibson`
  - Added Farin's c1 interpolant, `DelaunayTriangulation::nn_interpolation_c1_farin`
  - trait `ThreeDimensional`
  
### Changed
 - `SimpleEdge` and `SimpleTriangle` have a `DelaunayKernel`
 in their type signatures.

## [0.1.1] - 2016-09-28
### Added
 - Documentaion to all functions and types intended for public use
 - `RTree::lookup_mut(..)`
 - `RTree::contains(..)`
 - `DelaunayTriangulation::handle_mut(..)`
 - `DelaunayTriangulation::lookup_mut(..)`
 - `DelaunayKernel::point_on_edge(..)`
 - `SimpleTriangle::nearest_point_on_edge(..)`
 - types `TwoDimensional`, `HasPosition2D`
 
### Removed
 - `SimpleEdge::point_on_edge(..)`
 - `SimpleTriangle::is_ordered_ccw(..)`

### Fixed
 - Potential crashes when inserting points into a `DelaunayTriangulation`,
 even though `FloatKernel` was used.

### Changed
 - cgmath dependency bumped to 0.12.*
 - DelaunayTriangulations and some primitives now will only work with two
 dimensional coordinates. Using higher dimensions actually yielded unspecified
 results.

## 0.1.0 - 2016-09-23
Initial commit

[Unreleased]: https://github.com/Stoeoef/spade/compare/v0.1.1...HEAD
[0.1.1] https://github.com/Stoeoef/spade/compare/v0.1.0...v0.1.1