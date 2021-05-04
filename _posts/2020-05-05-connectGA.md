---
layout: single
comments: true
toc: true
toc_label: "Table of Contents"
toc_icon: "paw"
categories:
  - Github

title:  "How to connect Github Page with Google Analytics"
---

# Google Analytics 4 (GA4)   

Google offers Google Analytics for free. You can track and analyze your webpage using Google Analytics.
This is also important when you are trying to connect your page with any ad.
Google released new version of Google Analytics, GA4(Google Analytics 4).
Google Analytics 3 is refered to as UA(Universal Analytics).

# How to connect your Github Page(Esp. Minimal-Mistakes by Jekyll) with GA   

Make your own account through the link(https://analytics.google.com/) and follow the process as photo captured below.   
<img width="1223" alt="스크린샷 2021-05-05 오전 6 00 15" src="https://user-images.githubusercontent.com/81342538/117069571-9d772500-ad67-11eb-8e40-ead736c85f45.png">
<img width="1213" alt="스크린샷 2021-05-05 오전 6 00 54" src="https://user-images.githubusercontent.com/81342538/117069574-9fd97f00-ad67-11eb-8419-d8173ef5daf1.png">   

Then you will find this page.
<img width="1030" alt="스크린샷 2021-05-05 오전 6 01 50" src="https://user-images.githubusercontent.com/81342538/117069577-a10aac00-ad67-11eb-9aea-eebd69d27b48.png">
Please save or copy your "measurement ID". This is needed for the following process.    

In your `_config.yml` file, make `measurement_id:` and insert your measurement ID.   
The code will be shown like below:   

```
# Analytics
analytics:
  provider               : "google-gtag"
  google:
    measurement_id          : "INSERT YOUR MEASUREMENT ID HERE"
    anonymize_ip         : # true, false (default)
```    


In your `/_includes/analytics-providers/google-gtag.html` file, add a line of code written below:

```
gtag('config', '{{ site.analytics.google.measurement_id }}');
```
   
   
If you have any questions, feel free to comment below!
