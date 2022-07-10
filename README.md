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

![Historical Metrology ODP schema diagram](https://github.com/kulturinformatik/noback/blob/main/HistoricalMetrologyPatternSchema.png?raw=true

## Use case scenario: deprecated measures

The scenario illustrates the type of research problems addressed by scholars in historical metrology. 

A historian studies a geopolitical entity, e.g. the Kingdom of Bavaria around 1850, and tries to identify those dependent entities (cities or territories) where deprecated units of measurement are still in use. The scholar wants to learn whether there exist differences in the level of adoption between places of trade. This transformation of old (traditional) into new (legal) measurement practices is a typical object of study in historical metrology.

## Selected competency questions

| --- | --- |

| CQ1 | Was there a measurement practice using the unit "guz" in Arungabad in 1850 according to source *S*? |

| CQ2 | Which places have "Schiffspfund" as a measurement unit at some time period according at least one source *S*? |

| CQ3 | Do the sources *S1* and *S2* agree on the conversion factors between the different "guz" units used on the Indian subcontinent? |

| CQ4 | For which places in the Kingdom of Bavaria does source *S* report the largest (smallest) number of persisting traditional measurement practices? |

| CQ5 | For which places in the Kingdom of Bavaria does source *S* report measurement practices that are connected by simple unit conversions? |

| CQ6 | Which types of measurement practices on the Indian subcontinent in 1850 have been redefined and bound to the metrological system of a colonial power? |

## Elements of the Historical Metrology pattern

### Practice

A historical practice of measurement is characterized by their *BaseUnit*. A metrological source has to provide at least this piece of information to be considered a witness for the measurement practice (existential axiom). In most cases, the property is also functional. Specializations of the pattern can add a functionality axiom if needed.

Sources refer to measurement practices by means of a *Descriptor* or a combination of descriptors. When a source identifies a practice as the one that measures in "guz" from "Bangalore", it uses a unit descriptor together with a place descriptor.

The *Domain* of a practice specifies a field of application, such as measuring lengths in the trade of cut goods or, being more specific, in the trade of woolen cloth. The component is left unmodeled. It could refer to an ontology of historical craft and trade activities. For many practices, sources attest a local *Convention*, e.g. allowances.

### Decomposition, Aggregation

*Decomposition* and *Aggregation* are mirror concepts that specify how exactly a measurement practice decomposes a unit into subunits or aggregates the unit to a superunit.  An instance of Decomposition (Aggregation) decomposes (aggregates) exactly one *Unit* into *decompNoOfUnits* (*aggregNoOfUnits*) subunits (superunits).

### Transformation

Sources often describe just the status quo at the time of their writing. It is by combining sources from different points in time that a picture of the transformations emerges. This dependence on the application studied explains why it is difficult to come up with a one-size-fits-all model of a *Transformation*. The Historical Metrology pattern refrains from specifying details beyond the fact that a transformation starts from and ends in a *Practice* as expressed by scoped domain and range axioms.

### Unit, Conversion

The Historical Metrology pattern specifies scoped range and scoped domain axioms for the interaction of *Conversion* and *Unit* in order to facilitate the pattern’s reuse with different ontologies for scientific metrology.




