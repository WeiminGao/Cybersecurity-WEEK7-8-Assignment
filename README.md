# Cybersecurity-WEEK7-8-Assignment - WordPress Pentesting


Time spent: **5** hours spent in total

> Objective: Find, analyze, recreate, and document **(at most) five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) : XSS vulnerability in new post file with unsafe processing of file names
  - [X] Summary: An attacker can create a specially crafted image file name which, when uploaded in WordPress,
                 injectsmalicious JavaScript code into the application.
    - Vulnerability types: XSS
    - Tested in version: 3.9
    - Fixed in version: 4.6.1
  - [X] GIF Walkthrough:
  - [X] Steps to recreate: 
    - download or choose a image file (png or jpg formate)
    - rename file name to cengizhansahinsumofpwn<img src=a onerror=alert('Hello')>.jpg or ...>.png
    - go to Media and upload this file
    - once user viewing this image, user will be attacked
  - [X] Affected source code: https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0
