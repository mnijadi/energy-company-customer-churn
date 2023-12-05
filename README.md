# Data Science Virtual Internship : Customer Churn Analysis & Modeling (In Progress)

## Introduction

This project is a part of the [BCG's Data Science virtual internship](https://www.theforage.com/virtual-internships/prototype/Tcz8gTtprzAS4xSoK/Data-Science-Virtual-Experience-Program).  
The project is about analyzing and modeling customer churn data for an electricity and gas commpany.  
The project is divided into 3 parts:

- Hypothesis framing and in depth exploratory data analysis
- Feature engineering and modeling with machine learning
- Business insights and recommendations using a dashboard

## Data

The data our client provided us with contains 2 datasets:

- `client_data.csv`: contains information about the clients
- `price_data.csv`: contains information about historical prices

## Tools

The project was done using Python 3 and the following libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

Dashboards were created using Tableau Public, you can find them [here](https://public.tableau.com/).

## Setup

### Docker

If you want to use Docker (first time dockerizing a project) for running the project in an isolated environment, you can use the provided `Dockerfile` by doing the following:

1. In the project directory, build the image `customer-churn-image`
2. Run the container
3. Go to `localhost:8888` in your favorite browser and go through the notebooks

### Virtual environment

If you want to use a virtual environment, you can use the provided `requirements.txt` file by doing the following:

1. In the project directory, create a new virtual environment `customer-churn-venv`
2. Activate the virtual environment (demo uses linux but the process is similar for any OS)
3. Install the requirements

```bash
python3 -m venv customer-churn-venv
source customer-churn-venv/bin/activate
pip3 install -r requirements.txt
```

## Acknowledgements

Huge thanks <3 to [Forage](https://www.theforage.com/) and [BCG](https://www.bcg.com/) for providing practitioners with real-world data science problems.
