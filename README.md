# The Historical Metrology ontology design pattern

This repository contains material on the Historical Metrology ontology design pattern created 
in the Digital Noback project.

Historical metrology studies past systems of measurement in contrast to scientific metrology,
which is concerned with measurements in today's sciences and engineering disciplines.
When we shift the perspective from scientific to historical metrology, we move the focus of
attention from units of measurement to practices of measurement, and from the conversion of
units to the transformation of measurement practices.

## Overview

The Historical Metrology pattern provides a solution for the problem of separately describing
measurement practices for which historical sources document independent uses (e.g. foot vs. ell).
*Practice*, *Transformation*, *Unit*, and *Conversion* are the pattern’s main components. 

*Practice* is modeled in the most detail because it is the interaction of this component with 
the other three that creates the intended abstraction. To put it in a simplified way, *Practice* 
and *Transformation* capture the historical aspects of measurement, *Unit* and *Conversion* 
the physical aspects.

The components *Decomposition* and *Aggregation* have a supporting function. They serve to
describe the decomposition of units into subunits and the aggregation of units to superunits
as operations that are distinct from unit conversions.

## ODP schema diagram

![Historical Metrology ODP schema diagram](https://github.com/kulturinformatik/noback/blob/main/HistoricalMetrologyPatternSchema.png?raw=true)

