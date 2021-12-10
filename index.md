{% include lib/mathjax.html %}

## Briah Davis|CLIM680|Fall 2021
## [Assignment Notebook](https://github.com/BDavis39/CLIM680/blob/master/CLIM680_Assignments.ipynb)

## Introduction
---
#### Background

> Evapotranspiration can be defined as the aggregate of all evaporation from land-surfaces in addition to all transpiration from plants (“Evapotranspiration and the Water Cycle”). This results in a net loss of moisture to the atmosphere from the ground, water table, plants, and even neighboring soil (“Evapotranspiration and the Water Cycle”). It is of great interest because this communal process influences both the land energy and water balances in the atmosphere (Seneviratne et al 129). Consequently, soil moisture, with its direct relationship on evapotranspiration is essential in quantifying these budgets (Seneviratne et al 129). It then stands that understanding the relationship between the governing parameters of soil moisture (and subsequently evapotranspiration) such as temperature, humidity, wind, and vegetation type…etc. facilitates the evaluation of such budgets (Seneviratne et al 129).


#### The Land Energy Balance (for a surface soil layer including vegetation)

![Land Energy Balance](Seneviratne_LandEnergyBalance.png)

$$
\frac{dH}{dt}=R_n-{\lambda}E-SH-G
$$

where, <br>
* $$\frac{dH}{dt}$$ = Change of Energy <br>
* $$R_n$$ = Net Radiation <br>
* $${\lambda}$$ = Latent Heat of Vaporization <br>
* E = Evapotranspiration <br>
* SH = Sensible Heat Flux <br>
* G = Ground Heat Flux to deeper layers <br>

and the **Net Radiation** is defined as:

$$
R_n=SW_{in}-SW_{out}-LW_{in}-LW_{out}
$$

#### Koppan Climate Classification

* Areas of interest:
    * High Temperature (Warm)
    * High Humidity (Moist)

## Data
---
#### **[SMAP L4](/SMAP.md)**
 
* 2015-04-01 to 2021-08-31
* 9km global EASE-Grid 2.0 projection
* 180˚W to 180˚E/85.044˚N to 85.044˚S
* Variables of Interest:
	* Net Radiation  
		* Net Downward Longwave Flux
        * Net Downward Shortwave Flux
    * Evapotranspiration           
        * Latent Heat Flux
    * Sensible Heat Flux
    * Ground Heat Flux
	* Soil Moisture

## Conda Environment
---
Channels and dependencies needed to replicate results can be found [here](./env.md).

## Results and Analysis
---

#### Climatologies
<br>
> *Latent Heat Flux*: The following map represents the latent heat flux averages -- calculated from April 2015 to December 2021 -- over the United States and the Caribbean. Latent heat flux depicts the loss of energy due to evaporation and transpiration. As is expected, more evaporation takes place during the warm season when more heating due to solar radiation and more moisture is present. Notably, in all seasons, the Southwest US maintains low LHF values. This is most likely due to the dry state of the region which is limiting the loss of energy. 

![Latent Heat Flux Climatology](/Figs/Climo_LHF.png) 
<br>
> *Sensible Heat Flux*: The following map represents the sensible heat flux averages -- calculated from April 2015 to December 2021 -- over the United States and the Caribbean. Sensible heat flux (SHF) depicts the loss of energy to the atmosphere due to heating from the surface. More heat is transfereed during the warm months as the land is warmer during this period and therefore is able to transfer this heat to the atmospere. A significant feature in this plot is that the pattern from that in. the LHF plot has reversed. For the most part, the Southwest US maintains high SHF values. The high altitude and spare vegetation region allows for a larger land-atmosphere temperature difference that drives the loss of energy.

![Sensible Heat Flux Climatology](/Figs/Climo_SHF.png)
<br>
> *Ground Heat Flux*: The following map represents the sensible heat flux averages -- calculated from April 2015 to December 2021 -- over the United States and the Caribbean. Sensible heat flux (SHF) depicts the loss of energy to the atmosphere due to heating from the surface. More heat is transfereed during the warm months as the land is warmer during this period and therefore is able to transfer this heat to the atmospere. A significant feature in this plot is that the pattern from that in. the LHF plot has reversed. For the most part, the Southwest US maintains high SHF values. The high altitude and sparse vegetation region allows for a larger land-atmosphere temperature difference that drives the loss of energy.

![Ground Heat Flux Climatology](/Figs/Climo_GHF.png)
<br>

#### Composite and Correlation
<br>
> *Region*: Two regions of interest -- one warm and the other moist -- were chosen to calculate the composite and correlation. Warm region, especially during the summer when there is more solar radiation, suggest more evapotranspiration should be taking place due to the increase in energy of water molecules and opening of stoma in plants. On the contrary, moist regions suggest less. evapotranspiration should be taking place. Water is easier to evaporate (or transpire in the case of vegetation) in drier regions as opposed to moist ones. The maps below shows two regions encompassed in colored boxes that will be averages and used for calculating composite and correlation relative to the LHF. The regions were chosen based on the [Köppen Climate Classification](https://www.weather.gov/jetstream/climate_max) maps which divides regions based on their temperature and moisture characteristics.  

![Regional Latent Heat Flux](./Figs/AVG_LHF.png)


> *Latent Heat Flux Composite*: The following map is a composite of the latent heat flux anomolies calculates over the entire region with the averages of the temperature and specific humidity lowest model layer (56-70m). The averages in each box were computed individually then the percentile data was composited with the anomolies of the LHF for the entire region. The maps below shows the results of this calculation. The top row represents the LHF composite with the warm temperature region and the bottom row represents the LHF composite with the moist temperature region.  

![Latent Heat Flux Composite](/Figs/LHF_Composite.png)
* Top Row
    * West looks fairly similar to what we expect in taking the average from the region
    * Top 10% of temperatures depict a strong signal
        * Small region of low value to the East is most likely due to cool temperatures
    * Surrounding temperatures depict high values
        * Most likely due to advection of dry air over moist region
* Bottom Row
    * Unexpected outcome as regional average is not consistent with plot
        * Potentially due to some greater circulation pattern
        
![Correlation with LHF](/Figs/LHF_Corr.png)
* Top
    * Positively correlated
    * More strongly correlated in Northeast
* Bottom 
    * Positively correlated
    * More strongly correlated in the Southwest
    
![Regression](/Figs/LHFSMReg.png)
* Still being analyzed


## Summary
---
        



## References
---

* Data Products/Data SMAP. https://smap.jpl.nasa.gov/data/. Accessed 27 Nov. 2021.
* Description/Mission SMAP. https://smap.jpl.nasa.gov/mission/description/. Accessed 27 Nov. 2021.
* Evapotranspiration and the Water Cycle. https://www.usgs.gov/special-topic/water-science-school/science/evapotranspiration-and-water-cycle?qt-science_center_objects=0#qt-science_center_objects. Accessed 23 Nov. 2021.
* Global Modeling and Assimilation Office Soil Moisture Active Passive (SMAP) Mission Level 4 Surface and Root Zone Soil Moisture (L4_SM) Product Specification Document. http://gmao.gsfc.nasa.gov/pubs/office_notes. Accessed 27 Nov. 2021.
* Reichle, Rolf, et al. Soil Moisture Active Passive (SMAP) Algorithm Theoretical Basis Document Level 4 Surface and Root Zone Soil Moisture (L4_SM) Data Product Revision A. 2014.
* Seneviratne, Sonia I., et al. “Investigating Soil Moisture–Climate Interactions in a Changing Climate: A Review.” Earth-Science Reviews, vol. 99, no. 3–4, Elsevier, May 2010, pp. 125–61, doi:10.1016/J.EARSCIREV.2010.02.004.

