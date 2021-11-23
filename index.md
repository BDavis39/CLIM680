{% include lib/mathjax.html %}

## Briah Davis|CLIM680|Fall 2021

## Introduction
---
Evapotranspiration can be defined as the aggregate of all evaporation from land-surfaces in addition to all transpiration from plants (“Evapotranspiration and the Water Cycle”). This results in a net loss of moisture to the atmosphere from the ground, water table, plants, and even neighboring soil (“Evapotranspiration and the Water Cycle”). It is of great interest because this communal process influences both the land energy and water balances in the atmosphere (Seneviratne et al 129). Consequently, soil moisture, with its direct relationship on evapotranspiration is essential in quantifying these budgets (Seneviratne et al 129). It then stands that understanding the relationship between the governing parameters of soil moisture (and subsequently evapotranspiration) such as temperature, humidity, wind, and vegetation type…etc. facilitates the evaluation of such budgets (Seneviratne et al 129).

#### The Land Energy Balance (for a surface soil layer including vegetation)

![Land Energy Balance](Seneviratne_LandEnergyBalance.png)

$$
\frac{dH}{dt}=R_n-{\lambda}E-SH-G
$$

where, <br>
* $$R_n$$ = Net Radiation <br>
* $${\lambda}$$ = Latent Heat of Vaporization <br>
* E = Evapotranspiration <br>
* SH = Sensible Heat Flux <br>
* G = Ground Heat Flux to deeper layers <br>

and the **Net Radiation** is defined as:

$$
R_n=SW_{in}-SW_{out}-LW_{in}-LW_{out}
$$

(Seneviratne, Sonia I., et al. “Investigating Soil Moisture–Climate Interactions in a Changing Climate: A Review.” Earth-Science Reviews, vol. 99, no. 3–4, Elsevier, May 2010, pp. 125–61, doi:10.1016/J.EARSCIREV.2010.02.004.)

## Data and Functions
---
#### **[SMAP L4](./SMAP.md)**
 
	* 2015-04-01 to 2021-08-31
	* 9km global EASE-Grid 2.0 projection
	* 180˚W to 180˚E/85.044˚N to 85.044˚S
	 * Variables of Interest:
                * Net Radiation  
                        * Longwave Radiation Flux
                        * Shortwave Radiation Flux
                        * Longwave Absorbed Flux
                        * Shortwave Absorbed Flux
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

## Figures
---
Figures Intro.

![Latent Heat Flux Climatology](/Figs/Climo_LHF.png)

Insert Description

![Sensible Heat Flux Climatology](/Figs/Climo_SHF.png)

Insert Description

![Ground Heat Flux Climatology](/Figs/Climo_GHF.png)

Insert Description

## Summary
---
