# Automated-Data-Query-and-Retrieval-System

This is a small Python project I built to load product data from a CSV file into MongoDB and then use LLaMA (via Ollama) to generate MongoDB queries based on natural language prompts.

### What it does:
1. Loads data from `sample_data.csv` into MongoDB Atlas.
2. Runs some predefined test cases where I ask questions in plain English.
3. Uses the LLaMA model to generate MongoDB queries from those prompts.
4. Executes the queries on the MongoDB collection.
5. Saves both the query results as CSV files and also stores the generated queries in a text file (`Quries_generated.txt`).
6. Has an interactive mode where I can type any custom query prompt and get results.

---

### How to run the code:

1. Make sure you have:
   - Python installed
   - `pandas` and `pymongo` installed (`pip install pandas pymongo`)
   - [Ollama](https://ollama.com/) installed and set up with LLaMA 3 pulled

2. Replace the path to your CSV if it's different:
   ```python
   df = pd.read_csv("/Users/apple/Downloads/sample_data.csv")
Run the script:

bash
Copy
Edit
python your_script_name.py
After running:

The queries will be saved in Quries_generated.txt

Each test case result will be saved as a CSV (like test_case1.csv)

You can also type your own prompt during interactive mode!

Example test cases:
Find products from Nike or Sony with more than 200 reviews and rating below 4.5

Find all Electronics products that are in stock and have a rating >= 4.5

Show products launched after Jan 1, 2022 in Home & Kitchen or Sports categories

These are used to check how well the LLaMA model can generate real MongoDB queries.

File Outputs
Quries_generated.txt – contains the queries generated for the test cases.

test_case1.csv, test_case2.csv, etc. – query results from MongoDB.
