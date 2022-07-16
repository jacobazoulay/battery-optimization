# Lithium-Ion Battery Charging Schedule Optimization to Balance Battery Usage and Degradation

This work optimizes a lithium-ion battery charging schedule while considering a joint revenue and battery degradation model. The study extends the work of Meheswari et. al. to encourage battery usage/charging at optimal intervals depending on energy cost forecasts. This project utilizes central difference Nesterov momentum gradient descent to come to optimal charging strategies and deal with the non-linearities of the battery degradation model. This optimization strategy is tested against constant, random varied price forecasts and a novel Gaussian process cost forecasting model. Contrary to many other papers regarding battery charging, formulating schedule optimization as a multivariate optimization problem provides meaningful insight to the inherent balance between these two competing objectives.

This is the final project for AA222 Engineering Design Optimization course at Stanford University.

The final paper can be found [here](https://arxiv.org/abs/2205.15440).



## Directory Structure

- **data**: contains AEP.csv file of historical energy consumption data found [here](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption).
- **notebooks**:
	- [charging-optimization.ipynb](https://github.com/jacobazoulay/battery-optimization/blob/main/notebooks/charging-optimization.ipynb "charging-optimization.ipynb"): jupyter notebook containing charging schedule optimization functions and model
	- [energy-price-prediction.ipynb](https://github.com/jacobazoulay/battery-optimization/blob/main/notebooks/energy-price-prediction.ipynb "energy-price-prediction.ipynb"): jupyter notebook containing energy price prediction model
	- [optimization-with-price-prediction.ipynb](https://github.com/jacobazoulay/battery-optimization/blob/main/notebooks/optimization-with-price-prediction.ipynb "optimization-with-price-prediction.ipynb"): jupyter notebook incorporating both charging schedule and price prediction models
- **reference**: relevant motivating research papers

## Sample Results
### Pareto Frontier Curve
![Pareto frontier curve](/assets/images/pareto-frontier.png)

### State of Charge (SOC) vs Prices
![SOC and prices](/assets/images/SOC-and-prices.png)

### Gaussian Process Energy Price Sampling
![Gaussian process sampling](/assets/images/gaussian-process-sampling.png)

### Worst case Charging Schedule using Periodic Kernel
![Worst case](/assets/images/worst-case-SOC.png)