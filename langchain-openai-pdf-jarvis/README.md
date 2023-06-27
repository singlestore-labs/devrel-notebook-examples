# How to use the Notebook

## Step 1
Sign up for SingleStore at https://singlestore.com

## Step 2
Create a workspace and a database

## Step 3
Clone this repo or download this notebook file (langchain_pdf_demo.ipynb) locally.

## Step 4 
Click on the Notebooks link on the left-hand side and then click on the down arrow on the top right near the New Notebook button in the SingleStore portal. Click Import Notebook and choose the notebook you selected in the step above.

## Step 5
In the Notebook, replace "winter_wikipedia" with your database in the code block in Notebook:
```
%%sql

USE winter_wikipedia;
DROP TABLE IF EXISTS my_book;
CREATE TABLE IF NOT EXISTS my_book (
    id INT PRIMARY KEY,
    text TEXT CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci,
    embedding BLOB
);
```
## Step 6
In the Notebook, add your OpenAI key in the code below by replacing OPENAI_KEY with your own:
```

OPENAI_API_KEY = os.environ.get(
    'OPENAI_API_KEY',
    'YOUR-KEY-HERE'
)

```

## Step 7
Execute each block of code from the top by clicking on the play button next to each code block
