#####################################################################################
ScrapeScript_YouTube_v2-2.py

Script for scraping a comments on a YouTube video using...
Homepage URL: https://www.youtube.com/
Tools: Selenium, Chrome Driver
Data Organizer: Pandas

Version: 2.2
Date Created: 02/05/2019
Last Modified: 03/14/2019
#####################################################################################

#####################################################################################

ABOUT V2-2:

1. Added functions to handle and get styled usernames.
   This function is called if no username is detected for a post after
   first trying to use the original function to get normal usernames.
2. Added function to make custom comment IDs called "My Comment ID" in output.
3. Added function to make list of URLs for output
   where len(URLs) = len(comments) and all items are the same video URL.
4. Added function to get video's title from top of page below the video player.
5. Added function to make list of video titles for output
   where len(video_titles) = len(comments) and all items are the same video title.
6. Changed global variable v_code to automatically get code from URL:
   v_code = myURL.split("v=")[1]

#####################################################################################



##### READ ME #######################################################################

This script is able to scrape YouTube video comments on:
https://www.youtube.com/

This script's code should only be executed at portions at a time due to
Chrome Driver being unable to open the given webpage all the time.
Please do not run this script as an executable / as a whole.

##### WARNINGS ######################################################################

1. This script is prone to errors when scraping videos with 2,000+ comments.
   Videos with 1,500+ comments are iffy...
   This is because the browser has trouble displaying many comments at once on
   one page, so if the browser crashes or the page becomes unresponsive,
   the script will no longer work.
2. Please do not scroll or click anywhere on the browser window where Chrome Driver
   is operating while the script is trying to click buttons or extract data.

##### READ ME (continued) ###########################################################

Before running this script:
1. Change the values of the global variables in the "GLOBAL VARIABLES" section
   as necessary. Please read the notes attached to each when changing the value.
2. Reminder: If you change the value of any of the global variables, please
   re-run the "GLOBAL VARIABLES" section before executing any code that uses
   the global variable you changed or updated.

When running this script:
1. Messages will print out to the terminal to indicate where the code is
   currently at during execution.
2. If the webpage does not load when Chrome Driver starts, please manually
   reload the page in the same window until the webpage loads. If the webpage
   is appearing to take a long time to load, please try manually refreshing the
   page until it loads.
3. Please allow the webpage to fully load before moving on.
4. Suggestion: After the page loads, please manually pause the video if you do
   not want it to play while the script runs the next pieces of code.
5. Reminder: Please manually scroll down the page past the description to get the
   first few comments to load before executing the piece of code to scroll to
   the very bottom of the page.

#####################################################################################
