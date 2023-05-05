# STAT395_Network
STAT 395 Exploration Activity

Included in the network.py script is Python code which builds, draws, and calculates some basic statistics for a network created from Twitter data. The 
tweets in this data set were obtained for my research project in which my partner and I are attempting to build a proxy measure for homelessness rates
based on Twitter activity related to homelessness in the US. As such, all of the twetes in this data set are only those which contain the substring 
"homeless," and have associated locational data placing them in the US. Tweets were gathered from 2010-2021, inclusive. 

This directed network was designed to show how users are interacting with other tweets, and to hopefully determine whether there were any users in the data
set who perhaps had a very high engagement, meaning they tended to receive a lot of replies or quote retweets, or others who made a large number of replies
to other tweets but didn't receive many themselves. For this network, each node represents a unique Twitter account, and each edge marks either a reply or 
quote retweet made from the source account to a tweet on the target account. 

The only caveat to this network is that in order for an edge to appear, both tweets (the reply/quote retweet itself and the tweet being replied to/quote 
retweeted) must appear in the data set, that is, they must both contain the substring "homeless." Unfortunately, this did not prove to be a particularly 
interesting network. Out of over 900,000 tweets in the data set, a network of just 54 nodes and 24 edges was built. Additionally, the majority of those 
edges were self loops, indicating a large number of threads, or users replying to their own tweets in a long sequence, usulaly as a way of getting around
character limits. Therefore, although this network was interesting to make, network methods do not appear to be the best approach when moving forward with 
this data set. 

It should also be noted that a large number of metadata fields are included in the original data set, as they are useful for the other parts of my research
project. For this particular project, however, the only fields used were 'tweet_id,' 'tweet_type,' 'referenced_tweets,' and 'author_id.'
