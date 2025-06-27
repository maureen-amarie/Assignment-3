# Batch Processing using Python

This is a simple Python project that generates, processes, and exports fake employee contact data. It's a great way to practice working with data using Python libraries like `Faker`, `pandas`, and `re` for regular expressions.

# Project Description

The script creates a list of fake employee records containing:

- Full Name  
- Phone Number  
- Email Address  
- Job Title  
- City  

Once the data is generated, it cleans up all phone numbers by converting them into a consistent **11-digit numeric format** (no symbols, no spaces). Finally, the clean data is saved to a CSV file for use in other applications like Excel, databases, or analytics tools.

This kind of data processing is useful in real-world scenarios where raw data must be cleaned before being stored or analyzed.

---
# Setup Instructions
1. Make sure you have Python 3 installed.
2. Install the required Python libraries:
   ```bash
   pip install faker pandas

# How to Run the Script
Run the script using the command line or an IDE (like VS Code, PyCharm, or Jupyter Notebook):
python batch_processing.py
After running, a file called fake_data.csv will be created in your current directory with the processed records.

# Sample Output
Here’s an example of what the output might look like:

| Full Name         | Phone Number | Email Address                                           | Job Title         | City          |
| ----------------- | ------------ | ------------------------------------------------------- | ----------------- | ------------- |
| Melanie Wilson    | 32743447442  | [scottmose@example.com](mailto:scottmose@example.com)   | Marketing Manager | Gilmoreport   |
| Christopher Mccoy | 2435328800   | [jacobisms@example.com](mailto:jacobisms@example.com)   | Engineer          | South Bruce   |
| Jean Craig        | 45280755690  | [meyeralex@example.com](mailto:meyeralex@example.com)   | Stage Manager     | South Yolenda |
| James Price       | 78577243593  | [upeck@example.com](mailto:upeck@example.com)           | Scientist         | North Thomas  |
| Joel Hamilton     | 4136704128   | [galexander@example.com](mailto:galexander@example.com) | Company Director  | Pagemouth     |



