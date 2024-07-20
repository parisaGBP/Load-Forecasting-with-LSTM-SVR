# Load-Forecasting-with-LSTM-and-SVR
Very short term Load Forecasting with LSTM and SVR methods.
# Data:
**Individual Household Electric Power Consumption**

@misc{misc_individual_household_electric_power_consumption_235,
  author       = {Hebrail,Georges and Berard,Alice},
  title        = {{Individual Household Electric Power Consumption}},
  year         = {2012},
  howpublished = {UCI Machine Learning Repository},
  note         = {{DOI}: https://doi.org/10.24432/C58K54}
}
# Description of the problem:
the goal is to predict the "Voltage" based on six features listed blew:
* Global_active_power 	
* Global_reactive_power 	
* Global_intensity 	
* Sub_metering_1 	
* Sub_metering_2 	
* Sub_metering_3

represents the active energy consumed every minute (in watt hour) in the household by electrical equipments.
# Evaluating methods:
![a](https://wikimedia.org/api/rest_v1/media/math/render/svg/92ea807c3147d94e8762772be5d12511f1d55938)

![a](https://wikimedia.org/api/rest_v1/media/math/render/svg/6d689379d70cd119e3a9ed3c8ae306cafa5d516d)

![a](https://wikimedia.org/api/rest_v1/media/math/render/svg/2173f69a3c0192c836e19e9942d875c48621af81)


# LSTM:

**Model Development**

* Model is developed after trying different combinations of Hyperparameters and kernels
* Best optimizer is adam

## Model

 Layer (type)                Output Shape              Param    

 =================================================================
 
 lstm_1 (LSTM)               (None, 50)                11400     
                                                                 
 dense_1 (Dense)             (None, 1)                 51        
                                                                 
### Evaluate model

**Train**

* MSE: 7.274632256868921
* RMSE: 2.697152620240264
* MAPE: 0.01031660451601425
  
**Test**

* MSE: 7.233911777009279
* RMSE: 2.689593236348069
* MAPE: 0.008975953148864863

### Predicted Test data using LSTM for 100 data
![Untitled](https://github.com/user-attachments/assets/b71d160a-ba1d-486b-9a49-ff18c8af12e7)

# SVR
**Model Development**

* Model is developed after trying different combinations of Hyperparameters and kernels
* Best Hyperparameters are C= 1, degree= 1 and Gamma=0.1
* Best Kernel is Radial Basis Function

## Model
SVR
SVR(degree=1, gamma=0.1)  
                                                                 
### Evaluate model

**Train**

* MSE: 9.33769352755235
* RMSE: 3.055763984268476
* MAPE: 0.024842191932585977
  
**Test**

* MSE: 5.296041433630696
* RMSE: 2.301312980372443
* MAPE: 0.007412437740864859

### Predicted Test data using SVR for 100 data
![Untitled](https://github.com/user-attachments/assets/dba67c78-489a-425b-a8ee-7a581d51b1cc)

