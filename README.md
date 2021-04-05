Black Businesses Matter - README 
===

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
Connect users with black-owned businesses. Garner more support and income for black-owned businesses. Develop long-standing relationships between the advertised businesses and the consumers. Could potentially be used for startup black businesses to promote their businesses.


### App Evaluation
- **Category:** Social Networking/Lifestyle
- **Mobile:** This app is only accessible on mobile devices 
- **Story:** Analyzes user's preferences and connects them to businesses that suit them. The user can also personalize their feeds and try new products. 
- **Market:** Any individual can use this app. Especially those that are interested in finding new businesses to support and include in their every day life. 
- **Habit:** This app can be used day to day or whenever the user needs a new place to shop.
- **Scope:** First, the user's location is used to display nearby Black owned businesses on their home feed. Then hopefully, this can lead to a relationship with these businesses as well as other customers. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

[ X ] User can sign up
[ X ] User can sign in
* User stays signed in 
* User can leave a review
* User picks their favorite businesses
* Profile page for each user

**Optional Nice-to-have Stories**

* Log of most visited businesses
* Businesses can create an account
* Users can rate businesses
* Business page shows how far away from user businesses are located
* User can personally add a business
* Users can search for specific businesses 

### GIF
<img src="https://github.com/BBMGroupProject/unit-10/blob/main/Screen%20Recording%202021-03-28%20at%206.26.00%20PM.gif" width=600>

### 2. Screen Archetypes

* Lauch Screen
* Login
    * User can login 
* Sign Up
    * User can register 
* Home
    * User can view businesses nearby
    * User can "favorite" businesses
    * User can search for businesses
* Category
    * User can select business categories
* Favorites
    * User can view Favorite Businesses or unfavorite.
* Post
    * User can post promotions.
* Profile
    * User can upload profile picture
    * User can view all previous reviews

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Home
* Category
* favorites
* Post
* Profile

**Flow Navigation** (Screen to Screen)

* Launch screen
* Login/Signup screen
   * Home
* Category
   * Home
* Favorites
   * None
* Post
    * Home 
* Profile 
    * None 

## Wireframes

<img src="https://github.com/BBMGroupProject/Unit8/blob/main/IMG-2846.jpg" width=600>

<img src="https://github.com/BBMGroupProject/Unit8/blob/main/IMG-2846.jpg" width=600>


### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 

### Models

## Login/Sign Up

| Property | Type   | Description                            | 
| -------- | ------ | -------------------------------        | 
| password | String | Unique id for the user to login/signup |
| username | String | Unique id for the user to login/signup | 
| LoginBTN | Button | Button for users to login              | 
| SignUpBTN| Button | Button for user to sign up             | 


## Home


| Property     | Type   | Description                        |
| ------------ | ------ | ---------------------------------- |
| businessName | String | Name of business                   |
| location     | String | Business address                   |
| description  | String | Description of business            |
| category     | String | Category of business               |
| review       | String | User can view and leave reviews    |
| website      | String | Link to business website           |
| reviewCount  | Number | Number of reviews under post       |
| image        | Image  | Image of business                  |
| createBTN    | Button | Button for user to add businesses  |
| isFavorited  | Bool   | Records when presses favorite icon |
| favorite_img | Icon   | User can favorite business         |


## Categories
| Property  | Type  | Description                                         |
| --------  | ----- | ----------------------------------------------------|
|categoryBTN| Button|User clicks on this to view the different categories |
|fashionBTN | Button|User clicks on this to view fashion related business |
|foodBTN    | Button|User clicks on this to view food related business    |
|serviceBTN | Button|User clicks on this to view services related busines |
|productsBTN| Button|User clicks on this to view product related business |

## Favorites


| Property     | Type   | Desciption                                      |
| ------------ | ------ | ----------------------------------------------- |
| favorite_img | Icon   | Signifies user favorites business               |
| businessName | String | Name of business                                |
| favoriteBTN  | Button | User clicks this button to view favorite screen |

## Add Business



| Property       | Type   | Description                      |
| -------------- | ------ | -------------------------------- |
| addDescription | String | Input of description of business |
| addLink        | String | Input of website link            |
| addLocation    | String | Input of business address        |
| addCategory    | String | Input of business category       |
| addBusiness    | String | Input of business name           |
| addPhoto       | File   | Image of business                |

## Profile



| Property  | Type   | Description                              |
| --------- | ------ | ---------------------------------------- |
| reviewBTN | Button | Holds current list of the user's reviews |
| photo     | File   | Uploaded image for user profile picture  |


### Networking
List of network requests by screen:

* Home feed screen
1. (Create/POST) Create a new review on business post
2. (Delete) Delete review
3. (Create) Create a new "liked" post
4. (Delete) Undo "liked" post

* Profile screen
1. (Read/GET) Query logged in user object
2. (Update/PUT) Update profile picture
3. (Update/PUT) Update user's reviews

* Favorites screen
1. (Update/PUT) Update user's favorites
2. (Delete) Remove favorites
3. (Read/GET) Save user's current favorites

* Login/Sign up page
1. (Read/GET) Query logged in user object
2. (Read/GET) Query signed in user object
