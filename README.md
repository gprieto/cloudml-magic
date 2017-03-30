# cloudml-magic
cloudml-magic is a Jupyter Notebook Magics for interactively working with [Google Cloud Machine Learning Engine](https://cloud.google.com/ml-engine/).

![diagram](readme_diagram.png)

# Prerequisites
Before you begin, prepare Google Cloud Platform project and enable billing.

Also this magics use Application Default Credentials.
To activate the credentials, enter
```bash
gcloud auth application-default login
```

# Installation
**To install** this magics
```bash
pip install cloudmlmagic
```

**To use** this magics, enter the following command in your notebook.

```py
in [1]: %load_ext cloudmlmagic
```

That's it!

# How to use

## %ml_init
This magic initializes your cloud ml job request. Do NOT forget to initialize before adding code or run.

Example:

```py
in [2]: %ml_init -projectId PROJECTID -bucket BUCKET -region us-central1 -scaleTier BASIC
```

## %ml_code
This magic adds the block into uploading package.

## %ml_run
To run a training job, add this magic on your code block.

**Run on local Machine**  
Do not add this magic, or add `%ml_run`

**Run on Cloud ML Engine**  
add `%ml_run cloud`
