# How to use this tool:
This tool was built to scrape job posting data from indeed.com.
The first block of code has imports for the required libraries, and also asks for a vocation and also a location. If
you enter a location, you need to change the commented out portion of code in the second block.
Once you have entered a vocation, the code will scrape the first 500 jobs posted on indeed (location, company, title, and a link).
Then the code gets the latitude and longitude for each job location. This chunk of code is pretty slow and could be optimized to be
significantly faster. After getting the locations for each job, we then plot it on a basic basemap and smooth the point dataset with 
a gaussian kernel. 

After visualizing the heatmap of the jobs, the code then plots a few word clouds of the job locations, titles, and companies.
We then visualize the data by state and a basic countplot so we can see which states have the most jobs for the specific vocation. After
visuzliaing all the basic statistics, the code opens all the job links and proceeds to scrape the text from the company website. What we
are after is the years of experience that are mentioned in each posting. The code scrapes both integers and words from the text string 
(think seven and 7) and compiles them into a list. If there is no years experience noted in the post it records a NaN.

There is a lot more we could do with this code as far as predicting where the next "hot spots" for certain jobs are. Feel free to 
contribute if you have some fun ideas.
