# Recommendation systems applications
1. what to buy
2. where to eat
3. which job to apply to
4. who you should b friends with
5. personlize your experience on web(new platforms)
* two types
  1. content-based: figure out what a user's favorite aspects of an item are, and then make recommendations on items that share those aspects
  2. collaborative filtering: find similar groups of users, and provide recommendations based on similar tastes within that group
* Types of implementation
  1. memory-based: use the entire user-item dataset to generate a recommendation system
  2. model-based: a model of users is developed in an attempt to learn their preferences.
  
## Content-based
1.  build the user profile
2.  build content of set items matrix
3.  gain weighted feature set by multiply 1 and 2
4.  update a new user profile by normailize weighted feature
5.  gain a new weighted feature item by nultiply new user profile and feature set of predict items 
### Advantages and Disadvantages of Content-Based Filtering

##### Advantages
* Learns user's preferences
* Highly personalized for the user

##### Disadvantages
* Doesn't take into account what others think of the item, so low quality item recommendations might happen
* Extracting data is not always intuitive
* Determining what characteristics of the item the user dislikes or likes is not always obvious

# Collaborative filtering
* approaches:
  1. user-based: based on users' neighborhood
  2. item-based: based on items; similarity
  * different
    * user-based:based on users of the same neighborhood with whom he or she shares common preferences. 
    * item-based: similar items build neighborhoods on the behavior of users
## User-based
1. create similarity index of active user with others by using user ratings matrix
2. create weighted ratings matrix(user's neighbors about items) by multily similarity index and rating matrix
3. generate the recommandation materix by aggreate all of weighted rates

## Challenges
1. data sparity: user in general rate only a limited number of items
2. cold start: difficulty in recommendation to new users or new items

### Advantages and Disadvantages of Collaborative Filtering

##### Advantages
* Takes other user's ratings into consideration
* Doesn't need to study or extract information from the recommended item
* Adapts to the user's interests which might change over time

##### Disadvantages
* Approximation function can be slow
* There might be a low of amount of users to approximate
* Privacy issues when trying to learn the user's preferences
