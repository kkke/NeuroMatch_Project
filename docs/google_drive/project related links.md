## Links
___

### Understanding RNN and LSTM (it's a commonly used RNN):

__RNN__ -[https://www.youtube.com/watch?v=AsNTP8Kwu80&ab\_channel=StatQuestwithJoshStarmer](https://www.youtube.com/watch?v=AsNTP8Kwu80&ab_channel=StatQuestwithJoshStarmer)

__LSTM__ -[https://www.youtube.com/watch?v=YCzL96nL7j0&t=98s&ab\_channel=StatQuestwithJoshStarmer](https://www.youtube.com/watch?v=YCzL96nL7j0&t=98s&ab_channel=StatQuestwithJoshStarmer)

## Datasets

[https://deeplearning.neuromatch.io/projects/docs/datasets\_and\_models.html](https://deeplearning.neuromatch.io/projects/docs/datasets_and_models.html)

[https://deeplearning.neuromatch.io/projects/Neuroscience/ideas\_and\_datasets.html](https://deeplearning.neuromatch.io/projects/Neuroscience/ideas_and_datasets.html)

Colab Notebook : [Steinmetz Notebook](https://github.com/NeuromatchAcademy/course-content/blob/main/projects/neurons/load_steinmetz_decisions.ipynb)

## Project idea: Decoding of neural activity

[_Description of the decoding of human brain activity and dataset_ (Electrocorticography aka ECoG)](https://www.youtube.com/watch?v=rAqtrBhwS80&ab_channel=TEDxTalks)

[_ECoG dataset_ on the Neuromatch Github](https://github.com/NeuromatchAcademy/course-content/tree/main/projects/ECoG)

_Possible options/idea_
1. Using the [memory n-back dataset](https://deeplearning.neuromatch.io/projects/ReinforcementLearning/human_rl.html%23n-back-task) mentioned in the website above could be an option if we want to explore that (it could also possibly be connected with this RL project template if we would also like to implement that.

2. The decoding performed in the data of faces/houses mentioned in the video seems to be some [template projection approach](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004660). I was wondering if deep learning could be applied to this dataset for the decoding but we need to see if that data would be enough for a deep learning network to perform well…the description mentions that the [data consists of 2 sessions from 7 subjects](https://colab.research.google.com/github/NeuromatchAcademy/course-content/blob/main/projects/ECoG/load\_ECoG\_faceshouses.ipynb).

 _Problems/concerns_

 Not sure whether the memory n-back would be enough data for applying deep learning…the description mentions that the [data consists of 3 sessions from 3 subjects](https://colab.research.google.com/github/NeuromatchAcademy/course-content/blob/main/projects/ECoG/load_ECoG_memory_nback.ipynb).

### Another decoding idea/possibility

_Decoding of neural activity in the mice brain_. Data collected using electrophysiology recordings by Nick Steinmetz… [here's the description of the data](https://www.youtube.com/watch?v=WXn4-FpVaOo&ab_channel=NeuromatchAcademy).

[_Steinmetz dataset_](https://compneuro.neuromatch.io/projects/neurons/README.html)

_Background_: [Paper on applying ML/DL models for neural decoding at the population level](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7470933/). The codes are provided and the intuition behind applying ML/DL models for neural decoding is mentioned, so would be a good background material to understand how ML/DL can be applied to decode neural activity) - the data used in this paper for the decoding of spatial location based on the population level neural activity in the Hippocampus is from the Buzsaki's lab and [can be found here](https://crcns.org/data-sets/hc/hc-2/about-hc-2). So possibly that dataset could also be used for trying several DL algorithms like Feed-forward NN, Simple RNN, GRU and LSTM (both are types of RNN), and ensemble methods (combining several of them).

The dataset used in this paper from the neural recordings in the premotor cortex of the monkeys [can be found here](https://crcns.org/data-sets/motor-cortex/pmd-1/about-pmd-1).