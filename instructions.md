# Cisive's 2025 Data and AI Intern Interview Project

Congratulations on being invited to complete this interview project!

This project is meant to exercise and assess your ability in the basic skills required to be successful in this internship. For a junior- or senior-level Computer Science student or equivalent, we anticipate this project taking no more than a few hours, and it can be completed on any personal computer, using only free, publicly-available resources.

## Project Overview

This project consists of the following tasks:

1. **Setup:** Establish a working Python notebook `.ipynb` environment.
2. **Task 1 - Data Modeling:** Using the `.csv` files found in the `\data` directory, design, create and populate a set a database tables, and use those tables to answer a few questions. 
3. **Task 2 - Semantic Search:** Create a vector index and semantic search workflow on the `description` column of the job postings dataset.

The final product should consist of four files, two files for each task.

* The first file should be a `.ipynb` Python notebook, that should have the following properties:
    * The code cells should run in sequential order, top-to-bottom, and should complete the task (either data modeling or semantic search) when run in sequential order.
    * Markdown text cells should be used to organize the notebook cells, and provide descriptions and comments as appropriate.

* The second file should be a PDF copy of the Python notebook, showing the final state of the notebook and the output of all cells when the notebook cells are run in sequential order.

In summary, there should be four files:
1. An `.ipynb` notebook that completes data modeling task.
2. A PDF file of the `.ipynb` notebook (file #1) that shows the final state of the notebook when all cells have been run in sequential order.
3. An `.ipynb` notebook that completes semantic search task.
4. A PDF file of the `.ipynb` notebook (file #3) that shows the final state of the notebook when all cells have been run in sequential order.

All four files should be sent to back to the interviewer via the contact email provided by the recruiter.

## General Guidelines
* Read these instructions carefully and follow them carefully. Part of the evaluation is the ability to execute on written instructions.
* Feel free to use any AI tools you wish, but please make sure you understand the code you're using as you will be asked to explain your work.
* Clear thinking and clear documentation are almost as important as well-written, working code. Part of the evaluation is the ability to clearly write technical documentation.
* Please do not spend more than a few hours working on this project. We are not looking for perfection here, rather, we want to see how you think about and solve data-related problems. 


## Setup

Being able to setup a working Python notebook environment is a basic requirement for this internship.

You are free to use any Python notebook environment you choose, as long as it can be used to develop `.ipynb` notebooks, and supports the installation of python packages to the notebook environment.

If you don't have a particular preference, we find [`Visual Studio Code`](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) to be a very flexible development environment.

## Task 1 - Data Modeling

### 1.1 Explore the source data

Download this repository and explore the `.csv` source files found in the `\data` directory. This dataset gives information about job postings on a job website, along with additional information about the companies, industries, and the jobs themselves.

Spend some time exploring the data. What are the relationships between the files? What are the relationships between the various columns among the files?

If you have any questions about the dataset, use python to analyze the dataset further.

Document your findings in your python notebook.

### 1.2 Design a database schema

After spending some time familiarizing yourself with this job posting dataset, design a set of tables, also known as a database schema, to store this data.

You're free to design the schema as you see fit, but your database schema should consist of a least a `fact_job_postings` table and a `dim_company` table. If you are unfamiliar with dimension (dim) and fact table design, please consult available online resources on [`star schema`](https://en.wikipedia.org/wiki/Star_schema). 


Document your database table schema in your notebook, as well as any design choices you made, and why you made them. Why did you choose one design over another design, what trade-offs did you make?

### 1.3 Create and load a local database

Using SQLlite, or any other SQL database of your choice, implement your database schema, and load the available datasets into that schema. We recommend using the `pandas` or `polars` dataframe libraries to accomplish this.

Again, document your code as appropriate.

### 1.4 Use your database to answer some questions

Using your star schema, answer the following questions via SQL queries:

- **What is the average normalized salary by company industry?**
- **Which company has the highest average normalized salary per employee?**

### 1.5 Wrap-up and capture results 

During the course of your development of this `.ipynb` notebooks, you may have needed to circle-back and run cells out-of-order. This is entirely normal and part of the rapid, iterative development process that these notebooks are designed to facilitate. 

Please ensure that the notebook can run properly from a restarted kernel with all cells running sequentially, from beginning to end. Save the `.ipynb` notebook and a PDF of the notebook as described in previous instructions.


## Semantic Search

Create a vector index and semantic search workflow on the `description` column in the job postings dataset. Please do not feel compelled to spend any money on this section for vector indexes or embedding models - you are free to use open source libraries and providers or your choice such as [`SentenceTransformers`](https://sbert.net/),[ `ChromaDB`](https://www.trychroma.com/), and [`HuggingFace`](https://huggingface.co/).

For your final submission, show that your semantic search workflow functions as expected by looking at the top 10 results for the following queries:

- `I'm looking for a job that requires a nursing degree`
- `Construction work, civil engineering, architecture`
- `Are there any medical research jobs?`


