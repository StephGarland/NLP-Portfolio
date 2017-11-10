---
layout: default
---
[Home](https://stephgarland.github.io/NLP-Portfolio)<br>
[Project Timeline](https://stephgarland.github.io/NLP-Portfolio/timeline)<br>
[Scope](https://stephgarland.github.io/NLP-Portfolio/scope)<br>
[Depth vs. Breadth](https://stephgarland.github.io/NLP-Portfolio/depthVsBreadth)<br>
[CV](https://stephgarland.github.io/NLP-Portfolio/CV.pdf)

# [](#header-1)Scope
Around week 6, Tom posited that it might be quicker to manually visit each page, and just copy/paste the desired text. 
It sure seemed that way at times, and I think it took quite a bit of exploring to understand just how vast these crawls are. 

One of the websites I crawled that ended with a memory exception was on Princeton University (princeton.edu).<br>
It ran from 6.31pm on 21/09/2017 to 7.36pm on 23/09.2017.<br>
It searched ~1,876,251 pages, and gave me (NUMBER) samples for the Princeton file. <br>
The file is 3,624,844 kb. <br>
To put this in perspective, Harry Potter and the Philosopher’s Stone as a .txt file is 479 kb - it would need to repeat 7,568 times to be of a similar size to the .txt file that contains the text scraped from the incomplete princeton.edu crawl. 

I’ve been running a crawl on The College of William and Mary (wm.edu) since 29/09/2017, and as of 9/11/2017 it has yet to complete. 

## [](#header-2)Responding to the realisation of scope:
I realised how massive these projects were shortly after solving my domain vs. sub-domain mystery in week 8.<br> 
(To recap briefly, up until that point I’d been setting ‘allowed_domains’ as www.example.edu, when setting it as example.edu was yielding a much more whole representation (LINK TO INFO PAGE)

Following this realisation I made a few deliberate choices:

### [](#header-3)Revisiting the spec:
The word vector examples I was finding did not need such vast amounts of text in order to build a decent word vector. David was able to confirm this by using the 40,410 kb output from an early test crawl on Emory University to make a word vector that made some amount of intuitive sense. <br>
I started to run breadth-first tests, and experimenting with depth-limits in the hopes that that would produce a dense but broad representation of different aspects of an individual university’s website. 

### [](#header-3)Output format and encoding needed to drastically improve:
When each crawl takes the good part of a week, time needed to be spent on making the output as close to spec as possible. I’d been working on improving this alongside other tasks, but decided to make this my greatest priority. Week 9 saw reductions in the amount of encoding appearing within the responses, and by Week 10 the format spec was achieved. 

### [](#header-3)Preparing for the long crawl:
Each crawl would need to run interrupted for many days. I prepared three project room machines with the intention of using them as dedicated crawlers. Three, because that’s how many spare Ethernet wall jacks I could find. David also offered the use of a couple of computers on the third floor. <br>
I monitored the strain simultaneous crawls put on each computer, and determined five each was the magic number. When I checked back the next day, many had aborted due to out-of-memory exceptions. While I suspect this was due to a few different reasons, I have yet to retry more than two simultaneous crawls on any given machine. 


## [](#header-2)Improvements that could have been made:

Encoding still appears in the output files. I don’t know how to eliminate it completely, but chapter 3 of the book ‘Learning Scrapy’, by Dimitrios Kouzis-Loukas introduced me to ItemLoaders and MapCompose(), both of which are promising data-processing leads that I just didn’t find the time to look into extensively.

Scrapy allows crawls to be paused and resumed using ‘Jobs’. https://doc.scrapy.org/en/latest/topics/jobs.html. I haven’t yet used this functionality, but it seems really helpful.
