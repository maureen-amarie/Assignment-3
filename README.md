!pip install faker                                                         #To install the faker library
from faker import Faker                                                    #Imports the Faker library, which is used to generate fake names, emails, jobs, cities, etc.
import pandas as pd                                                        #Imports the pandas library, which is used to store and manage data in a table-like format (DataFrame).
import re                                                                  #Imports Python's built-in re module, used for regular expressions — useful for cleaning up the phone numbers.


# Initialize Faker
fake = Faker()                                                             #Creates a Faker instance. This object (fake) is used to generate fake data.


# Number of records to generate
num_records = 5                                                            #change this to generate more or fewer records

# Generate data
data = []                                                                  #Initializes an empty list to store each fake person's info.
for _ in range(num_records):                                               #Starts a loop that runs num_records times (10 times in this case).
    person = {                                                             #Inside the loop, a dictionary called person is created. Each field uses fake methods to                                                                            generate fake: fullname,phone number(random format),email address, job title and city
        "Full Name": fake.name(),
        "Phone Number": fake.phone_number(),
        "Email Address": fake.email(),
        "Job Title": fake.job(),
        "City": fake.city()
    } 
    data.append(person)                                                    #Adds each person dictionary to the data list.



# Function to clean phone numbers
def clean_phone_number(phone):                                             #Defines a function called clean_phone_number():
    digits = re.sub(r'\D', '', phone)                                      #removes all characters except digits.
    return digits[-11:] if len(digits) >= 11 else digits                   #Keep only last 11 digits

# Convert to DataFrame for easy viewing/export
df = pd.DataFrame(data)                                                    #Converts the data list into a DataFrame — a table-like structure that's easier to process and export.

# Clean phone numbers
df["Phone Number"] = df["Phone Number"].apply(clean_phone_number)          #Applies the clean_phone_number function to every value in the "Phone Number" column. This standardizes the format.

# Display the DataFrame
print(df)                                                                  #Prints the entire DataFrame with all fake records and cleaned phone numbers.

df.to_csv("fake_data.csv", index=False)                                    #Exports the cleaned data to a CSV file named fake_data.csv.index=False prevents pandas from saving the row numbers (0, 1, 2...) into the file.





