
# Project Background

We are exploring a particular use case where CSV files are received via email and new data to be updated directly to the main Postgres database. 

Instead of manually checking the email received, downloading the file and then updating the database. We will automate the whole process where the email is checked for the particular attachment received and then updates it to Postgres database directly.

# Assumptions and Caveats

- Monthly sales data in email is received by the user in CSV format only.
- CSV headers match the table columns exactly.
- n8n is used as low-code bridge linking email, data parsing and database.

# Thought process

- Check for the emails being received with attachment.
- Filter out only attachments with .CSV files.
- Validate at every step that we have a CSV and that data structure fits the database schema.
- Append the rows directly to Postgres database.

# Outcome

- Monthly CSVs emailed to you are automatically added to your Postgres table. 
- Manual imports and human errors reduced or zero.
- The workflow stays modular, reliable, and simple to maintain.

![Outcome](Images/Screenshot%202026-11-08%20180007.png)