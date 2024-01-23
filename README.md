# moviestowatch

Use Case: List of Movies I want to watch at some point.  
Can’t find where I can stream them online at the time I want to watch them and don’t want to search away for hours. So this Make Scenario does the hard work for me.

Using a Google Sheet to track which movies to watch, this Make Scenario searches JustWatch and updates the google sheet with the places each movie can we watched.

# How to Use

1. Make a copy of the Google Sheet and Add in the movies you want to search for.
2. Import the Make Scenario and create a new Webhook URL (Noting the unique URL for your new Scenario)
3. Link the Google Connections to your Google Account and Sheet.
4. Update the Top left hand link in the Google Sheet with a link to your own Webhook.
5. When you want to update the availability of the Movies on your list click on the Google Sheet Link to Update.

# How the Scenario Works

Once initiated via the webhook, the scenario reads the google sheet line by line looking for movie titles, it uses Col Q to get the URL to www.justwatch.com and searches for the movie title, then parses the HTML looking for the first movie in the list and using that URL to feach the details of where you can stream the movie from cleaner page (one movie to the page). Finally the scenario searches for the icons of the places the movie can be streams and updates the rows in the google sheet with details.  This repeats for every row with a movie title. 
