# Cisive's 2025 Data and AI Intern Interview Project

Congratulations on being invited to complete this interview project!

This project is meant to exercise and assess your ability in the basic skills required to be successful in this internship. For a junior- or senior-level Computer Science student or equivalent, we anticipate this project taking no more than a few hours, and it can be completed on any personal computer, using only free, publicly-available resources.

## General Guidelines
* Read these instructions carefully and follow them carefully. Part of the evaluation is the ability to execute on written instructions.
* Feel free to use any AI tools you wish, but please make sure you understand the code you're using as you will be asked to explain your work.
* Clear thinking and clear documentation are almost as important as well-written, working code. Part of the evaluation is the ability to clearly write technical documentation.
* If you encounter any ambiguities in the tasks, just use your best judgment, and decide for yourself what is the best way to accomplish those tasks. We are not looking for any specific answer, so any reasonable interpretation will be fine.
* Please do not spend more than a few hours working on this project. We are not looking for perfection here, rather, we want to see how you think about and solve data-related problems.
* Don't be discouraged if you find you cannot complete all tasks. Some of these tasks are designed to be more difficult than others. Submitting partially-completed work is still sufficient to continue in the interview process, and is not disqualifying.


## Project Overview

This project consists of the following tasks:

1. **Setup:** Establish a working Python notebook `.ipynb` environment.
2. **Task 1 - Data Modeling:** Using the `.csv` files found in the `\data` directory, design, create and populate a set a database tables, and use those tables to answer a few questions. 
3. **Task 2 - Semantic Search:** Create a vector index and semantic search workflow on the `description` column of the job postings dataset.
4. **Submit Completed Project:** Gather your completed files and submit them to the interviewers - congratulations, you're done!


## Setup

Being able to setup a working Python notebook environment is a basic requirement for this internship.

You are free to use any Python notebook environment you choose, as long as it can be used to develop `.ipynb` notebooks, and supports the installation of python packages to the notebook environment.

If you don't have a particular preference, we find [Visual Studio Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) to be a very flexible development environment.

## Task 1 - Data Modeling

### 1.1 Explore the source data

Download this repository and explore the `.csv` source files found in the `\data` directory. This dataset gives information about job postings on a job website, along with additional information about the companies, industries, and the jobs themselves.

Spend some time exploring the data. What are the relationships between the files? What are the relationships between the various columns among the files?

You'll encounter a lot of missing data in certain columns. Don't worry too much about this, just assume those fields are optional.

If you have any questions about the dataset, use python to analyze the dataset further.

Document your findings in your python notebook.

### 1.2 Design a database schema

After spending some time familiarizing yourself with this job posting dataset, design a set of tables, also known as a database schema, to store this data.

You're free to design the schema as you see fit, but your database schema should consist of a least a `fact_job_postings` table and a `dim_company` table. If you are unfamiliar with dimension (dim) and fact table design, please consult available online resources on [star schema](https://en.wikipedia.org/wiki/Star_schema). 


Document your database table schema in your notebook, as well as any design choices you made, and why you made them. Why did you choose one design over another design, what trade-offs did you make?

### 1.3 Create and load a local database

Using SQLlite, or any other SQL database of your choice, implement your database schema, and load the available datasets into that schema. We recommend using the `pandas` or `polars` dataframe libraries to accomplish this.

Again, document your code as appropriate.

### 1.4 Use your database to answer some questions

Using your star schema, answer the following questions via SQL queries:

Let's start with some simpler questions:

- **How many companies have more than one job posting?**
- **How many job postings are there for each job industry?**

Now let's move to more advanced questions:

- **What is the average normalized salary by company industry?**
- **Name the top 5 companies with the highest average normalized salary for their job postings.**

You should notice that there is some missing salary data, but we still need to come up with an answer to these questions. How can we properly communicate the limitations of our analysis, given that we don't have all the data?

### 1.5 Wrap-up and capture results 

During the course of your development of this `.ipynb` notebook, you may have needed to circle-back and run cells out-of-order. This is entirely normal and part of the rapid, iterative development process that these notebooks are designed to facilitate. However, now that you're done, take some time to organize and clean-up the notebook as appropriate.

Please ensure that the notebook can run properly from a restarted kernel with all cells running sequentially, from beginning to end.

Additionally, please create a PDF copy of the `.ipynb` notebook, showing the final state of the notebook and the output of all cells after the notebook cells have been run in sequential order.

Save the `.ipynb` notebook and the PDF file.


## Task 2 - Semantic Search

### 2.1 Pick vector index and embedding providers

You can use any vector index/database and embedding provider that you like, but the simplest and most time-effective solution is probably [ `ChromaDB`](https://www.trychroma.com/) and [`SentenceTransformers`](https://sbert.net/). Install the necessary libraries for you vector index and embedding model.

### 2.2 Create a job description index

Create a vector index and semantic search workflow on the `description` column in the job postings dataset. You can use either the data from your SQL tables or the original CSV file for this. After embedding all of the descriptions, display the dimension of one of the embedding vectors in your index.

### 2.3 Test your semantic search workflow

Show that your semantic search workflow functions as expected by looking at the top 10 results for the following queries:

- `I'm looking for a job that requires a nursing degree`
- `Construction work, civil engineering, architecture`
- `Are there any medical research jobs?`

For each query, your notebook should display the top 10 most semantically similar results. Based on the results, do you think your semantic search workflow is functioning properly? What are some rigorous ways to evaluate semantic search? List one or two ways you might improve your semantic search workflow if you had more time.

## Submit Completed Project

The final product should consist of four files, two files for each task.

* The first file should be a `.ipynb` Python notebook, that should have the following properties:
    * The code cells should run in sequential order, top-to-bottom, and should complete the task (either data modeling or semantic search) when run in sequential order.
    * Markdown text cells should be used to organize the notebook cells, and provide descriptions and comments as appropriate.

* The second file should be a PDF copy of the `.ipynb` notebook, showing the final state of the notebook and the output of all cells after the notebook cells have been run in sequential order.

In summary, there should be four files:
1. An `.ipynb` notebook that completes data modeling task.
2. A PDF file of the `.ipynb` notebook (file #1) that shows the final state of the notebook when all cells have been run in sequential order.
3. An `.ipynb` notebook that completes semantic search task.
4. A PDF file of the `.ipynb` notebook (file #3) that shows the final state of the notebook when all cells have been run in sequential order.

All four files should be sent to back to the interviewer via the contact email provided by the recruiter.