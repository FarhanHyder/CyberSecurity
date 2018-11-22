# Project 8 - Pentesting Live Targets
> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.
The six possible exploits are:

    Username Enumeration
    Insecure Direct Object Reference
    SQL Injection
    Cross-site Scripting
    Cross-site Request Forgery
    Session Hijacking / Fixation

Each version of the site has been given two of the six vulnerabilities

## Blue

Vulnerability #1 : Sql Injection

This takes place by injecting sql code directly into URL of the  parameter. We insert ' OR SLEEP(5)=0--' after thet php id which makes the page loading for a few seconds and not reponsive, then returning to the same page. We tried it for green target which didn't work and took us to the home page of salesperson. 


![week 8 sql_injection](https://user-images.githubusercontent.com/36938994/48818423-42792100-ed19-11e8-86dc-40f84cfbc87c.gif)

Vulnerability #2: Session Hijacking/Fixation

This vulnerabiility lets you log back into the site without having your login info. Just changing the session id from previous session (using previous session's id) would let you log in and letting the attacker to access your useful info.only works for the blue target.


## Red 
Vulnerability #3: Insecure Direct Object Reference

This vulnerability makes the hidden salesperson IDs accesiable and visible to others.While trying the same thing to green and blue target doesn't respond to anything. 

![week 8 idor](https://user-images.githubusercontent.com/36938994/48818511-9dab1380-ed19-11e8-84aa-70b6f41d1c38.gif)


Vulnerability #4 : Cross-Site Request Forgery

Staff database can be access and edit without a csrf token for the red target. While returns an invalid request for blue and green target for doing so. 

![week 8 csrf](https://user-images.githubusercontent.com/36938994/48818556-cb905800-ed19-11e8-882b-4b59dbb66d46.gif)
)

## Green

Vulnerability #5: Username Enumeration

Login Error message text become bolds if the person's user name exist and unbold if it doesn't exist revealing important information to the attacker. 

![week 8 user_enum](https://user-images.githubusercontent.com/36938994/48804481-bc41e800-ece2-11e8-8b22-747336d131dc.gif)

Vulnerability # 6: Cross-Site Scripting

This takes a script and aplplies it to the feedback section while finish that and try to login agiain the feedack pops up with your name and the XSS runs. Trying it on blue target, the xss doesn't run but still shows the message. 
XSS Script - <script>alert('Mallory found the XSS!');</script>

![week 8 css](https://user-images.githubusercontent.com/36938994/48818618-fd092380-ed19-11e8-94ee-9f569292bc58.gif)

## Bonus

## Build on Objective #3 (SQL Injection)

The Green and red site works perfectly for the database query. The user inject SQL code into the sales person page by requesting  salesperson.php?id=?' OR '1=1' which works for the Green and Red but failed when tried for the blue site.


