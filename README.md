friendlister
============

A Facebook friend list tool.  A friend asked if smart lists could be smarter (specifically, she wanted the intersection of two lists, I believe).  So I figured I'd write this up.  Didn't think it'd take me that long, but it still ended up taking about 4 hours to whip together (between distractions and dinner).

This isn't fancy.  I figured for the first version, I'd write it completely in html and javascript.

Functionality supported:
1. Retrieve Facebook friend lists
2. Run a few set operations on a pair of lists to generate a new list
3. Editing of your new list
4. Store newly generated list to Facebook.

There's no way to delete a list or delete a friend from a list right now.  This is mostly because destructive actions are harder to make sure I don't screw up.

If people actually find this useful (Facebook's friend list editing tools are kinda sucky and awkward.  Not like this is _that_ much better.)


Installation Notes
=============
1. Create a Facebook application.
2. Get the App ID.
3. Change the appId on line 54 (in FB.init()).
4. Shove friendlister.html onto a server somewhere.
5. Update your Facebook application with the domain of your server, so there's no crossdomain whining from your browser.


Future Features
============
- Cronjob support.  So you could define rules and we'd periodically pull lists from Facebook and update lists you create with this app.  This is much more complex and requires a full backend + database.
- Search.  Typeahead search, ideally.  (I have the code for this already.  Just need to merge it into this tool.)
- Multiple list operations.  (list_A U list_B) - list_C would be kinda cool.