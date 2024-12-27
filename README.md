
# Sentiment Analysis on Response PDF file

## Response PDF
* The Response PDF file comprises 106 student feedback responses, all centered around the fascinating subject of Mathematics. These responses are neatly organized in a table format in PDF, featuring 15 distinct questions and corresponding answers.
* I have delve into techniques for PDF data extraction, gaining practical skills. Sentiment analysis will allow to gauge student sentiments, providing valuable context.

## Project Objective
* The mission is to uncover insights from PDF files and perform sentiment analysis on the student feedback.
* Extracting data from the PDF and transforming it into a structured dataframe will be our key challenge.
* Through this project, I will bridge the gap between raw PDF content and meaningful data insights.



# Deployment

## Reading PDF and Data Cleaning
* Utilized the PdfReader from the PyPDF2 library to read the Response.pdf file.
* Extracted the data as text into a NumPy array.
* Split the text based on question marks (‘?’) to isolate individual questions.
* Segregated the 15 questions into a list called “ques” and collected student answers into a separate list called “feedbacks”.
* Removed timestamps and dates from the feedbacks.
* Developed a function to format feedback elements into new list after every 14 entries.
* Identified unique student responses and organized them into a nested list representing all student feedback.
## Data Frame Conversion
* Rename nested list as “df_row” for feedbacks and renamed the ques list to “col_df”.
* Converted both lists into Pandas DataFrames.
* Concatenated the df_row and col_df DataFrames to create a single table resembling the PDF structure.
* Shifted the first row to serve as the header, resulting in 15 distinct responses across 106 student rows.
## Column-wise Sentiment Analysis
* Counted the student responses for each distinctive option within a question column.
* Assigned sentiment scores (positive, zero, negative) to these options.
* Calculated the total sentiment score by multiplying the count with the corresponding sentiment score and dividing by the total count (106 students).
* Computed the average sentiment score for each question.
* Plotted pie graphs to visualize student responses for each question.
* This provided an overview of sentiment distribution across options.
## Row-wise Sentiment Analysis
* Developed a function for row-wise sentiment analysis using TextBlob.
* The result was divided by 15 to obtain the final sentiment value for each student.
* If the value was ≤ 0.12, the student was considered confident with a strong foundation in mathematics; otherwise, they were deemed under-confident with a weaker base.

[Sentiment Analysis on Response PDF Presentation](https://www.canva.com/design/DAGCxWiSnes/oFEHxChZOMB0XI7Ow3b4kQ/view?utm_content=DAGCxWiSnes&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h338195a6d5)

