# fastplotlib-fens2024

Materials for the [`fastplotlib`](https://github.com/fastplotlib/fastplotlib/) talk at FENS Forum 2024. This repo includes installation instructions and the demo notebooks covered in our talk.

For more info on `fastplotlib` see the repo: https://github.com/fastplotlib/fastplotlib/

The demos cover the following topics:
1. Simple introduction to `fastplotlib` - `Images`, `ImageWidget`, and `Lines`
   - plotting simple images, feature changes, image updates, fancy indexing of features
2. Neuroscience using `fastplotlib` 
   - building a complex plot to explore behavioral and calcium imaging data
   - integration of `fastplotlib` with `pynapple`

# Installation Instructions

See the `fastplotlib` repo for [installation](https://github.com/kushalkolar/fastplotlib#installation). 

In order to run the notebooks you will need to have `imageio`. This is not a dependency of `fastplotlib`, but is being used in these demos.

### Install using pip
```
# you will need to install imageio
pip install imageio

# optional, you'll need C compilers
pip install simplejpeg

# fastplotlib with notebook dependencies
pip install "fastplotlib[notebook]"

# pynapple
pip install pynapple
```

# General `fastplotlib` API

### 1. Graphics - objects that are drawn
- `Image`, `Line`, `Scatter`
- Collections - `LineCollection`, `LineStack` (ex: neural timeseries data)
    #### a) Graphic Features
  - Common: `Name`, `Offset`, `Rotation`, `Visible`, `Deleted`
  - Graphic Specific: `ImageVmin`, `ImageVmax`, `VertexColors`, etc.
  #### b) Selectors
  - `LinearSelector` - horizontal or vertical line slider 
  - `LinearRegionSelector` - horizontal or vertical resizable region selection

### 2. Layouts
- `Figure` - a single plot or a grid of subplots 

### 3. Widgets - high level widgets to make repetitive UIs easier
- `ImageWidget`- widget for `Image` data with dims: `xy`, `txy`, `tzxy`
- Sliders, support window functions, etc.

# Docs
For a more in-depth look at our API, please visit our [docs](http://fastplotlib.readthedocs.io/).

# Contributions
`fastplotlib` is a relatively new library, and we are always looking for feedback or help! Please see the [contributing guide](https://github.com/fastplotlib/fastplotlib/blob/main/CONTRIBUTING.md). 

You can also look at our [Roadmap for 2025](https://github.com/fastplotlib/fastplotlib/issues/55) and [Issues](https://github.com/fastplotlib/fastplotlib/issues) for more ideas on how to contribute.
