This is a GitHub Repo for the project to reproduce results of paper "Learning of Cluster-based Feature Importance for Electronic Health Record Time-series" for Deep Learning for Healthcare project Spring 2023.

Apart from basic model implementation, it contains ablation study to introduce weight smoothning within the model.

The Repo is structured as follows:
- all scripts are saved under "src/"
- data is assumed to be under folder "data/{DATA_NAME}"
- paths to save results and visualisations are "visualisations/{DATA_NAME}/" and "results/{DATA_NAME}"

- "src/data_processing/" details scripts for processing HAVEN (proprietary dataset) and MIMIC-IV dataset.
- "src/results/" contains main.py script that determines what results to save/how to save/...
- Similarly, "src/visualisation/" contains main.py script that determines how to print, what to print, ...
- "src/models/" contains all models considered for analysis (inc. CAMELOT and benchmarks). Each model contains a model wrapper class that has a "train" and "analyse" methods.
- Training can be done in "src/training/run_model.py" using the command "python -m src.training.run_model" using this folder as the working directory. Configuration files for data, model and results need to be edited for new experiments. The script runs for all configuration possibilities (check the individual folders for the precise configuration names". 
