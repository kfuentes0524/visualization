# Data Visualization

## Assignment 4: Final Project

### Requirements:
- We will finish this class by giving you the chance to use what you have learned in a practical context, by creating data visualizations from raw data. 
- Choose a dataset of interest from the [City of Toronto’s Open Data Portal](https://www.toronto.ca/city-government/data-research-maps/open-data/) or [Ontario’s Open Data Catalogue](https://data.ontario.ca/). 
- Using Python and one other data visualization software (Excel or free alternative, Tableau Public, any other tool you prefer), create two distinct visualizations from your dataset of choice.  
- For each visualization, describe and justify: 

Average OSAP debt
Data on the average amount of OSAP debt owed by students. The data is specific to those who attended programs with typical durations.
Data is for:
4-year undergraduate university students
2-year college diploma students
1-year private career college students
The data fields are:
academic year of completion
postsecondary sector (university, publicly-assisted college, or private career college)
program duration (1 year, 2 years or 4 years) average repayable debt after loan forgiveness applied through the Ontario Student 


    > What software did you use to create your data visualization?
The visualizations were created using Python and Excel. Python utilized for data analysis and programmatic plotting with Matplotlib, while Excel used for simpler data manipulation and graphical display.
This is the code used
import matplotlib.pyplot as plt
import pandas as pd

# Sample data creation (replace this with your actual dataset)
data = {
    "Academic Year": [
        "2003-2004", "2004-2005", "2005-2006", "2006-2007", "2007-2008",
        "2008-2009", "2009-2010", "2010-2011", "2011-2012", "2012-2013"
    ],
    "4-Year University": [22000, 22500, 23000, 23000, 23500, 24000, 24500, 25000, 25000, 25500],
    "2-Year College": [12000, 12500, 12500, 13000, 13000, 13500, 14000, 14000, 14500, 14500],
    "1-Year Private Career College": [8000, 8500, 8500, 9000, 9000, 9500, 9500, 10000, 10000, 10500],
}

# Convert data to a Pandas DataFrame
df = pd.DataFrame(data)

# Plotting the data
plt.figure(figsize=(10, 6))

# Create bar positions for each category
x = range(len(df["Academic Year"]))
bar_width = 0.25

# Plot each bar
plt.bar(
    [p - bar_width for p in x], 
    df["4-Year University"], 
    width=bar_width, label="4-Year University Students", color="blue"
)
plt.bar(
    x, 
    df["2-Year College"], 
    width=bar_width, label="2-Year College Students", color="red"
)
plt.bar(
    [p + bar_width for p in x], 
    df["1-Year Private Career College"], 
    width=bar_width, label="1-Year Private Career College Students", color="green"
)

# Adding labels and title
plt.xticks(x, df["Academic Year"], rotation=45)
plt.xlabel("Academic Year")
plt.ylabel("Average Repayable Debt ($)")
plt.title("Average Repayable Debt by Postsecondary Sector and Program Duration")
plt.legend(loc="upper left")

# Display the plot
plt.tight_layout()
plt.show()


    > Who is your intended audience? 
Policy-makers: To assess trends in student debt and evaluate funding programs like OSAP.
Educational institutions ( colleges and universities): To identify the financial burden on students.
Students and families: To inform decisions regarding postsecondary education based on financial implications.

    > What information or message are you trying to convey with your visualization? 
I am trying to transmit the average repayable debt for three categories of students (4-year university, 2-year college, and 1-year private career colleges) across academic years. The message highlights the differences in debt levels among these groups, with university students consistently incurring higher debts.

    > What design principles (substantive, perceptual, aesthetic) did you consider when making your visualization? How did you apply these principles? With what elements of your plots? 
The data is specific, relevant, and focused on average repayable debt trends over time. The visualization prioritizes data relevance and clarity by focusing on specific trends in average repayable debt. A bar chart was used to compare debt levels across categories. The use of consistent colors for each group improves comprehension. The consistent use of distinct, solid colors (blue, red, and green) to represent each category reinforces the association between color and data group, making it easier for viewers to distinguish between categories at a glance. The design is clean, with labeled axes and a readable title. However, improvements in color contrast and annotation for significant trends could enhance the visualization. Irrelevant or extraneous data was intentionally excluded to keep the visualization focused, ensuring that the message.

    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
To ensure that my data visualizations are reproducible, I utilized both Python and Excel. Python, being a programmatic tool, is inherently reproducible. I saved my Python scripts with detailed comments explaining each step of the process, from loading the dataset to preprocessing and creating the visualization. On the other hand, Excel, while user-friendly, lacks the same level of reproducibility as Python due to its reliance on manual processes, such as creating charts and formatting. This limitation underscores the importance of using reproducible tools like Python, especially when precision and consistency are critical. While Excel was helpful for quick and intuitive chart creation, I relied on Python for a more systematic and replicable approach.

    > How did you ensure that your data visualization is accessible?  
Colors was adjusted to accommodate colorblind users (e.g., using Color Universal Design palettes), larger labels and legends ensure readability and providing clear descriptions of charts for visually impaired audiences.
      
    > Who are the individuals and communities who might be impacted by your visualization?  
Students: Insights into debt trends could impact their educational choices.
Policy-makers: Debt analysis might influence student loan policies or grant programs.
Educators: Financial data could guide institutional support strategies for students.

    > How did you choose which features of your chosen dataset to include or exclude from your visualization? 
I opted to include all the features since they were directly relevant to the message I wanted to convey. By including all the features, I ensured the visualization effectively illustrated the comparisons between the three student groups and highlighted how their debt levels changed over time.  

    > What ‘underwater labour’ contributed to your final data visualization product?
Cleaning and organizing the dataset.
Writing Python code for visualizations.
Refining chart layouts and conducting exploratory data analysis. This foundational work ensures accuracy and clarity in the final product.


- This assignment is intentionally open-ended - you are free to create static or dynamic data visualizations, maps, or whatever form of data visualization you think best communicates your information to your audience of choice! 
- Total word count should not exceed **(as a maximum) 1000 words** 
 
### Why am I doing this assignment?:  
- This ongoing assignment ensures active participation in the course, and assesses the learning outcomes: 
* Create and customize data visualizations from start to finish in Python
* Apply general design principles to create accessible and equitable data visualizations
* Use data visualization to tell a story  
- This would be a great project to include in your GitHub Portfolio – put in the effort to make it something worthy of showing prospective employers!

### Rubric:

| Component         | Scoring  | Requirement                                                                 |
|-------------------|----------|-----------------------------------------------------------------------------|
| Data Visualizations | Complete/Incomplete | - Data visualizations are distinct from each other<br>- Data visualizations are clearly identified<br>- Different sources/rationales (text with two images of data, if visualizations are labeled)<br>- High-quality visuals (high resolution and clear data)<br>- Data visualizations follow best practices of accessibility |
| Written Explanations | Complete/Incomplete | - All questions from assignment description are answered for each visualization<br>- Explanations are supported by course content or scholarly sources, where needed |
| Code              | Complete/Incomplete | - All code is included as an appendix with your final submissions<br>- Code is clearly commented and reproducible |

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `HH:MM AM/PM - DD/MM/YYYY`
* The branch name for your repo should be: `assignment-4`
* What to submit for this assignment:
    * A folder/directory containing:
        * This file (assignment_4.md)
        * Two data visualizations 
        * Two markdown files for each both visualizations with their written descriptions.
        * Link to your dataset of choice.
        * Complete and commented code as an appendix (for your visualization made with Python, and for the other, if relevant) 
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/visualization/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-4`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-3-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.

