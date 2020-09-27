# CISC3140-Lab-5
Task 1 Terminal Activities:
Objective: Select a column file from a CSV file using the terminal software
How I approached this task
1.	I started off creating and opening a new directory folder for myself to work within called task1.
2.	Then I downloaded a movie lens zip file using the “curl -O http://files.grouplens.org/datasets/movielens/ml-latest-small.zip” command, unzipped the file using the “unzip ml-latest-small.zip” and tried to sample one of the csv files by returning the first 12 lines using the command “head -n 12 movies.csv”.
3.	I ran into the problem of only being returned html script and not the actual contents of the csv, so I used Google to search for a solution. I quickly found out the problem was due to myself not using the “cd” command to go into the newly zipped file.
4.	I then started over and used the “cd ml-latest-small” command after unzipping the file and when I used the head command, I was returned the first 12 lines within the actual file.
5.	To extract the file that contained the movie names and put them in alphabetical order, I used the command line “cut -d, -f2 movies.csv | sort | uniq”
6.	I then took the command and results and put it within the text file Task1.txt. Due to the csv file being too large, only a certain amount of the sorted column were displayed within the screen.

Task 2 Terminal Activities:
Objective: Create a shell script version of task 1
How I approached this task:
1.	I knew what I wanted to put within the script file, my only problem was creating it and opening the actual file. So, after many different google searches, I found a YouTube tutorial where the person within the video used the “vim” command to create a new file.
2.	After using the vim command and the editor appearing, I typed in “#! /bin/bash” then enter and began typing out the same commands as that I used for task 1.
3.	After typing the commands, I had some issues with finding out how to save the script file and exit the editor, but after more searching and trial and error, I found out to hit the esc button, then type “:xa”
4.	After exiting the vim editor, I typed the command “chmod +x csvscript.sh” to make the file executable
5.	Lastly, I used the command “./csvscript.sh” to execute the file and make sure that it worked
