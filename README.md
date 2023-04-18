# ICCS23Data
Data from our ICCS 2023 paper on using random forests to predict ABM results.

If using this data, please cite `M. Olsen, M. Raunak, D.R. Kuhn. Predicting ABM Results with Covering Arrays and Random Forests. Proceedings of the 2023 International Conference on Computational Science, June 2023.`

## What is the Data?

The data in this repository is the result of running Wilensky's HeatBugs simulation across about 4 million parameter combinations (4,005,551). Each parameter combination was run 4 times with different random number seeds. We used this data to demonstrate that it was feasible to train a random forest machine learning model on a small subset of the data to then predict a larger subset of data.

The parameter combinations were generated using covering arrays, as detailed in the above paper: a 2-way covering array, and 3-way covering array. This data is separated for the purpose of our study, but as they are of the same format with no duplicate parameter combinations they could be combined for a different study.

The data has columns related to the parameters used to run that simulation, and columns of analyzed results.

### Columns Related to Parameters

For this data, the number of agents is always 200. The rest of the parameters for a given run can be found in each row under these columns:

* 'run': for a particular parameter combination, each run of that parameter combination is number 0, 1, 2, or 3. This value is for tracking results, and is not a parameter to the simulation.
* 'min-ideal-temp': minimum ideal temperature for agents
* 'min-output-heat': minimum output level of heat by agents
* 'max-ideal-temp': maximum ideal temperature for agents
* 'max-output-heat': maximum output level of heat by agents
* 'evaporation-rate': the rate of heat evaporation
* 'diffusion-rate': the rate of heat diffusion
* 'random-move-chance': random change that agents will move each time step

We did not create the HeatBugs model. For full description of these parameters, please see the model in NetLogo.

### Columns Related to Results

The main metric in this model is the unhappiness level of agents. Agents are unhappy when the heat in their immediate environment is not in their ideal range. We calculated results across the entire simulation as well as over the final 500 time steps of the simulation.

*   'average': the average unhappiness level across the entire simulation, across all agents
*   'average over 500': the average unhappiness level across the last 500 time steps, across all agents
*   'stdev over 500': the standard deviation of unhappiness across the last 500 time steps, across all agents
*   'min over 500': minimum unhappines level across all agents over the last 500 time steps
*   'max over 500': maximum unhappiness level across all agents over the last 500 time steps

## Data Files

There are two data files in this repository.
