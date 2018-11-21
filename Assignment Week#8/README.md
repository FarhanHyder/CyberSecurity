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
Vulnerability #2: Insecure Direct Object Reference

This makes the hidden salesperson IDs accesiable and visible to others.While trying the same thing to green and blue target doesn't respond to anything. 

-- image 
## Green
Vulnerability #1: Username Enumeration

Login Error message text become bolds if the person's user name exist and unbold if it doesn't exist revealing important information to the attacker. 

![week 8 user_enum](https://user-images.githubusercontent.com/36938994/48804481-bc41e800-ece2-11e8-8b22-747336d131dc.gif)

