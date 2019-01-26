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
    - An example can be seen below. Each horizonatal line is a single output and can have a typical, a maximum and a minimum value. As see in this example, not all values are populated.
    - ![Example outputs](Images/egStatVarSemiconductor.png?raw=true "Title")
*	Can we predict the limits before the integrated circuits are manufactured to preemptively make changes when specs are expected to be out of range?
    - Yes, using electrical simulation (+ running Monte Carlo simulations)
    - However, this is very resource intensive as each electrical simulation can take several hours
    - Alternate: Build a model to predict the performance (min, typ, max) of the output variable 

## Dataset
* Variables controlled by engineers: 
    - x1 – x23
    - values range dependent on variables
        - Some are between 1 to 100
        - other are in nano or micro range               
* Process Variation (beyond human control): stat1 – stat217
    - Represents various statistical parameters
    - Variable values represent the sigma variation around the mean
    - Range is from -4 (sigma) to 4 (sigma)
* Output Variables: y1 - y19
    - Represents various output variables
    
 ## Files
 * features.csv
    - Contains all the features in the data x1-x23 and stat1 - stat217
    - Column JobName is ued to merge with labels (outputs)
    - Note some observations have NA values which will need to be filtered out
* labels.csv
    - Output variables y1 - y19
    - JobName corresponsing to features.csv file
    - NA values will need to be removed
  
## Goals:
* Pick at least 1 output variable 
* Build a model to predict the statistical variation of the output with respect to the process
    - i.e. model needs to include all statistical parameters at a minimum
    - Target accuracy: +/- 10% required, but +/- 15% would be acceptable also
* Build a model to predict the mean value of the output
    - Free to choose any variables of liking from the model
    - Target accuracy: +/- 10% required, but +/- 15% would be acceptable also
  
## Sponsor
* Data has been sponsored and approved for use by Texas Instruments Inc. 


