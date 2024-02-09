<img src="https://assets.website-files.com/61a888508b7cccb7485cdac2/61b31d9009792071f950394b_logo_dscovr.svg">

# Data Scientist: NLP </br>Dynamic Domain - Topic Modeling 📝 challenge

## Abstract

This NLP challenge is an opportunity to familiarize yourself with the technologies and domains you will be working on daily here at [DSCOVR](https://dscovr.io)

We understand that your time is valuable, so please take your time to read the code challenge carefully, and when you are ready, write to me with an estimate of how long you think the development of this task will take. We are also open to negotiating an extension if necessary.

It is important to complete the challenge rather than not doing it partially. Try to push beyond your comfort zone 💪.

ML/AI research and development should be an enjoyable experience, and we hope this code challenge will be stimulating and entertaining for you.

Red 🔴 - Green ✅ - Refactor 📝 - and have fun.

## Purpose

The purpose of this test is:

* Assess your proficiency in general NLP
* Assess your expertise in data science as an engineering domain
* Comprehend your approach to algorithm selection and tuning

## The Task

Analysis of short text, such as open-ended survey responses, media posts, etc.., is challenging because of their inherent brevity.

In this ML NLP code challenge, we motivate the candidate to provide a way for hard-clustering (in which one observation, the short text, can belong to one and only one topic) open-ended responses from surveys from different and dynamic domains.

Your end goal is to implement an NLP ML pipeline (with all the relevant steps for short text processing with dynamic topic modelling by applying the most appropriate techniques from the wide range of clustering, classification, and probabilist techniques.

One of the goals is also to dynamically discover the best value for `K`, where `K` is the number of topics; pay attention to not underestimate or overestimate the number of topics.

### Output

The output (a new dataset) must represent each relevant short text with its associated topic.

See "Extra for ML/AI 🥷" below for another challenge.

### Dataset

We will provide you with 4 (indipendent) datasets in JSON format, containing a set of open-ended responses from **4 different surveys from 3 different domains**.

```shell!
$ pip install gdown
$ gdown 1YGcv-a026sMdkX_q-whqhyh1ybiH6eCI
$
$ openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -d -in datasets.tar.gz.enc | tar xz
$
$ for i in 1 2 3 4 ; do jq length json/$i.json ; done
$ for i in 1 2 3 4 ; do cat json/$i.json | jq '.[0]' ; done
$ cat sq/* #print the open question for each dataset
```

### ML NLP Stack

You can use any ML approach with the frameworks, libraries, and data visualization tools you prefer and are comfortable working with.

The language for this challenge is Python 🐍

### Notes

- Use GIT and preserve all commits.
- Ensure that the project has a well-structured directory layout.
- The use of **Jupyter Notebook** is recommended only **for a prototyping phase**, but after creating a functioning PoC in the notebook, refactor the code to create a suite of methods inside a Python module, and use it inside your preferred pipeline orchestrator or `"__main__"` function.
- Write clean and maintainable code following best practices.
- Implement proper error handling throughout the pipeline.
- A clear and concise README.md (you can write whatever you want in it, but it should mainly explain ML NLP architecture choices, how to run the pipeline, how to run tests on data (optional), etc.)
- You should be able to complete the project within a few days.

### Extra for ML/AI 🥷

#### LLMs

- Using [Langchain](https://github.com/langchain-ai/langchain) in combination with an industry LLM (OpenAI) or open-source LLM from  [Huggingface](https://huggingface.co) generate a name for each topic.

#### Modeling

- Within each main topic, there might be other relevant sub-topics; think about a technique to detect and implement them.

#### MLOps (optional):

*Choose one of these:*

- Versioning the dataset with a tool like [DVC](https://dvc.org/).
- Create a DAG with tools such as [Airflow](https://airflow.apache.org/) or [Dagster](https://dagster.io/).
- If you think experiment tracking is indispensable for production-grade ML engineering, try using [MLFlow](https://mlflow.org/) or another library.
- Implement automated testing for components and data that you think are important to test (choose the appropriate type of test).
- We highly value MLOps principles. Therefore, if you opt to utilize containers and DevOps practice for development, training, inference, and test execution, we would be extremely pleased.

## Submission

Please submit your project as a Git repository using `git bundle` with all commits preserved, or share it with us on GitHub or Gitlab.

## Contacts

For any information: [https://linktr.ee/mauro.malvestio](https://linktr.ee/mauro.malvestio)
