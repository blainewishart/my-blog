---
title: Possible roadmap for one of our blogs
date: "2019-11-07:02:30"
---
### A learning path for either bog implementation designed for learning JavaScript
#### New Blog Engries -- definition
1. I think blog engries should be in fles with the date as a name
1. All other information belongs in the front matter
1. We need a good way to handle too much front mater or not enough
    1. slug: is the blog entry title
    1. author: one of us for now
    1. date is not needed, but...
    1. time: is optional
    1. tags: is optional
    1. location: is optional
    1. image: is optional but highly deserable. 
    1. public: boolean is devaults to private if missing
#### Implementation for new blog entries
1. at first, they come from file system
1. if there is no time appended to date, use value of file creation
1. build an in-memory collection of entries
    1. put in a hash map with date + time as key (later we will look in multiple locations including db
    1. build the page on a persistent canvas w/o pagination
    1. use cards to guide user
    1. organize cards by month
    1. entries w/o a graphic will include something random from some image collection
#### Non-post documents
1. we want some docs which evolve. for instnce a page showing the current approach to setting up Elm
1. we will probably start by modifying an existing blog, but once we know a bit more, 
we should extend GitBook to support a the blog modeled after the individual section at first
#### use of GraphQL
1. user can filter based on GraphQL schema 
1. subscriptions will be supported with default LIFO presentation so blog is a little like sorted slack
````
one filter would be by author,tag, location sorted by reverse date 
````
### what we will learn
1. scroolable canvas
1. SSR to build full pate
1. graphQL schema. and then GraphQL subscriptions 
1. use of basic data structures
1. how to combine a roadmap with a prioritized feature list

### process going forward
1. these notes are a litte contracictory
1. we will discuss and modify road map
1. we will identiry about 20 hours work to get started
1. we are green. we should expect several false starts
1. we will probably limit the first work engineering prototypes and not try to integrate
    1. track one
        1. example: take a folder sull of markdown, use the file name to build an inmemory collection of entires.
        1. persist it
        1. take persistent enries and add new entries and persis
        1. persistance could be file system or db
    1. track two
        1.    starting with a persisted set of entries, use SSL
