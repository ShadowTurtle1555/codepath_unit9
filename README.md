# Pen Testing Live Targets

Time spent: 10 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: SQL Injection. 

Description:Developer forgot to properly sanitize salesperson.php query.

<img src='sqli.gif' title='SQLI'/>


Vulnerability #2: Session Hijacking/Fixation. 

Description: Website does not check if user-agent is the same as the one used when first user login, cookie set without HttpOnly and secure flag, and PHPSESSID is not regenerated and is allowed to be a year old.


<img src='sessionhijacking.gif' title='Session Hijacking/Fixation'/>

## Green

Vulnerability #1:  Username Enumeration.

Description: Developer forgot to keep span tag class the same when username is or is not found, leading to vulnerability.

<img src='uerenumeration.gif' title='Username Enumeration'/>


Vulnerability #2: Cross-Site Scripting.
Description: Detected that Stored XS Script was run in admin feedback panel.

<img src='xss_.gif' title='Cross-Site Scripting'/>

## Red

Vulnerability #1: Insecure Direct Object Reference.

Description: Developer forgot to check if object reference request is made public or not. Other two websites properly redirected user to public/territories folder.

<img src='idor.gif' title='IDOR'/>


Vulnerability #2: Cross-Site Request Forgery.

Description:Developer forgot to check for CSRF token on salesperson edit form submit, check for domain name, and disallow loading responses onto iframes. 

<img src='csrf.gif' title='Cross-Site Request Forgery'/>

## Notes

Describe any challenges encountered while doing the work
