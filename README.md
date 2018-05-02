# redesigned-robot
Twitter and VaderSentiment
This app is a web app designed to show live and long-term sentiment graphs with Dash of twitter feeds using the tweepy api.
## Repo Contents: 
- `dash_mess.py` - front-end. Runs on local or external server
- `twitter_stream.py` - streams from twitter, creates database, runs in background.
- `config.py` - Words not in "trending"
- `cache.py` -  For caching purposes in effort to get things to run faster. 
- `db-truncate.py` - A script to truncate the infinitely-growing sqlite database. You will get about 3.5 millionish tweets per day, depending on how fast you can process. You can keep these, but, as the database grows, search times will dramatically suffer. 

## Quick start

- Clone repo
- install `requirements.txt` using `pip install -r requirements.txt`
- Fill in your Twitter App credentials to `twitter_stream.py`. 
- Run `twitter_stream.py` to build database
- If you're using this locally, you can run the application with the `dev_server.py` script.
- You might need the latest version of sqlite3
- Consider running the `db-truncate.py` from time to time (or via a cronjob), to keep the database reasonably sized.


socialsentiment.net
