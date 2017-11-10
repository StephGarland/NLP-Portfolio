---
layout: default
---
[Home](https://stephgarland.github.io/NLP-Portfolio)<br>
[Project Timeline](https://stephgarland.github.io/NLP-Portfolio/timeline)<br>
[Proficiencies](https://stephgarland.github.io/NLP-Portfolio/proficiencies)<br>
[Reflection](https://stephgarland.github.io/NLP-Portfolio/reflection)<br>
[Scope](https://stephgarland.github.io/NLP-Portfolio/scope)<br>
[Depth vs. Breadth](https://stephgarland.github.io/NLP-Portfolio/depthVsBreadth)<br>
[CV](https://stephgarland.github.io/NLP-Portfolio/CV.pdf)

# [](#header-1)Personal reflective story

I came into the Machine Learning Project with a lot of excitement, and not a lot of specific expectations. Now I’m leaving the first half behind and I’m still feeling a lot of excitement towards this project, and have high expectations of myself and my work in the upcoming semester. 

Working on such an exploratory project is a significant change from anything I’ve undertaken before. I’m very used to time-frames, and marking schedules, and knowing that ultimately, a task is able to be completed given enough time and tinkering.

I was eager to make good progress, but struggled at times with how to define progress. I think I mostly interpreted progress as achieving the spec as fast as I could, but in my haste, neglected to really enjoy what should have been the focus - leaving a legacy of incredible documentation and Jupytor Notebooks. 

Throughout this past semester I did a fair amount of reading, and really enjoyed taking my time to understand the concepts I encountered. By week 2 I think I’d told just about everyone I know how a neural network of perceptrons works. Sometimes they were interested!

I expand on some of the following areas on separate pages, but here are some thoughts on some substantial aspects of my work:

## [](#header-2)Scope
Based on no evidence, I really thought I’d be able to complete all 50 crawls in about a week. It was pretty disarming to slowly realise how vast they really were. I’ve definitely learned a lot about using Scrapy and data-extraction in general. 

I was surprised when David was able to build a word vector from a crawl that had what would call pretty low-quality output. On reflection, I should have been attempting to make word vectors as a sort of gauge for output quality. 

Early on I was concerned about many pages having the same snippet of text, for example “It looks like you’re trying to zoom”, which occurred on many of the more top-level pages of the Yale website. In hindsight, I can now see that actually, when you’re getting samples from millions of pages, the model is robust enough to handle a few flaws in your dataset.

## [](#header-2)Depth vs. Breadth
This is something that David was pretty keen for me to look into, and it took a few goes for me to understand why. 

I was so sure that if my will was strong enough, everything would work out, and given enough time all the crawls would finish after traversing every page. Traversal order would never matter. 

Again, I think this was my naivety going into an exploratory project for the first time. It legitimately confused me to think that everything wouldn’t work as expected. I understood that if David kept bringing it up despite my foolproof logic, I must have been missing something. I’m pretty chuffed that I was able to have this realisation and act on it at the time by bringing it back and getting David to clarify why it was a thing the next time we met.

## [](#header-2)Tools
Learning new frameworks and libraries is hard work! I came into this project pretty scared of command windows. I’d still prefer a GUI, but now I flinch a little less if I don’t have that option.

This project has finally cemented what my Lecturers have been trying to instill: always start at the official docs. 
I initially experimented with a Scrapy crawler I built using a lynda tutorial. It worked okay, but the tutorial was more geared towards people trying to get a general gist of how crawlers worked in order to protect their websites. The appeal was that the tutorial was easy to understand and quick to set up. Unfortunately a lot of the implementation details were a little funky, and I ended up losing time trying to figure out weird kinks. There’s a beginner tutorial on the scrapy docs page, and I quickly realised my error in not starting there.
