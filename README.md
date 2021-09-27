# About DVC :
DVC is a system for data version control. It is essentially like Git but is used for data. With DVC, you can keep the information about different versions of your data in Git while storing your original data somewhere else.In a typical data science project, the scientists and machine learning experts deal with a large volume of data of various kinds. There are multiple models built with varying configurations, features, with multiple iterations of parameters tuning to get the best performing model. In such a scenario, all the changes we make to data and in the model building process need to be tracked and measured for us to understand what has worked and what has not. It also is necessary to have the option to go back to a specific version and investigate past results. One such tool which lets us track all of this is Data Version Control (DVC) which helps in governing the data, the underlying model and run reproducible results.

DVC provides the following features :
1. Experiment tracking with help of DVC studio
2. Data versioning
3. Model versioning
4. Managing the artefacts with help of Git
5. Building machine learning pipelines

Reference Link : https://dvc.org/

In this repository we build a very basic Data pipeline, wherein one component will create the file, the other two components will read the file.

# Instructions

1. Create a Conda environment first.The command used is :- `$ conda env_name python=3.7 -y`
2. After creating the environment, activate it using the command `$ conda activate env_name`
3. Install the library dvc : `$ pip install dvc`
4. Initialise the git : `$ git init`
5. Initialise the dvc. This will result in a .dvc and .dvcignore files : `$ dvc init`
7. Create the three python files namely stage_01, stage_02, stage_03 using touch command.
8. We generate a yaml file called `dvc.yaml` where in we include information about the the command we need to run, the dependencies and the outputs
9. We reproduce the pipeline by running the command `$ dvc repro`. Running dvc repro would automatically create a dvc.lock that help to track the pipeline outputs.Additionally, it also allows the DVC to detect when dependencies have changed and tracks the intermediate and final outputs of the file.
10. To view the DVC pipeline type `$ dvc dag`

In this DVC we have three stages namely, Stage 1, Stage 2 and Stage 3

1. In Stage 1, we create the file artifacts01.txt
2. The stage 2 would read the contents of the text file artifacts01.txt
3. In Stage 3, we read the text fike artifacts01.txt and output another text file artifacts02.txt

NOTE : Stage 2 and Stage 3 would execute successfully only when Stage 1 has completed the execution

The output of the DVC dag would look like for this code which is essentially a data pipeline.

![dvc](https://user-images.githubusercontent.com/45694329/134889028-561dd3e0-97c1-4d76-8c24-6865a479dc9a.png)

