# NeuroMatch_Project
# Modeling Steps 1 to 4

We can enter our results for each modeling step we take.

## Step 1: Define question/goal of project
Note: select dataset compatible with deep learning.
### Goal 1: Predict from one emsemble neural activity (same session) to other emsemble neural activity (same session) focusing on one trial type;
Can test whether it generalize to other trial types: From one trial type to other trial types; 
Prediction accuracy

### Goal 2: Repeat goal 1 with each trial types
“Find a way to get insights where generalizaiton works or not ”
Scratch thoughts: check the latent dynamic


### Goal 3: Repeat goal 1 with all trial types combined
Test whether the predicition accuracy comprised or not.

### Goal 4: Predict from neural activity (real data & generated artificial data) to animal’s behaviors (reaction time, pupil size, et al) or trial types (left, right, correct, error)
##########################
##########################
Use MLP to decode animal's responses from neural data: check Copy_of_load_steinmetz_decisions.ipynb 



### Goal 5: “latent dynamic from RNN, could it be used to predict behaviors?”

## Step 2: Literature review summary (put links in links doc)


## Step 3: Identify ingredients (what items to use in the model for our study)


## Step 4: Quantify hypotheses

Neural activity from one trial type generalizes to other trials (Goal 1-3)?: 
Cross-trial type prediction accuracy
Pitfall: some neurons are specialists for each trial types, while some may be generalists for all. 
Animal’s behaviors could be predicted by neural activity?


Usefull links:
Sequence Classification with LSTM Recurrent Neural Networks in Python with Keras
https://machinelearningmastery.com/sequence-classification-lstm-recurrent-neural-networks-python-keras/

https://neuronaldynamics.epfl.ch/online/Ch16.S2.html

https://compneuro.neuromatch.io/_images/WorkingMemoryAttractorModels.svg

https://pillowlab.princeton.edu/pubs/Valente22neurips_lowrankRNNs.pdf
