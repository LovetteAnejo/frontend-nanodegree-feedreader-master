# Project Overview

In this project you are given a web-based application that reads RSS feeds.
The original developer of this application clearly saw the value in testing,
they've already included [Jasmine](http://jasmine.github.io/) and even started writing their first test suite! Unfortunately,
they decided to move on to start their own company and we're now left with an application with an incomplete test suite.
That's where you come in.

## Important Note

This is a web based application so it won't run correctly offline

## Table of Content

- How to run the app
- How each test is `done();`
- Dependencies


### How to run the app

Make sure you have a good internet connection, then run the index.html file in the apps root folder.

### How each test is `done();`

- RSS Feeds
	- Test 1 `"are defined"`
	- Test 2 `"each object in allFeeds has a working url"`
	- Test 3 `"each object in allFeeds has a non empty name field"`
- The Menu
	- Test 4 `"all menu elements are hidden by default"`
	- Test 5 `"all menu elements hide when clicked and show like wise"`
- Initail Entries
	- Test 6 `"there is atleast one entry in the feed element"`
- New Feed Selection
	- Test 7 `"Feed changed!"`
	
#### RSS Feeds

> Test 1 `"are defined"`

For this test we first check if the allFeeds array var is defined,
Then check if the length of it is not zero.

> Test 2 `"each object in allFeeds has a working url"`

In this test we loop through every feed in the allFeeds array and check if its url property is defined,
Then check also if its url property is not nothing.

> Test 3 `"each object in allFeeds has a non empty name field"`

This test we also loop through every feed in the allFeeds array and check if its name property is defined,
Then check also if its name property is not nothing.

#### The Menu

> Test 4 `"all menu elements are hidden by default"`

This test simply checks the body for a class attribute called `.menu-hidden` which hides the menu elements

> Test 5 `"all menu elements hide when clicked and show like wise"`

This test grabs the clickable icon that toggles the `.menu-hidden` class on the body, and the calls the `.click()` method,
the first `.click()` hides it the while the second `.click()` show the menu elements, all that is check at these different `.click()` method call is if the `menu-hidden` class is there or not.

#### Initail Entries

> Test 6 `"there is atleast one entry in the feed element"`

This test checks if the feed container has anyfeed in them by checking the `childElementCount`,
And also checking if there is any element with the `.entry` class.

#### New Feed Selection

> Test 7 `"Feed changed!"`

This test calls the `loadFeed()` function and collects all the loaded feed, calls the function again and the collect the new feeds and loops through each feed and checks if they are thesame.

### Dependencies

> Internet Connection

Make sure you have a good internet connection for the app to run properly
