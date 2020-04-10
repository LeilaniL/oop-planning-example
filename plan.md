// A user can post a tweet that consists of a short text message and their username.

// A user can post a tweet and view it in their news feed.

// A user can view a news feed that shows the tweets of other users they follow.

// Can “Like” a tweet and see that tweet’s Likes increase.

// Can retweet another user’s tweet.

// Nouns = objects
// User
// Tweet
// Newsfeed

// Verbs = methods that go along with an object
// User
// - Post
// - Like
// - Retweet
// - Follow

// Tweet
// - increaseLikes
// Newsfeed
//  - Show

function User(name) {
  this.userName = name;
  this.tweets = [];
  this.followers = []
  this.follows = [];
}
User.prototype.post = function (message) {
  var newTweet = new Tweet(message);
  this.tweets.push(newTweet);
}
User.prototype.like = function (tweet) {
  tweet.likes += 1;
}

function Tweet(text) {
  this.text = text;
  this.likes = 0;
  this.retweets = 0;
}

function Newsfeed() {
  this.posts = []
}

Newsfeed.prototype.show(userId) {

}