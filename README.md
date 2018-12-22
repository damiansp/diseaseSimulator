# Disease Simulator

This is an agent-based model that simulates the spread and potential persistence of a disease in an animal population (potentially including humans).

The original idea was derived from my work on chronic wasting disease when I was a postdoctoral researcher at the University of Illinois, and the current R code (`/R/old/simDeer.R`) is complete and based on that scenario.  I am currently rewriting the code in Python, with the intention of making it more generalizable.  I may eventually rewrite the R code to make it cleaner as well.

If I get really ambitious, I may one day animate the simulation....


In the case of the original deer model each iteration of the model represents a single year.  In the course of the year, the following events happen, by calling the following methods:

* Initialize population: `Population()` (`Population.__init__()`)
* Plot initial distribution: `Population.plot()`

Iterative sequence begins here:
* Disperse (young leave the mothers): `Population.disperse()`
* Plot new distribution

TODO:
* [ ] Migrate to summer grounds: `Population.migrate('summer')`
* [ ] Plot
* [ ] Calcualate home ranges: `Populaton.calculate_ranges()` [possibly private]
* [ ] Plot ranges
* [ ] Initialize soil matrix (distribution of infectious material in the environment: `Soil()` (`Soil.__init__()`)
* [ ] Soil Plot (Heat map of infectious material): `Soil.plot()`
* [ ] Infect (allow new animals to become infected as a function of distance to infected animals and probability of disease spread): `Population.infect()`
* [ ] Plot showing newly infected animals
* [ ] Infect soil (allow infected animals to leave contaminants in the soil): `Population.infect_soil()`
* [ ] Plot soil status
* [ ] Migrate back to winter grounds: `Population.migrate('winter')`
* [ ] Plot
* [ ] Infect soil
* [ ] Soil plot
* [ ] Animal-to-animal infection
* [ ] Soil-to-animal infection
* [ ] Plot animals
* [ ] Plot soil
* [ ] Mortality: Some animals die as a function of sex, age and disease status (`Population.die()`)
* [ ] Plot
* [ ] Subdivide map into discrete units
* [ ] Local mortality: additional deaths as a function of local carrying capacity
* [ ] Reproduction (babies are born): `Population.reproduce()`
* [ ] Plot
* [ ] Advance Time (animals age)
* [ ] Diminish Infectious Material in Soil
* [ ] Soil Plot

--------------------------------------------------------------------------------

Finish the above, the combine into a single command allowing the model to run for an arbitrary number of iterations (with or without plots being output along the way). Initialize data summary tables and track:
* [ ] Demographics
* [ ] Disease Prevalence
* [ ] Soil Matrices
