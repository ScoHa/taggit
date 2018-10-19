# Taggit

## Overview
The purpose of this web application is to add hashtag functionality to reddit, utilizing first a web portal, and later tying into the reddit UI either as a Chrome/Firefox extension or as part of RES.

## Portal
Initial versions of this app will operate primarily using a web app utilizing React and a database (TBD). Users will be prompted to submit a link and up to five hashtags. While typing hashtags, the database will be queried for similar previous entries, encouraging users to use pre-existing tags for posts. Eventually there will be a system to up- and downvote tags based on relevance to the link. This will allow tags to be removed if they were added maliciously or were misleading in some way.

Users will be able to search for posts using hashtags similar to how other sites use them, Twitter in particular. Clicking a tag under a post will query the database and return all posts with that tag, sorted algorithmically either by relevance (perhaps weighted by the tag's weight on the post?) or chronologically.

### Portal features
- Form for submitting a reddit link (shortlink prefered)
    - Field to enter up to five (5) hashtags (taggs?)
    - Submit button
        - Submit button creates database entry containing a link reference to the post, the tags (obj or arr?) and, optionally later on, information about who submitted the tags, datetime information about the tags.
    
## Reddit bot
A reddit bot could be made that leaves a comment on tagged threads indicating that the app exists, that this post was tagged, and listing the tags (clickable links). This could help to spread awareness of the app and create avenues for people to discover new posts related to their chosen tags.

Comment would be set up similar to the wiki bot, where downvoting the bot to -1 will automatically delete the comment. Also, a blacklist could be set up where subreddit mods can turn the bot off from commenting in their subreddit.

## Subreddit
If /r/taggit is able to be acquired, the subreddit can serve one of a couple purposes.
- As a repository for tagged posts, which are automatically crossposted there,  or
- A subreddit discussing/tracking app development