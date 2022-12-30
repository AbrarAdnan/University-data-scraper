# Statistical Analysis of Top CS Universities

## Problem Statement
The goal of this project was to gather and analyze data on the top computer science institutions around the world, as ranked by the website [CS Rankings](https://csrankings.org/#/index?all&world) which is a metrics-based ranking of top computer science institutions around the world. The data we gathered includes information about university rankings, the count of geometric mean papers published across all areas, and the number of faculty members who have published papers in our areas of concern (Computer Architecture, Computer Networks, Computer Security, Operating Systems, Programming Languages, and Software Engineering). We took the ranking of the whole world from 2000 to 2022 and found approximately 500 universities.

## Data Collection
To gather the data, we used a Python script and the [Selenium](https://selenium-python.readthedocs.io/) library to scrape the CS Rankings website. An example of the raw data obtained from the website is shown below:
<br>
![image](https://user-images.githubusercontent.com/52294804/209989670-7b18be8a-5922-4c5d-bcb5-04109728c44a.png)
<br>

## Data Analysis
We used our scraped data to answer the following questions:

1. What are the top 10 universities in terms of ranking (along with their country names)?
2. What are the top 10 countries with the most number of universities?
3. What is the average ranking of universities in all countries?
4. Is there a correlation between the ranking of universities and the count and faculty number?

## Findings
We used [Tableau](https://public.tableau.com/app/profile/abrar.faiaz.adnan/viz/CSrankingsdemoproject/Dashboard1?publish=yes) to visualize and analyze our data. Some of our findings include:
1. American universities have the highest ranks, with Carnegie Mellon University having the highest rank.
2. America has the highest number of universities (172), followed by Germany (57 universities).
3. The average ranking of the top universities in Brazil, Norway, Finland, Czech Republic, Hungary, Malta, Greece,      Turkey, Iran, and UAE is over 300.
4. There is a strong correlation between the ranking of universities and the count and number of faculty members.

![image](https://user-images.githubusercontent.com/52294804/209989293-866157c5-3527-4bc3-8970-421700e33241.png)

## Building and Running the Source Code


1. Open the command prompt (Windows) or terminal (Linux/Mac) and navigate to the desired directory.

2. Clone the repository on your computer using the following command:
```bash
https://github.com/AbrarAdnan/Week-6-Project.git
```
3. Initialize and activate the virtual environment

On Windows:
```bash
virtualenv venv
venv\Scripts\activate
```
On Mac/Linux:
```bash
virtualenv --no-site-packages  venv
source venv/bin/activate
```
4. Install Dependencies
```bash
pip install -r requirements.txt
```
   
5. Run the scraper
```bash
python scraper.py --chromedriver_path <Location to the chromedriver>
```
For example: `python scraper.py --chromedriver_path "C:\Users\Adnan\Desktop\chromedriver.exe"`
6. After the script has finished running, it will save the scraped data in a file called best_uni_list.csv in the project directory.

# Notes
1. The chromedriver file is included in the repository
2. The code needs python to run. Download python for [Windows](https://www.python.org/ftp/python/3.11.0/python-3.11.0-amd64.exe), [Linux](https://www.python.org/ftp/python/3.11.0/Python-3.11.0.tgz) or [MAC OS](https://www.python.org/ftp/python/3.11.0/python-3.11.0-macos11.pkg).
3. While running the code, a window of Chrome will appear. You can see the website it is working on in real time. You can also check the console/terminal for additional output messages to get a better understanding of what is happening in real time.
4. The code will take approximately 10 minutes to run and produce output.
5. While loading the csv file into tableau, Taiwan needs to be identified manually or it'll not be recognized with tableau's country database.
