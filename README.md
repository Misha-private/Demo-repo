# Multigrid Graph Filtering on Unstructured Grids (MGGF)

**Standalone Google Colab Notebook — Research and Reproducibility**

## Overview

This repository contains a standalone Google Colab notebook demonstrating the construction, implementation, and numerical evaluation of Multigrid Graph Filtering (MGGF) on an unstructured spherical icosahedral grid.

The notebook accompanies research on multigrid graph-filtering methods for atmospheric modeling, covariance representation, and data assimilation.

The implementation uses a hierarchy of hexagon–pentagon grids and combines graph-filtering operators acting at different spatial resolutions.

## Scientific Objectives

The notebook is designed to:

- Construct spherical icosahedral grids and their multigrid hierarchy.
- Develop graph Laplacians and graph-filtering operators.
- Construct conservative and area-compatible inter-generation transfer operators.
- Verify constant preservation, conservation, positivity, and area-weighted self-adjointness.
- Examine impulse responses at different spatial scales.
- Investigate the approximation of Gaussian correlation structures through multigrid filtering.

## Current Implementation

The current notebook includes:

1. Construction of three spherical grid generations: G0, G1, and G2.
2. Construction and validation of graph-filtering operators.
3. Development of monotone, area-compatible inter-generation interpolation and restriction.
4. Construction and verification of the three-generation MGGF operator.
5. Numerical diagnostics of impulse responses from hexagonal and pentagonal source locations.
6. Exploratory calibration of generation weights against Gaussian reference kernels, including effective-radius constraints.

The calibration experiments are research extensions and should not be interpreted as establishing the accuracy limits of the general MGGF methodology.

## Running the Notebook

The notebook is designed to run in Google Colab using standard scientific Python libraries, including NumPy, SciPy, and Matplotlib.

No external input datasets or Google Drive connections are required.

To reproduce the experiments:

1. Open the notebook in Google Colab.
2. Connect to a Python runtime.
3. Execute the cells sequentially.
4. Examine the numerical diagnostics and generated figures.

## Mathematical Properties

The implementation includes numerical tests of the following properties:

- Constant preservation.
- Conservation of area-weighted integrals.
- Positivity of impulse responses.
- Area-weighted self-adjointness.
- Positive semidefiniteness, evaluated through numerical tests.
- Consistency of inter-generation interpolation and restriction.

These properties are evaluated numerically for the implemented operators and configurations.

## Development Status

**This repository is under active development.**

The current implementation provides a reproducible computational framework for studying MGGF and its mathematical properties.

Future developments may include:

- Additional grid generations to represent a wider range of correlation lengths.
- Improved calibration of multigrid weights and correlation shapes.
- Investigation of spatially varying target correlation lengths.
- Further analysis of coarse-grid representation and inter-generation communication.
- Computational efficiency improvements and GPU implementations.

The results of exploratory experiments may change as the methodology is extended.

## Relationship to the Manuscript

This notebook is intended as a computational companion to the
