# Multi-dimensional arrays with Scipp

## Type

Tutorial (90 mins)

## Abstract

Inspired by xarray, Scipp enriches raw NumPy-like multi-dimensional data arrays by adding named dimensions and associated coordinates. For an even more intuitive and less error-prone user experience, Scipp adds physical units to arrays and their coordinates. Through this tutorial, participants will learn about the basics of modelling their data with the Scipp library and using in built tools in Scipp for scientific data analysis.

One of Scipp's key features is the possibility of using multi-dimensional non-destructive binning to sort record-based "tabular"/"event" data into arrays of bins. This provides fast and flexible binning, rebinning, and filtering operations, all while preserving the original individual records.

Scipp ships with data display and visualization features for Jupyter notebooks, including a powerful plotting interface. Named Plopp, this tool uses a graph of connected nodes to provide interactivity between multiple plots and widgets, requiring only a few lines of code from the user.

Scipp is available via pip and conda and runs on Linux, Mac and Windows.

## Description

In this tutorial we will cover various key features of Scipp, a python library with a C++ core.

During the tutorial we will go through multiple notebooks with hands on exercises.

Part A (30 mins)
- Introduction to general concepts in scipp
- Basic data structures in scipp

Part B (30 mins)
- Binning of data and computation on top of it.
- Tips and tricks of data analysis on top of multi dimensional arrays.

Part C (30 mins)
- Visualizing scipp data with plopp.
- Interop with the wider scientific python ecosystem.
- File I/O.

By the end of the tutorial we hope that participants will be comfortable with using the scipp API to model and analyze their data.

## Notes

The EuroSciPy tutorial will build up on top of our User Guides and our previous introductory tutorials at other workshops.

No setup should be required as we will provide links to binder (or other online notebook service if necessary). The participants should be able to clone the repository and run the tutorial too.

