---
layout: post
title: "The Internet Was Designed"
category: articles
---

The right to be forgotten is not a straightforward issue. Moreover, the debate around it entirely rests upon broadly defined, unspecified iterations of the word public and privacy. We must seriously ask weather there is something inherently different about privacy online that doesn’t translate as well in the non-virtual world. While it is true that the practically infallible memory of the internet is in serious mismatch with the working of human memory, in the non-virtual world, once something has been said it cannot be taken back unless through an apology, which is not an erasure, but in fact a recognition of the offense in the first place. As the right to be forgotten applies mostly to things that other people have said about you, the issue is quite different: it is a struggle for the right to curate your own persona. Privacy has come to mean very different things, it is a retreat from social life where one does not have to put on a public face. Perhaps what this struggle over the right to be forgotten has shows us is that the visions around the emergence of the net were themselves based in notions that favored the individual over the social. This should also remind us that the internet is not teleological, neither in the sense that it arose due to humanity’s unquestionable technological process nor in the sense that its current iteration is inevitable. When thinking about the right to be forgotten we must think about our very notions of privacy, their history and our specific contextual use - if this concept is key to the debate we can’t use it as a ahistorical buzzword. 

```
import csv  


term_list = [] 
with open ('queries_2017.csv', 'rb') as csvfile:
	reader = csv.reader(csvfile, delimiter = '\t')
	for row in reader:
		term_list.append(', '.join(row))
		

for item in term_list:
	if "murder" in item:
		print item 
```


