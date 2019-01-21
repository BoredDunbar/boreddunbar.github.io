---
layout: post
title: Searching Gab
---

While social media newcomers like Gab, Mastodon or Dispora have not yet displaced the big players,
these platforms do provide valuable material for OSINT researchers. Here is a quick look at Gab.

## What is Gab?

Gab has gained the reputation of being "Twitter for nazis". The CEO, Andrew Torba, lauched the site as a
response to the perceived censorship of conservative voices by tech companies like Facebook and Twitter.
Gab prides itself as being the "free speech platform". While calling all Gab users nazis is an over-simplification
the site has definitely attracted a very right-wing user base.
 
## Gab search parameters

One thing of interest to OSINT is that it is not necessary to be logged in to perform searches. Creating an anonymous 
account on Gab is simple. There is no mandatory email verification step and unlike what is becoming more common with
 Twitter or Facebook, the service does not require a mobile phone number.

### General Search

Searches result in urls with the following structure:

https://gab.ai/search/*keyword*

Search results can be filtered by adding the following url parameter after the term being searched:

- https://gab.ai/search/*keyword*/top
- https://gab.ai/search/*keyword*/latest
- https://gab.ai/search/*keyword*/users
- https://gab.ai/search/*keyword*/groups
- https://gab.ai/search/*keyword*/topics

So if I wanted to search for a Gab user with the username *mysecretidentity*, all I would need to do is enter
*https://gab.ai/search/mysecretidentity/users* in a web browser address bar to get a list of users from Gab's search
function.

### usernames

A user's posts can be viewed by using the following url structure:

https://gab.ai/*username*

A user's list of followers can be displayed this way:

https://gab.ai/*username*/followers

### Hashtags

It is possible to search the platform for specific hashtags. They are displayed with the following url structure:

https://gab.ai/hash/*hashtag*

By default, they are displayed with the most recent post at the top. You can however, order them by popularity:

- latest: https://gab.ai/hash/*hashtag*/date
- top: https://gab.ai/hash/*hashtag*/score
