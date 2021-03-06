---
layout: post
title: FB Reactions Python script
---

I was looking for a project to practice my rudimentary Python skills. When 
I read in Michael Bazzell's book (Open Source Intelligence Techniques) that he used
the Firefox add-on "Copy All Links" to get a list of a users' friends I started to play 
around with the idea.

I noticed that when I saved all the links after opening up a reactions pop-up window that
the urls associated with the reactions all had this parameter:
```
?fref=pb&hc_location=profile_browser
```

More interestingly, this common parameter is preceded by the person who "liked" the posts' username or profile id number:
```
https://www.facebook.com/example.username.9?fref=pb&hc_location=profile_browser
https://www.facebook.com/profile.php?id=100011111111111&fref=pb&hc_location=profile_browser
```

This gave me the idea of creating a Python script that could isolated these usernames and store them. This still requires
that I manually click on the "reactions" link in a group or person's FB feed and then copy those links using the Firefox Add-on.

There might be a way to automate this further. I am also wondering if there is a way to differentiate the different types
of reactions (sad, like, angry, ...).

For the moment, the data is stored in JSON format for simplicity. I am playing around with ways of saving this to a CSV file,
which would be more usefull for most users.

You can find the repository here: [FBReactions](https://github.com/BoredDunbar/FBReactions)

When testing it using the Buscador VM, I had to install tkinter which is the program that lets the script copy the content
of the clipboard. To install it open up the terminal and type:
```
sudo apt-get update
sudo apt-get install python3-tk
```

