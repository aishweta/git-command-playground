## Working with Bash Commands

Learning Bash commands helps data scientists quickly handle data, organize files, and automate tasks, making their work more efficient. It allows easy data access, improves project management, and helps them use powerful computers for big tasks. Knowing how to use the command line is crucial for anyone working with data, simplifying complex tasks and saving time. The following are just a few of the most common daily things.

Environment Variables
export VAR_NAME=value: Set an environment variable.

echo $VAR_NAME: Print the value of an environment variable.

env: List all environment variables.

env | grep KEYWORD: Search through all environment variables for a keyword.

File and Directory Operations
touch filename.extension: Create a new file or update an existing file's timestamp.

ls -a: List all files, including hidden files.

head -n 2 filename.csv: Display the first two lines of a file.

mkdir folder_name: Create a new directory.

curl -O [URL]: Download files from the internet using cURL with the -O option to save the file.

Navigation and Directory Management
cd folder_name: Change to a specified directory.

cd ~: Change to the home directory.

cd ~/Downloads: Change to the Downloads directory.

cd ..: Change to the parent directory of the current directory.

open .: Open the current directory in the file manager.

cd -: Go back to the last accessed folder.

Editing and Viewing Files
vim somebody.py: Edit a file using the vim editor.

nano filename.extension: Edit a file using the nano editor.

echo "text" >> filename.extension: Append text to a file.

mv source destination: Move or rename a file or directory.

Python Scripts and Command Line Operations
python script_name.py: Run a Python script.

command >> textfile.txt: Append the output of a command to a text file.

command > textfile.txt: Overwrite a text file with the output of a command.

cat filename.extension | grep keyword: Search for a keyword in a text file.

Additional Commands and Tips
source ~./zshrc: Refresh the terminal profile.

cat tom\ and\ jerry.txt: Access a file with spaces in its name by escaping the spaces.

echo $PATH: View the list of directories in your system's PATH variable.

python or python3: Run Python in interactive mode.

which python: Check the location of the Python interpreter.

Using Command Line Commands in Jupyter Notebook
Prefix commands with ! to execute them in a Jupyter Notebook (e.g., !ls, !cat filename.extension).

Handling Filenames with Spaces
Use backslashes (\) to escape spaces in filenames or wrap the filename in quotes.

Miscellaneous
pip list | grep conda: Use grep to search through the output of pip list for a specific keyword.

Environment setup and package management using Anaconda and argparse for script inputs are also crucial tools for data scientists working with Python and command-line interfaces.

Resources
Linux Command Line Basics: A free course on Udacity that introduces the Linux command line from scratch.
https://www.udacity.com/course/intro-to-programming-nanodegree--nd000

Bash Scripting Tutorial: Ryan's Tutorials offer a comprehensive guide to Bash scripting that is great for beginners and intermediate users.
https://ryanstutorials.net/bash-scripting-tutorial/

The Bash Academy: An interactive guide to learning Bash scripting through lessons and exercises.

GNU Bash Reference Manual: The official manual of GNU Bash for those who want a deeper understanding of its features.

Learn Shell Programming: Offers interactive Shell programming lessons for beginners.
