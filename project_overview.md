# Cisive's Data and AI 2025 Intern Interview Project

For this interview project, you will be tasked with a relatively open-ended project broken out into into two sections. Both section require to use the attached `.csv` files.

For the final submission, please send us a PDF copy of an `.ipynb` file with your work. Please use markdown cells to provide brief explanations of what you've done.

## Data Modeling
Create a local SQLlite database, or any other SQL database or your choice, and load the available datasets into a star schema. We recommend using the `pandas` or `polars` dataframe libraries to accomplish this.

 You're free to design the schema as you see fit, but your star schema should consist of a least a `fact_job_postings` table and a `dim_company` table.

For your final `.ipynb` submission, show that you've successfully loaded the data into a star schema. Using your star schema, answer the following questions via SQL queries:

- `What is the average normalized salary by company industry?`
- `Which company has the highest average normalized salary per employee?`

## Semantic Search

Create a vector index and semantic search workflow on the `description` column in the job postings dataset. Please do not feel compelled to spend any money on this section for vector indexes or embedding models - you are free to use open source libraries and providers or your choice such as [`SentenceTransformers`](https://sbert.net/),[ `ChromaDB`](https://www.trychroma.com/), and [`HuggingFace`](https://huggingface.co/).

For your final submission, show that your semantic search workflow functions as expected by looking at the top 10 results for the following queries:

- `I'm looking for a job that requires a nursing degree`
- `Construction work, civil engineering, architecture`
- `Are there any medical research jobs?`

## General Notes
Please do not spend more than a few hours working on this project. We are not looking for perfection here, rather, we want to see how you think about and solve data-related problems. Feel free to use any AI tools you wish, but please make sure you understand the code you're using as you will be asked to explain your work.
