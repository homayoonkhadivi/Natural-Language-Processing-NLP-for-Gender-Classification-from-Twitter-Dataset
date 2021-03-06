![DMBUXwJVAAEFdM4](https://user-images.githubusercontent.com/57557590/107415235-5b539400-6b28-11eb-97e1-fa95c364719d.jpg)

# Natural-Language-Processing-NLP-for-Gender-Classification-from-Tweeter-Dataset
With the help of Natural Language Processing NLP, I could identify the gender classification from the Tweeter Dataset

# This file contains of:
* Loading the dataset:

This data set was used to train a CrowdFlower AI gender predictor. You can read all about the project here. Contributors were asked to simply view a Twitter profile and judge whether the user was a male, a female, or a brand (non-individual). The dataset contains 20,000 rows, each with a user name, a random tweet, account profile and image, location, and even link and sidebar color.

![Kaggle](https://user-images.githubusercontent.com/57557590/107414632-825d9600-6b27-11eb-974c-9695c50ac847.PNG)

The dataset comes from here: https://www.kaggle.com/crowdflower/twitter-user-gender-classification

# Inspiration
Here are a few questions you might try to answer with this dataset:

* how well do words in tweets and profiles predict user gender?

* what are the words that strongly predict male or female gender?

* how well do stylistic factors (like link color and sidebar color) predict user gender?

# The Data
The dataset contains the following fields:

* unitid: a unique id for user

* _golden: whether the user was included in the gold standard for the model; TRUE or FALSE

* unitstate: state of the observation; one of finalized (for contributor-judged) or golden (for gold standard observations)

* trustedjudgments: number of trusted judgments (int); always 3 for non-golden, and what may be a unique id for gold standard observations

* lastjudgment_at: date and time of last contributor judgment; blank for gold standard observations

* gender: one of male, female, or brand (for non-human profiles)

* gender:confidence: a float representing confidence in the provided gender

* profile_yn: "no" here seems to mean that the profile was meant to be part of the dataset but was not available when contributors went to judge it

* profile_yn:confidence: confidence in the existence/non-existence of the profile

* created: date and time when the profile was created

* description: the user's profile description

* fav_number: number of tweets the user has favorited

* gender_gold: if the profile is golden, what is the gender?

* link_color: the link color on the profile, as a hex value

* name: the user's name

* profileyngold: whether the profile y/n value is golden

* profileimage: a link to the profile image

* retweet_count: number of times the user has retweeted (or possibly, been retweeted)

* sidebar_color: color of the profile sidebar, as a hex value

* text: text of a random one of the user's tweets

* tweet_coord: if the user has location turned on, the coordinates as a string with the format "[latitude, longitude]"

* tweet_count: number of tweets that the user has posted

* tweet_created: when the random tweet (in the text column) was created

* tweet_id: the tweet id of the random tweet

* tweet_location: location of the tweet; seems to not be particularly normalized

* user_timezone: the timezone of the user

# Data Cleaning
### Regular expression RE =>> "[^a-zA-Z]"
### Description lower
In computer language, "BAND" and "band" words are understood differently. So I am going to convert all letters into lowercase
### Stopwords
Using word_tokenize method instead of split is more beneficial. Because, for example if you have a word like "shouldn't". split method cannot divide it into two parts but word_tokenize divide it into two parts : should and n't.
### Word tokenize method
### Lemmatazation
**This part, I am going to find root of letters (lemmatization) in order to do classification.**
### CountVectoizer
![download](https://user-images.githubusercontent.com/57557590/107987103-b41ca400-6fe2-11eb-95b7-6fd2d83d314d.png)

The CountVectorizer provides a simple way to both tokenize a collection of text documents and build a vocabulary of known words, but also to encode new documents using that vocabulary.
### Bag of Words


# Building Model:


