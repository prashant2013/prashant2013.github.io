---
layout: post
title: "Simple Web Crawler"
date: 2013-06-13 08:29
comments: true
categories: 
---
A Simple Web Crawler can be done in Python by using just two of its libraries:
{% blockquote %}
*	BeautifulSoup &
*	Requests
{% endblockquote %}

Install these packages by using either of pip or apt-get commands in Python environment:

{% codeblock Installing Libraries %}
sudo apt-get install python-bs4 OR
sudo pip install BeautifulSoup4
sudo pip install requests
{% endcodeblock %}

Now the sample code to fetch text on the webpage:
{% codeblock code %}
from bs4 import BeautifulSoup
import requests
url=requests.get("http://www.crummy.com/software/BeautifulSoup/bs4/doc/")
soup=BeautifulSoup(url.content)
print (soup.get_text())
{% endcodeblock %}

The link mentioned here is also a reference site for crawler, please visit and read first.
