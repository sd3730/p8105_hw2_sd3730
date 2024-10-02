Problem 0
This “problem” focuses on structure of your submission, especially the use git and GitHub for reproducibility, R Projects to organize your work, R Markdown to write reproducible reports, relative paths to load data from local files, and reasonable naming structures for your files.

To that end:

create a public GitHub repo + local R Project; we suggest naming this repo / directory p8105_hw2_YOURUNI (e.g. p8105_hw2_ajg2202 for Jeff), but that’s not required
create a single .Rmd file named p8105_hw2_YOURUNI.Rmd that renders to github_document
create a subdirectory to store the local data files, and use relative paths to access these data files
submit a link to your repo via Courseworks
Your solutions to Problems 1, 2, and 3 should be implemented in your .Rmd file, and your git commit history should reflect the process you used to solve these Problems.

For this Problem, we will assess adherence to the instructions above regarding repo structure, git commit history, and whether we are able to knit your .Rmd to ensure that your work is reproducible. Adherence to appropriate styling and clarity of code will be assessed in Problems 1+.

Problem 1
This problem focuses on NYC Transit data; in particular, this CSV file contains information related to each entrance and exit for each subway station in NYC. If you’re not familiar with the NYC subway system, keeping a map in mind while looking at these data might help.

Read and clean the data; retain line, station, name, station latitude / longitude, routes served, entry, vending, entrance type, and ADA compliance. Convert the entry variable from character (YES vs NO) to a logical variable (the ifelse or case_match function may be useful).

Write a short paragraph about this dataset – explain briefly what variables the dataset contains, describe your data cleaning steps so far, and give the dimension (rows x columns) of the resulting dataset. Are these data tidy?

Answer the following questions using these data:

How many distinct stations are there? Note that stations are identified both by name and by line (e.g. 125th St 8th Avenue; 125st Broadway; 125st Lenox); the distinct function may be useful here.
How many stations are ADA compliant?
What proportion of station entrances / exits without vending allow entrance?
Reformat data so that route number and route name are distinct variables. How many distinct stations serve the A train? Of the stations that serve the A train, how many are ADA compliant?

Problem 2
This problem uses the Mr. Trash Wheel dataset, available as an Excel file on the course website.

Read and clean the Mr. Trash Wheel sheet:

specify the sheet in the Excel file and to omit non-data entries (rows with notes / figures; columns containing notes) using arguments in read_excel
use reasonable variable names
omit rows that do not include dumpster-specific data
round the number of sports balls to the nearest integer and converts the result to an integer variable (using as.integer)
Use a similar process to import, clean, and organize the data for Professor Trash Wheel and Gwynnda, and combine this with the Mr. Trash Wheel dataset to produce a single tidy dataset. To keep track of which Trash Wheel is which, you may need to add an additional variable to both datasets before combining.

Write a paragraph about these data; you are encouraged to use inline R. Be sure to note the number of observations in the resulting dataset, and give examples of key variables. For available data, what was the total weight of trash collected by Professor Trash Wheel? What was the total number of cigarette butts collected by Gwynnda in June of 2022?

Problem 3
This problem uses data on elements of the Great British Bake Off. The show has been running for 10 seasons; in each episode, contestants compete in signature challenges, technical challenges, and a showstopper. At the end of an episode the winner is crowned “Star Baker” (and winner in the last episode of a season), and a loser is eliminated.

Information about individual bakers, their bakes, and their performance is included in bakers.csv, bakes.csv, and results.csv. In the first part of this problem, your goal is to create a single, well-organized dataset with all the information contained in these data files. To that end: import, clean, tidy, and otherwise wrangle each of these datasets; check for completeness and correctness across datasets (e.g. by viewing individual datasets and using anti_join); merge to create a single, final dataset; and organize this so that variables and observations are in meaningful orders. Export the result as a CSV in the directory containing the original datasets.

Describe your data cleaning process, including any questions you have or choices you made. Briefly discuss the final dataset.

Create a reader-friendly table showing the star baker or winner of each episode in Seasons 5 through 10. Comment on this table – were there any predictable overall winners? Any surprises?

Import, clean, tidy, and organize the viewership data in viewers.csv. Show the first 10 rows of this dataset. What was the average viewership in Season 1? In Season 5?

