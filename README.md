# MSDS-6372-Project1
Repo for SMU MSDS Applied Statistics (Spring 2019) Project 1

## Team
Joanna Duran, Nikhil Gupta, Max Moro

##	Problem Background: 
*	Semiconductor manufacturing is a variable process and outcomes depending on several factors. 
*	In order to meet target specs, some parameters are controlled by engineers, however some are beyond human control. 
* Challenges
    - Manufacturing process variation leads to output variables varying between a min and max value (typically measured after the manufacturing process – all R&D done – can lead to issues if the variation of output is outside target specs)
    - Not all values can be practically measured (due to time, resource and cost constraints)
*	Can we predict the limits before the integrated circuits are manufactured to preemptively make changes when specs are expected to be out of range?
	Yes, using electrical simulation (+ running Monte Carlo simulations)
	However, this is very resource intensive as each electrical simulation can take several hours
	Alternate: Build a model to predict the performance (min, typ, max) of the output variable 
•	Describe Dataset
o	Variables controlled by engineers: 
	x1 – xn
	values range dependent on variables
•	some are between 1 to 100
•	other are in nano or micro range               
o	Process Variation (beyond human control): stat1 – statn
	Represents various statistical parameters
	Variable values represent the sigma variation around the mean
	Range is from -4 (sigma) to 4 (sigma)
•	Goals:
o	Build a model to predict the statistical variation of the output with respect to the process
	i.e. model needs to include all statistical parameters at a minimum
•	Target accuracy: 
o	+/- 10% required, but +/- 15% would be acceptable also.

