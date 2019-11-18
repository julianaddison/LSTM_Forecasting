# DESCRIPTION
An exercise in incoporating auxillary data in an LSTM model applied in a ride hailing setting.

Drivers are pinged whenever they are online on their mobile phone every 15 seconds indicating that they are available. The dataset contains 3 weeks (1 Jun 2017 to 21 Jun 2017) of training data and 1 week (22 Jun 2017 to 28 Jun 2017) of test data. Training data contains driver id, gender, age, number of kids the driver has and all the pings that have been received (during the training data period). The test data also contains the actual online hours which is what the LSTM model will predict.

The objective is to predict the number of hours a driver will be online on a given day. Given driver_id and date, the model should predict online_hours.The test data contains driver id, and date (during the test data period). The Root Mean Squared Error (RMSE) will be used to assess model performance. A lower RMSE suggets better model performance.

The dataset has three files. The data in the first two files are used for training the model while the third file contains test data.
1. drivers.csv: This file contains driver profile data
2. pings.csv: This file contains the driver pings. A subset of the pings.csv file called pings_subset.csv is provided as the file size is approx 1GB.
3. test.csv: This file has the test data


## INSTALLATION & USAGE
### TO RUN VIA DOCKER 

*TO BE INCLUDED IN FUTURE UPDATE*

### TO RUN LOCALLY
1. clone contents to a folder ./LSTM

2. Launch Shell

3. Install required packages in requirement.txt
	
3. cd to filelocation

```bash
cd .\.\LSTM\
```

4. Launch Jupyter Notebook
 
```bash
jupyter notebook
```

---

# FUTURE ENHANCEMENTS
The current model was trained using simple auxillary inputs. Several other features can be derived and worked into the model such as an indicator for weekdays/weekends, categorical bins for number of kids, etc. The existing model employs simple model architectures. More LSTM layers and fully connected can be added to improve the models.