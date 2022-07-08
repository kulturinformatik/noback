# The Historical Metrology ontology design pattern

This repository contains material on the Historical Metrology ontology design pattern created 
in the Digital Noback project.

## Overview

The Historical Metrology pattern provides a solution for the problem of separately describing
measurement practices for which historical sources document independent uses (e.g. foot vs. ell).
*Practice*, *Transformation*, *Unit*, and *Conversion* are the pattern’s main components as can be 
seen from the pattern's schema diagram. *Practice* is modeled in the most detail because it is
the interaction of this component with the other three that creates the intended abstraction.
To put it in a simplified way, *Practice* and *Transformation* capture the historical aspects of
measurement, *Unit* and *Conversion* the physical aspects.

## ODP schema diagram

![Historical Metrology ODP schema diagram](https://github.com/kulturinformatik/noback/blob/main/HistoricalMetrologyPatternSchema.png?raw=true)
