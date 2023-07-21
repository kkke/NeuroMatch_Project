## NeuroMatch_Project

The structure of this repository has been reorganised to prevent clutter as we proceed with the project. You'll find a defintion of the structure following.

### root
The repository root stores the files we want immediately accessable and the repository folders. This is mostly for the benefit of the TAs, so we want our summary documents and explanatory notebooks here.

### docs
Stores current docs for the project. These can be in markdown or notebook format when explaining a dataset or code. They're often a summary of the raw experimental notebooks placed in the notebooks folder, but also contain our project goals and questions.

### docs/google_drive
Stores previous docs from Google Drive converted to markdown format.

### links
Stores reference links with a description of the purpose of the link in a markdown file. We could put all the links in one file, or use multiple files for datasets, research and topic when the single file becomes too unwieldy.

### notebooks
Stores a notebook template which loads the Steinmetz dataset and indexes it in a variety of ways. Raw experimental notebooks, derived from the notebook template, are used in developing training stages and results, etc. 

Here we save and document why the notebook was created, how we went about teasing out the why, and a summary of results which we expect our target audience to understand. We're not just writing for our purposes, but also for those who read it later -- unless, of course, we just did a quick and dirty test that doesn't need to be kept.

### notebooks/deprecated
Stores notebooks which won't be used going further in the project. For example, this is the new home of `inferring low-dimensional dynamics.ipynb`.
