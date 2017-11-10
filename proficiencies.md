---
layout: default
---
[Home](https://stephgarland.github.io/NLP-Portfolio)<br>
[Project Timeline](https://stephgarland.github.io/NLP-Portfolio/timeline)<br>
[Proficiencies](https://stephgarland.github.io/NLP-Portfolio/proficiencies)<br>
[Project Timeline](https://stephgarland.github.io/NLP-Portfolio/reflection)<br>
[Scope](https://stephgarland.github.io/NLP-Portfolio/scope)<br>
[Depth vs. Breadth](https://stephgarland.github.io/NLP-Portfolio/depthVsBreadth)<br>
[CV](https://stephgarland.github.io/NLP-Portfolio/CV.pdf)

# [](#header-1)Technical Proficiency:

## [](#header-2)What is the overall quality of your code like?

This project did not have a vast amount of code. That said, the code I did write is well-commented, with sensible method and variable names. I think the flow makes sense, and that I successfully avoid surprising the reader. 

It was important to me to avoid fragility, as I hoped to run the same script on all 50 universities, and have it easily adapted to future projects. I think I largely achieved this, as I have yet to find a university website that I have needed to change my spider for.

While it’s possible to be very specific with XPath selections, and to automatically generate expressions using chrome, these expressions do not respond well to changing page layouts. I very deliberately chose my selectors so that they would be applicable to almost any page.

## [](#header-2)How well did you follow best practices in development?

I tried to incorporate scrapy best practices as I discovered them. I initially had my own method for writing output to file, but switched to using feed-exporters after reading about them in the docs. Similarly, I had my own method for extracting and following links, but changed to the Link Extractor library upon my discovery of its existence. 

I could have improved my work in a few ways here:
For a long time I thought I was using scrapy Items, which are a kind of wrapper for a dictionary. I discovered recently that I was just using a dictionary, and hadn’t noticed. 
Along with Items, I haven’t yet implemented the use of Item Loaders and Item Pipelines - both recommended scrapy tools. 

## [](#header-2)How well did you use appropriate version control?

Again, although the crawler code wasn’t extensive, I tried to use version control as best as I knew how. My commits were modular, and I was quick to push any changes. I kept crawler development on a separate branch until it was mostly completed. I made sure to exclude crawler output from the online repo, but still keep it accessible on the I:Drive for the rest of the group.

I could definitely have improved on repo documentation. Beyond code comments and a very difficult to read .txt file, I didn’t commit information on how anything is used. This was a huge part of my research, and should have been a huge part of my repository.

## [](#header-2)To what extent do you think you contributed an equal portion of the overall project?

Although there wasn’t much cross-over between my work and Tom’s this semester on this project, I do think that this will be an important tool going forward for a range of projects. I’m happy I spent a lot of time exploring this area, as data extraction is a hugely important part of Machine Learning.

# [](#header-1)Professional Proficiency: 

## [](#header-2)How often do you attend scheduled group meetings/scrums?

I missed one scheduled group meeting, but was able to give prior notice. I met up the next day with David. I attended all other meetings. 

## [](#header-2)How well did you communicate with others in your group or subgroup?

The other person in my sub-group was Tom. I really enjoyed working with Tom, and we communicated often and well.  Although there wasn’t a lot of overlap in our tasks, we touched base frequently. My web-development and theory knowledge base is a weak-point for me, and by communicating frequently he was able to help me understand some important parts of my work. It was owing to Tom discussions that I solved a bug with my allowed_domains, thought to select text elements from the html <body> tag only, and realised that my crawler was crawling page-a-day calendars up until the year 9999. 

## [](#header-2)How well did you document your work throughout the project?

Not well. Documentation is such an important part of a research project, and David made sure to remind me and make sure I knew how to use Jupytor Notebooks. It wasn’t a personal priority for me, and it absolutely should have been. I hope to make documentation a strength in the coming semester.

## [](#header-2)How well did you respond to problems or changing requirements?

I think I communicated well about problems during group meetings. I was open about obstacles I was facing or that I anticipated, and brought back concerns if I felt I hadn’t understood something. 

This project didn’t have a client, so changing requirements came from new discoveries about the scraping process. These changes came about from necessity rather than whim, so weren’t emotionally compromising. 

Sometimes it felt like I was stuck on something every week, but having the group meetings as a bit of an outlet/recap made it easier to see that different problems every week is progress! And when problems stuck around for a bit, like the encoding/output issues, it was nice to take a step back and invest time in readings. 
