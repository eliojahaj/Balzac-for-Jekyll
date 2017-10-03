---
layout: post-no-feature
title:
description: Group work from Eden, Lucy and Elio
category: articles

---

For this assigment we chose to scrap the Wikipedia site of "Communism". (I solmenly swaer for the record that this was not my idea, but I can't say I wasn't into it.) The initial idea was to look at the amount of times "communism" and "capitalism" are mentioned in this article and then contrast that with the amount of time they are mentioned on Karl Marrx's 'Capital'. However, this resutled to be quite challenging for our skill level and before going into spoteneous combustion we decided to pivot, do a simple excersie to grasp some of the basic workings of web scrapping with Python.

The main challenge was to figure out a function that would tell us the amount of times that a sepcific word is repeated within an url. On top of that, we had to figure out how to do that for two separate urls. This part would've not possed diffculty if we could figure out an appropriate function as we could've made two separate python files.

Eventually, we settled on refining our skills and trying a random function. We created two files to get the text of the url as well as the word count. Additionally, we decided to print according to a random function. The results were random singular letters and characters, which poses the challenge of figuring out how to print full words or phrases while still adhering to a random function. The code we ended up with is attached below.

```
from bs4 import BeautifulSoup import requests import random import time

url = "https://en.wikipedia.org/wiki/Communism" result = requests.get(url) content = result.content soup = BeautifulSoup(content, "html.parser")

def get_text(url,text_file): text_on_site = (soup.get_text().encode('utf-8')) with open("communism.txt","w") as file: f.write(text) print "Created text file!"

def get_word_count(text_file, wordcount_file): with open(text_file) as f: wordcount = str(Counter(f.read().split())) with open(wordcount_file, "wb") as file: file.write(str(wordcount)) print "Check directory for file"

while True: print random.choice(content) time.sleep(1) 

```
