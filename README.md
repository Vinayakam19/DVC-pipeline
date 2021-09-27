# About DVC :
DVC is a system for data version control. It is essentially like Git but is used for data. With DVC, you can keep the information about different versions of your data in Git while storing your original data somewhere else.In a typical data science project, the scientists and machine learning experts deal with a large volume of data of various kinds. There are multiple models built with varying configurations, features, with multiple iterations of parameters tuning to get the best performing model. In such a scenario, all the changes we make to data and in the model building process need to be tracked and measured for us to understand what has worked and what has not. It also is necessary to have the option to go back to a specific version and investigate past results. One such tool which lets us track all of this is Data Version Control (DVC) which helps in governing the data, the underlying model and run reproducible results.

Reference Link : https://dvc.org/

# Instructions

1. Create a Conda environment first.The command used is :- $ conda env_name python=3.7 -y
2. After creating the environment, activate it using the command $ conda activate env_name
3. Install the library dvc : $ pip install dvc
4. Initialise the git : $ git init
5. Initialise the dvc. This will result in a .dvc and .dvcignore files : $ dvc init
7. Create the three python files namely stage_01, stage_02, stage_03 using touch command
8. Create the yaml file. Here is where all the configuration of the ML pipeline is written. The command is $ touch dvc.yaml
9. Run the command to see the dvc using the command $ dvc repro

