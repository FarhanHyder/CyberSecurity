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

## Red 
Vulnerability #1: Insecure Direct Object Reference

This makes the hidden salesperson IDs accesiable and visible to others.While trying the same thing to green and blue target doesn't respond to anything. 

-- image 

## Blue

Vulnerability #2 : Sql Injection

This takes place by injecting sql code directly into URL of the  parameter. We insert ' OR SLEEP(5)=0--' after thet php id which makes the page loading for a few seconds and not reponsive, then returning to the same page. We tried it for green target which didn't work and took us to the home page of salesperson. 

-- image

## Green

Vulnerability #3: Username Enumeration

Login Error message text become bolds if the person's user name exist and unbold if it doesn't exist revealing important information to the attacker. 

![week 8 user_enum](https://user-images.githubusercontent.com/36938994/48804481-bc41e800-ece2-11e8-8b22-747336d131dc.gif)

Vulnerability # 4: Cross-Site Scripting

This takes a script and aplplies it to the feedback section while finish that and try to login agiain the feedack pops up with your name and the XSS runs. Trying it on blue target, the xss doesn't run but still shows the message. 
XSS Script - <script>alert('Mallory found the XSS!');</script>