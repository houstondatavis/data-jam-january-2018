# data-jam-january-2018

Since it's been freezing in houston recently, we thought it might be fun to have a dataset that takes stock of Houston's current mood. We pulled in data using twitter's api following the #houwx hashtag. [Justin Gosses](https://twitter.com/JustinGosses) pulled the dataset, and [Yulan Lin](https://twitter.com/y3l2n) worked on munging it. The csv contains a lot less information than the raw json dump from the api, but is more structured. The "long" tweets do not exist in the json in this repository 
## datasets

### houwx.csv
fields

- trunc_text: text of the tweet, potentially truncated
- text: the text of the tweet, not truncated
- id: id of the tweet
- favorite_count: number of favorites
- is_quote_status: if it was a quote
- retweet_count: how many retweets
- username: screen name of the user
- followers: number of followers of the user
- verified: whether or not the user is verified
- description: user's description in their profile
- user_location: user_location
- create_at: timestamp

### quotes.csv
- id: id of the quoted tweet
- original_tweet: original tweet text
- original_tweet_id: original tweet id
- original_user: the user who first posted the tweet
- quoted_text: the text that was "added" in conversation

### retweets.csv
- rt_id: id of the retweet
- original_tweet: original tweet text
- original_tweet_id: original tweet id
- original_user: the user who first posted the tweet

### houwx.json
this is the raw data, which contains many more fields, but is also a lot messier

You can read more about the JSON data structure here in the [Twitter API](https://developer.twitter.com/en/docs/tweets/data-dictionary/overview/intro-to-tweet-json).

### Example:
1. There is a <a href="SpaCY exploration.ipynb">jupyter notebook</a> in this repo as well that Justin Gosses created. It is messy and not docoumented (sorry), but gives an example how to examine some of the tweets in terms of their text using both python's native string functionality and the NLP (natural language processing) python library <a href="https://spacy.io/">SpaCY</a>.

2. There is also this great website that does some very nice dat visualization of any hashtag over the last few days. https://www.csc2.ncsu.edu/faculty/healey/tweet_viz/tweet_app/

3. A very basic Tableau viz is <a href="https://public.tableau.com/profile/justin.gosses#!/vizhome/Twitter_Scrape_HOUWX/Summary?publish=yes">here</a>.


