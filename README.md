# NeuroMatch_Project
**Abstract**  
Neural activity in the brain is able to represent the outside world and instruct behavioral movements. Inferring this representation from neural activity is essential for understanding brain function and advancing the application of brain-machine interfaces. There are multiple approaches available to infer information from neural data. Using the Steinmetz dataset (**Steinmetz et al, 2019**), here we compare the performance of different deep learning models to infer responses from neural data recorded from a mouse brain when the mouse is performing a perceptual decision-making task. For classifying trial types based on neural data, we found that Multilayer Perceptron (MLP), Long Short Term Memory (LSTM), and Gated Recurrent Unit (GRU) predict trial types with validation accuracies of 0.81 (MLP, one hidden layer), 0.83 (GRU, one hidden layer), 0.82 (LSTM, one hidden layer) respectively. Surprisingly, we observed that MLP without a hidden layer (0.86) outperforms MLP with one hidden layer (0.81), which outperforms MLP with two hidden layers (0.69). For predicting the wheel speed, we tested MLP and LSTM models and found that the prediction accuracy (R^2) was marginally higher using LSTM (0.89) as compared to MLP (0.85). When comparing across the sub-regions of the motor cortex (primary and secondary) and predicting using a similar number of neurons (186) for each sub-region, we found that the prediction accuracy using the activity from the primary motor cortex (0.77) was better than the secondary motor cortex (0.65). For our experiments on the Steinmetz dataset, we observed that deep learning models work well for regression tasks such as predicting an animal’s action (turning the wheel) from neural data. However, MLP without a hidden layer (which resembles logistic classification) outperforms more complex models for simple classification tasks.

# Modeling Steps 1 to 4

We can enter our results for each modeling step we take.

## Step 1: Define question/goal of project
Note: select dataset compatible with deep learning.

The current dataset we are working with: Steinmetz dataset: https://compneuro.neuromatch.io/projects/neurons/README.html. 
Data collected using electrophysiology recordings by Dr. Nick Steinmetz…here’s the video description of the data: https://www.youtube.com/watch?v=WXn4-FpVaOo&ab_channel=NeuromatchAcademy
Steinmetz notebook: https://github.com/NeuromatchAcademy/course-content/blob/main/projects/neurons/load_steinmetz_decisions.ipynb

__Goal:__ Decode animal's behaviors (reaction time, pupil size, responses, feedback, et al) from neural data:
 1) data preparation: alldata, data for specific brain regions
    - Ke Chen, 
 2) build MLP, RNN models
    - Dev, Ke (MLP), Arjun (LSTM), Raymond, Mohammad (RNN),
 3) tuning hyperparameters to check model performance
    - Dev, Ke (MLP), Arjun, Raymond, Mohammad (RNN),
 4) Performance evaluation, sensitivity, AUC, Accuracy, R^2, Confusion Matrix
    - Dev, Ke, Arjun, Raymond, Mohammad,
 5) Try different loss function to choose the best one.
    - Dev, Ke, Arjun, Raymond, Mohammad,

Use MLP to decode animal's responses from neural data: https://github.com/kkke/NeuroMatch_Project/blob/main/Copy_of_load_steinmetz_decisions.ipynb

Other ideas that can be implemented: 

Technical stuff 
1) Use validation dataset, regularization, hyperparameter tuning by Bayesian Optimization (if its applicable) etc. 
2) RNN performance comparison with Multi-layer perceptron 
3) Check this for implementing RNN (LSTM) with Pytorch and Lightning:https://www.youtube.com/watch?v=RHGiXPuo_pI&ab_channel=StatQuestwithJoshStarmer 

Domain related stuff
1) Use particular time interval that is relevant to the decision making of the mice
2) Compare across brain regions
3) Try dat[‘feedback_type’] for correct vs incorrect responses: -1 for negative feedback (white noise burst); +1 for positive feedback (water reward delivery) - the neural activity in the relevant brain regions might be stable just before the mice makes the correct decision while it might be unstable just before the incorrect decision - Is that the case? Could probably be a testable hypothesis 
4) Can try with LFP data, if there’s time
5) Also here’s some useful info about Poisson distribution assumption for neural firing: Why do we use poisson process for neural firing? https://biology.stackexchange.com/questions/56679/why-poisson-process-for-neural-firing


~~_Goal 1: Predict from one emsemble neural activity (same session) to other emsemble neural activity (same session) focusing on one trial type;
Can test whether it generalize to other trial types: From one trial type to other trial types;_~~ 

~~_Goal 2: Repeat goal 1 with each trial types;
“Find a way to get insights where generalizaiton works or not ”
Scratch thoughts: check the latent dynamic_~~

~~_Goal 3: Repeat goal 1 with all trial types combined_
_Test whether the predicition accuracy comprised or not._~~

~~_Goal 5: “latent dynamic from RNN, could it be used to predict behaviors?”_~~

## Step 2: Literature review summary (put links in links doc)


## Step 3: Identify ingredients (what items to use in the model for our study)


## Step 4: Quantify hypotheses

Neural activity from one trial type generalizes to other trials (Goal 1-3)?: 
Cross-trial type prediction accuracy
Pitfall: some neurons are specialists for each trial types, while some may be generalists for all. 
Animal’s behaviors could be predicted by neural activity?


# Useful links:

Understanding RNN and LSTM (it’s a commonly used RNN):
RNN - https://www.youtube.com/watch?v=AsNTP8Kwu80&ab_channel=StatQuestwithJoshStarmer
LSTM - https://www.youtube.com/watch?v=YCzL96nL7j0&t=98s&ab_channel=StatQuestwithJoshStarmer

Sequence Classification with LSTM Recurrent Neural Networks in Python with Keras
https://machinelearningmastery.com/sequence-classification-lstm-recurrent-neural-networks-python-keras/

https://neuronaldynamics.epfl.ch/online/Ch16.S2.html

https://compneuro.neuromatch.io/_images/WorkingMemoryAttractorModels.svg

Extracting computational mechanisms from neural data using low-rank RNNs
https://pillowlab.princeton.edu/pubs/Valente22neurips_lowrankRNNs.pdf
Github scripts: https://github.com/adrian-valente/lowrank_inference/
