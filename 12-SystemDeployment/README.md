# System Deployment
This laboratory encompasses the entire life-cycle of a NIDS. It spans from the ANN model design, through the phases of model training and testing, culminating in the deployment onto the target machine. Follow the steps of the laboratory.

## NIDS implementation, training, tuning and testing
1. Implement an MLP model from scratch
2. Define the ranges of hyperparameters and execute training
3. Execute hyperparameter tuning
4. Test the trained model on the test set and on one or more pcap files using the notebook

## NIDS deployment
1. Export the notebook to a stand-alone Python script.
2. Execute the script using the arguments ```--model``` and ```--predict``` to indicate the paths to the trained model and to the folder with the test set respectively. 
3. Execute the script using the arguments ```--model``` and ```--predict_live``` to indicate the paths to the trained model and to a ```pcap``` file respectively.


## Technical details
In this lab, you need three terminals, one for running the jupyter server, one for running the stand-alone NIDS and a third one for starting the network attack:

- **Terminal 1:**
    - ```jupyter notebook```
- **Terminal 2:**
    - ```cd network-intrusion-and-anomaly-detection-with-ml/12-SystemDeployment```
    - ```jupyter nbconvert --to python NIDS-lab.ipynb```
    - Example: ```python NIDS-lab.py --train ./DOS2019_Binary_5_Attacks_MLP --model nids_model.h5```
    - Example: ```python NIDS-lab.py --predict_live DOS2019_Binary_5_Attacks_PCAPs/ddos-chunk.pcap --model nids_model.h5```
