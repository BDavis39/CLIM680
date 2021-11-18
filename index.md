## Briah Davis|CLIM680|Fall 2021

## Introduction
---
#### The Land Energy Balance (for a surface soil layer including vegetation)

![Land Energy Balance](Seneviratne_LandEnergyBalance.png)

\begin{equation*}
\frac{dH}{dt}=R_n-{\lambda}E-SH-G
\end{equation*}

where, <br>
* $R_n$ = Net Radiation <br>
* ${\lambda}$ = Latent Heat of Vaporization <br>
* E = Evapotranspiration <br>
* SH = Sensible Heat Flux <br>
* G = Ground Heat Flux to deeper layers <br>

and the **Net Radiation** is defined as:

\begin{equation*}
R_n=SW_{in}-SW_{out}-LW_{in}-LW_{out}
\end{equation*}

(Seneviratne, Sonia I., et al. “Investigating Soil Moisture–Climate Interactions in a Changing Climate: A Review.” Earth-Science Reviews, vol. 99, no. 3–4, Elsevier, May 2010, pp. 125–61, doi:10.1016/J.EARSCIREV.2010.02.004.)

## Data
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

## Conda Environment
---
Channels and dependencies needed to replicate results can be found [here](./env.md).

## Functions
---

## Results and Analysis
---

## Figures
---

## Summary
---
