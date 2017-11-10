---
layout: default
---
[Home](https://stephgarland.github.io/NLP-Portfolio)<br>
[Project Timeline](https://stephgarland.github.io/NLP-Portfolio/timeline)<br>
[Scope](https://stephgarland.github.io/NLP-Portfolio/scope)<br>
[Depth vs. Breadth](https://stephgarland.github.io/NLP-Portfolio/depthVsBreadth)<br>
[CV](https://stephgarland.github.io/NLP-Portfolio/CV.pdf)

# [](#header-1)Depth-First vs. Breadth-First

### [](#header-2)Depth-First vs. Breadth-First in general:

Scrapy crawls by visiting a page, extracting all links from that page, and then repeating on each extracted link. 
Some links can, and commonly are, filtered out - like pages already visited in the current crawl, links that are outside the allowed_domains, and links that are beyond the depth_limit setting.

Nevertheless, the crawl pattern is tree like, for example:




This tree can be traversed in Depth-first order, or Breadth-first order. 
In the case of a complete domain crawl, traversal order isn’t so important; each method results in every page being visited, and that’s the objective! 
But in the case of an incomplete traversal, the representation of the website as a whole is going to be quite different depending on whether the data was being obtained depth or breadth first. 

In the above example, if the traversal was only able to get about halfway through the tree, the incomplete depth first traversal is going to have a very thorough representation of the Student branch, but would not get to the Alumni branch.
An incomplete breadth-first order traversal will do a shallow visit to all branches. 

#### [](#header-3)Traversal Settings in Scrapy:

Scrapy uses a LIFO queue by default, meaning it crawls in depth-first order. To change this, these lines are added to the project’s settings.py file:

DEPTH_PRIORITY = 1 <br>
SCHEDULER_DISK_QUEUE = 'scrapy.squeues.PickleFifoDiskQueue' <br>
SCHEDULER_MEMORY_QUEUE = 'scrapy.squeues.FifoMemoryQueue' <br>

### [](#header-3)Depth-first vs. Breadth-first for our project:

My current hypothesis is that a breadth-first traversal of one of our universities would gather the most representative data. Setting the depth_limit would allow for experimentation on both how much data we can get at different levels, and the impact of different volumes of data has on our word vectors. On a side note, one possible downside of using a depth_limit is that there may not be a depth_limit that is a one-size-fits-all for all of our target universities. 

Around week 10 I started experimenting with breadth-first crawls. Tests on small websites, or when a small depth_limit was set were promising. Once the depth-limit was increased, or was not imposed, results tended to vary. Often the crawl would abort because of memory exceptions. In some cases, the filesize of complete depth-first vs breadth-first traversals on the same website would be vastly different (when it ought to have been the same data, just in a different order.)
