HackerNewsDownloader
====================

##Introduction##
This is a small program to download Hacker News (HN) stories and comments using public official APIs. The code uses REST APIs to retrieve items and paginate through time. It respects API rate limit of 10,000 requests per hour.

Hacker News: https://news.ycombinator.com/
Hacker News Public APIs: https://hn.algolia.com/api

##Points of Interest##
The output is json file containing array of objects. Each object is the response object that was returned by API call. Within this object `hits` property contains actual list of items.

As the output files are very large, the code uses JSON.NET is streaming mode to read and write very large JSON files. It also uses RestSharp for making API calls.

##Data Files for Download##
The output generated by this program as of May 29, 2014 is available at https://github.com/sytelus/HackerNewsData. This contains all of the stories and comments posted on HN from 2006 to 29 May, 2014. Please see that repo for more information and download links.