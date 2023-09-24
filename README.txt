# PubMed automated scraper tool ############################################################

This is a python tool designed to scrape newly posted papers from PubMed that contain
target keyword(s) and repost the articles to twitter. This script is primarily designed 
to be scheduled and run automatically.


This script requires two text files in the directory to operate properly:

1. doi_db.txt - This should contain the article DOIs of papers line by line that the 
		operator wishes to exclude from the bot. Reposted articles will 
		automatically be added to this file. (Format: 10.xxxx/xxxxxxxxxxx)

2. topics.txt - This file should contain the search terms line by line that the operator
		wishes to be run by the tool. The query is case sensitive and has no inbuilt 
		knowledge of abbreviations - any abbreviations should be listed as a
		separate search query in the topics.txt file. (Example: Staphylococcus aureus)


Configuration of PubMed scraping:

On line 122 [bot_search = pubmed_scrape(t, 'INPUT YOUR EMAIL HERE', 15)] of main.py the user 
must insert their email before running the script.


Configuration of twitter reposting function:

To configure twitter reposting functionality the use must add their twitter credentials in
the main.py file. The tool requires the api key, secret api key, bearer token, access token,
and secret access token. These should be inserted into the publish_twitter() function where
marked by: INPUT YOUR XXXX KEY/TOKEN HERE.


Any additional setup questions should be sent the author (GitHub: CPalmer3200)

