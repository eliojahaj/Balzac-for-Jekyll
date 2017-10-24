---
layout: post
title: "The-Architecture-of-Occupation-in-the-21st-Century"
description: "Midterm project reflection by Eden, Elbunit and Elio"
category: articles
---

The United States has a very strong international military presence. As of 2014 more than 800 U.S. military bases
have been officially recorded, but this number should be views as conservative considering recent proliferations as
the number of secret bases domestically and abroad. This militry presence is one of the main sources of power both 
for the U.S. goverment and U.S. capital, thus it actively shapes the project of American Imperialism. These imperial 
movements are increasingly considered as invasive by local inhabitants, consider here how the natives of Diego Garcia 
were forcefully displaced from their self-sufficent ansectoral lands to the slums of the Seychelles, or how the inhabitants 
of Okinawa have been treated by the military installation in this region. Largley inspired by Losh Begley's Prison Map porject,
we decided to investigate the architecture of occupation that is shaped by U.S. military installations in order to understand
their world-making impacts and what they mean for local cultures and life practices.

In order to do this we made the choice of using the Google Static Maps API, which allowed us to take a satellite picture of a 
location according to our own parameters such as zoom, size, annotations etc. We first collected and organized the langtitudes 
and longtitudes of a number of bases in the U.S. and abroad to serve as our testing sample. For this we used militarybases.com,
which is not officially affiliated with any governemnt agencies. After compiling this data, we wrote the following simple python script
to serve our testing purposes. 

```
import urllib


resource = urllib.urlopen("https://maps.googleapis.com/maps/api/staticmap?center=26.460693,127.916785&zoom=14&size=400x400&key=AIzaSyB6uNOMNhV-tJwKra3Oiy9fVJuE7XnQsGY")
output = open("file01.jpg","wb")
output.write(resource.read())
output.close()

print "Created map 1!"

resource = urllib.urlopen("https://maps.googleapis.com/maps/api/staticmap?maptype=satellite&center=26.460693,127.916785&zoom=14&size=640x400&key=AIzaSyB6uNOMNhV-tJwKra3Oiy9fVJuE7XnQsGY")
output = open("file02.jpg","wb")
output.write(resource.read())
output.close()

print "Created map 2!"
```




<figure>
	<img src="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg">
	<figcaption>Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</figcaption>
</figure>

{% highlight html linenos %}
<figure>
	<img src="/images/image-filename-1.jpg">
	<figcaption>Caption describing these two images.</figcaption>
</figure>
{% endhighlight %}
