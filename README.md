# Cybersecurity-WEEK7-8-Assignment - WordPress Pentesting


Time spent: **6** hours spent in total

> Objective: Find, analyze, recreate, and document **(at most) five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) : XSS vulnerability in new post file with unsafe processing of file names
  - Summary: An attacker can create a specially crafted image file name which, when uploaded in WordPress,
             injectsmalicious JavaScript code into the application.
    - Vulnerability types: XSS
    - Tested in version: 3.9
    - Fixed in version: 4.6.1
  - GIF Walkthrough: <img src="xss_unsafe_file_name.gif" width="800">
  - Steps to recreate: 
    - download or choose a image file (png or jpg formate)
    - rename file name to exampleimage<img src=a onerror=alert('Hello')>.jpg or example...>.png
    - go to Media and upload this file
    - once user viewing this image, user will be attacked
  - Affected source code: https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0
