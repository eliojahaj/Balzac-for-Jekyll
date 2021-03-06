---
layout: post
title: "The Architecture of Occupation in the 21st Century"
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
to serve our testing purposes. A main challenge for our code moving forward, also based on our thencical skills, is integrating a csv file where all the coordinate information is stored, which can be used to automatically take satellite imagery of these locations. At this time, the following script is still quite manual. 

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

There are roughly two main types of maps we can collect from Google Maps. The first one below is a representational map as opposed to staellite imagery, which allows us to analyze various political and to some extent demographic trends that spur up from the U.S. military base in Okinawa, Japan. This map allows us to make some easy inferences about political subdivisions and their surrouding geography, but overall they do not provide much intricate information as to how the architecture of bases is shaped by and shapes occupation itself.  

<figure>
	<img src="https://image.ibb.co/nL2L0m/file01.png">
	<figcaption>Map of Okinawa featuring the U.S. military base</figcaption>
</figure>


The second type of map, which is really at the crux of this project is exemplified by the following satellite image of Okinawa. Although this map lacks annotations at this moment, they can easily be added through specified parameters to the Google Maps API. This map allows us to intricatley analyze details that go beyond political subdivisions, they provide us a snapshot of the architecture of the base itself and how it differs from that of the city. This image in particular demonstartes how foreign occupation constantly trades on keeping the other at its boundaries. Juxtaposing the first map with the second shows us how clearly delinated are the borders between the base and its surrdoing area. More intricate parameters will allow for more intricate renderings and readings of these sites. Moreover, the crux of the project is also based on comparing deomstic U.S. bases with international bases and will be develped further as the project advances. 
<figure>
	<img src="https://image.ibb.co/jW3Sfm/file02.png">
	<figcaption>Satellite map of Okinawa featuring the U.S. military base</figcaption>
</figure>

Ultimatley, we were able to figure out how to carry this process out with a very simple script upon which we can positvley build in order to carry out more challenging tasks. However, the project at this stage needs to develop around a system of visual representation that allows for the reader to make visual inferences from the maps. 
