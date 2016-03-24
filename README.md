# Scripts used in Tremblay+16, Nature

This repository contains scripts used in the reduction and subsequent analysis of the [ALMA] data used in Tremblay et al. 2016, *Nature*. These scripts must be run with [CASA] version 4.1, in order to ensure complete reproduction of the data cubes presented in this paper (although later versions of CASA will also work, absent this guarantee). 


  - `reduction_script.py` | *used to reduce the raw ASDMs (which you download from the [ALMA Science Archive]) to measurement sets*. 
  - `scriptForFluxCalibration.py` | *called by reduction_script.py*
  - `make_cubes.py` | *images the measurement sets, producing data cubes as well as intensity, velocity, and velocity dispersion maps*. 
  

First, you must obtain the raw data (which will be delivered in ASDM format) from the [ALMA Science Archive] (search for Project Code 2012.1.00988.S). You may then create data products by running `reduction_script.py` and `make_cubes.py` (in that order). Note that running the reduction script will take roughly 24 hours on a reasonably high-end workstation with 64 GB of RAM and a 12 core processor. Machines with fewer cores and/or ram may take (much) longer. 


To run these, start CASA with 
```
casapy
```
and then type (for example)
```
execfile("reduction_script.py")
```

   [CASA]: <https://casa.nrao.edu/casa_obtaining.shtml>
   [ALMA]: <http://www.almaobservatory.org/>
   [ALMA Science Archive]: <https://almascience.nrao.edu/alma-data/archive>