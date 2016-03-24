# Scripts used in Tremblay+16, Nature

This repository contains scripts used in the reduction and subsequent analysis of the [ALMA] data used in Tremblay et al. 2016, *Nature*. These scripts must be run with [CASA] version 4.2, in order to ensure complete reproduction of the data cubes presented in this paper (although later versions of CASA will also work, absent this guarantee). 


  - reduction_script.py | *used to reduce the raw ASDMs (which you download from the [ALMA Science Archive]) to measurement sets*. 
  - scriptForFluxCalibration.py | *called by reduction_script.py*
  - make_cubes.py | *images the measurement sets, producing data cubes as well as intensity, velocity, and velocity dispersion maps*. 
  

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