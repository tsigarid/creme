# Simulations

Below is a detailed description of the requested configuration of all simulations as extracted from the protocol paper. The purpose of this page is to have everything available in one page, and enriched with answers from potential questions as each model is being set up. Modelers are requested to explicitly document what they have done in the [models page](models.md), even if this repeats information from here. When Earth is mentioned, it means conditions as close as possible to preindustrial, defined as the year 1850. The duration of the spinup will be model-dependent and should be documented, and the equilibrated simulation(s) should be 150 years, unless the 4xCO2 simulation comes to a complete equilibrium earlier. 

## Benchmark (BM)

This is the entry ticket to CREME, and need to be performed by all models. 

* Ocean: Dynamic. If not possible, a Q-flux ocean is also acceptable as long as the heat fluxes are those of Earth. Fixed sea surface temperatures are also acceptable if no ocean calculations of any kind are possible.
* Bathymetry: Earth if dynamic ocean, or whatever the Q-flux ocean configuration uses.
* Sea ice: Dynamic, or thermodynamic if sea ice flow is not possible across grid cells. Prescribed to Earth values if no prognostic calculations are possible.
* Topography: Earth.
* Vegetation: None.
* Land ice: No prescribed glaciers; snow accumulation imitates the cryosphere. The topography of land should resemble that of the top of the Earth's glaciers, so in places with thick glaciers like in Greenland and Antarctica the model surface is where the top of glaciers is.
* Atmosphere: 78.1 % N<sub>2</sub>, 20.9 % O<sub>2</sub>, 0.9 % Ar (if possible; make it N<sub>2</sub> if not).
* Long-lived GHGs: Earth CO<sub>2</sub> (284 ppmv). CH<sub>4</sub>, N<sub>2</sub>O, CFCs set to zero.
* Water vapor: prognostic.
* Ozone and aerosols: Earth.

## Preindustrial (PI)

Only models that can meet these requirements should perform this. The configuration is the same as in benchmark, with the following changes:

* Vegetation: Earth.
* Land ice: Earth.
* Long-lived GHGs: Earth; CO<sub>2</sub> as in benchmark (284 ppmv), CH<sub>4</sub> 808 ppbv, N<sub>2</sub>O 273 ppbv, CFCs as in benchmark (zero).
* Water vapor: as in benchmark.

## 4xCO<sub>2</sub> (4xCO2)

Mandatory simulation for all models. The configuration is the same as in benchmark, with only one change: the CO<sub>2</sub> concentration is 4x that of the benchmark (to 1136 ppmv), and the simulation should be an exact continuation of the model state at the end of the spinup. 
