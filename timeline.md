---
layout: default
---
[Home](https://stephgarland.github.io/NLP-Portfolio).

<table>
  <tbody>
    <tr>
      <th align="left">Week Beginning</th>
      <th align="left">Main Task(s)</th>
    </tr>
    <tr>
      <td>July 24</td>
      <td>Readings: <br> 
          Deep Learning: Udacity playlist</td>
    </tr>
    <tr>
      <td>July 17</td>
      <td>Software installation on Project Room and personal machines:
        <ul>
          <li>Anaconda (Packet Manager)</li>
          <li>Spyder (Python IDE)</li>
          <li>TensorFlow (Deep Learning Library)</li>
          <li>Scrapy (Crawling Framework)</li>
        </ul>
        Readings:<br> 
          http://neuralnetworksanddeeplearning.com/chap1.html<br>
          https://www.tensorflow.org/get_started/get_started
      </td>
    </tr>
    <tr>
      <td>July 31</td>
      <td>
        Readings:<br> 
          http://neuralnetworksanddeeplearning.com/chap2.html<br>
         Tutorials: <br>
          https://www.tensorflow.org/get_started/mnist/beginners<br>
          https://www.tensorflow.org/get_started/mnist/pros<br>
      </td>
    </tr>
    <tr>
      <td>August 7</td>
      <td>
        Manual extraction of url’s for top 50 Universities:<br>
        https://docs.google.com/spreadsheets/d/1K-LVJaFuSOURrAQXglgk8k7mNqdjiPkUwshY5qhmFLw/edit?usp=sharing <br><br>
        Desired end web-extraction results outlined:<br>
        <ul>
          <li>One text file for each university. Should contain all header text, and paragraph text from that university’s website.</li>
          <li>Each line in the text file should represent all text from a single page.</li>
        </ul>
        Tutorials:<br>
          https://docs.scrapy.org/en/latest/intro/tutorial.html<br>
          https://www.lynda.com/Python-tutorials/Creating-crawler-Scrapy/521198/532912-4.html<br>
          https://www.lynda.com/Python-tutorials/Recursive-crawling/521198/532913-4.html<br>
      </td>
    </tr>
    <tr>
      <td>August 14</td>
      <td>
        Focused on concerns relating to not getting arrested, also known as ‘polite scraping’<br>
        Verified in scrapy docs that scrapy obeys robot.txt files by default<br>
        Verified in scrapy docs that scrapy creates an artificial delay between visiting pages when crawling.<br><br>
        Preliminary crawl testing on www.yale.edu<br><br>
        Readings:<br> 
          Scrapy docs (partial): https://docs.scrapy.org/en/latest/index.html<br>
          https://blog.scrapinghub.com/2016/08/25/how-to-crawl-the-web-politely-with-scrapy/<br>
      </td>
    </tr>
    <tr>
      <td>August 21</td>
      <td>
        Attempts to improve output format of yale crawl. Largely unsuccessful. <br>
        <ul>
          <li>Responses seem impervious to normal string manipulation, like character stripping and replacing</li>
          <li>Should output one result per line, but one result often spans many lines</li>
          <li>Attempts to remove/replace character codes are largely ignored</li>
        </ul>
       Discussed concerns about repetitious text fragments.<br>
       <ul>
        <li>Added url field to results for debugging. </li>
        <li>Limited text extraction to within the body element only</li>
       </ul>
      </td>
    </tr>
    <tr>
      <td>August 28</td>
      <td>
        My personal machine broke and was replaced. Fresh installs of required software.<br>
        Created a Crawler branch on the NLP github repo.<br><br>
        Readings:<br> 
          http://mccormickml.com/2016/04/19/word2vec-tutorial-the-skip-gram-model/ <br>
          https://colah.github.io/posts/2014-07-NLP-RNNs-Representations/ <br>
          Stanford lecture on word embeddings: https://www.youtube.com/watch?v=ERibwqs9p38 <br>
      </td>
    </tr>
    <tr>
      <td>September 4</td>
      <td>
        Obtained persistent storage on I drive for crawl results.<br>
        Discussed suspiciously small file sizes for crawls with Tom. Discovered there is a substantial difference between a crawl on www.yale.edu and yale.edu. <br><br>
        Readings:<br> 
          Various ELI5 explanations about domains and subdomains
      </td>
    </tr>
    <tr>
      <td>September 11</td>
      <td>
        Changed output crawler output from JSON file to CSV. Ran test crawls.<br><br>
        In preparation for extended holiday crawls:<br>
        Rounded up a couple more machines in the project room and installed required software. <br>
        Readings (about encoding):<br> 
          http://www.unicode.org/faq//utf_bom.html <br>
          https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/
      </td>
    </tr>
    <tr>
      <td>September 18</td>
      <td>
        Encoding difficulties and format largely fixed this week.<br><br>
        In preparation for extended holiday crawls:<br>
        Rounded up a couple more machines in the project room and installed required software. <br><br>
        Readings:<br> 
        https://www.w3schools.com/xml/xpath_intro.asp <br>
        https://www.w3schools.com/xml/xpath_syntax.asp <br>
      </td>
    </tr>
     <tr>
      <td>September 25</td>
      <td>
        Started holiday crawls, including a Breadth First vs. Deep First comparison of wm.edu/<br>
        By wednesday these had crashed due to out of memory exceptions. Went back to Scrapy docs in an attempt to learn why and how to prevent that<br><br>
        Readings:<br> 
        Scrapy docs (partial): https://docs.scrapy.org/en/latest/index.html
      </td>
    </tr>
    <tr>
      <td>October 2<br>October 9</td>
      <td>
          Break
      </td>
    </tr>
    <tr>
      <td>October 16</td>
      <td>
          CV workshop.<br><br>
          Readings:<br>
          Deep Learning with Python (Francois Chollet) Chapter 1<br>
          Learning Scrapy (Dimitrios Kouzis-Loukas) Chapters 1-3
      </td>
    </tr>
    <tr>
      <td>October 23</td>
      <td>
          Updated crawler based on Scrapy chapters:
          <ul>
            <li>Changed from generic crawler inheritance to CrawlSpider </li>
            <li>Changed from own logic for link extraction to Link Extraction library</li>
            <li>Added datetime field to each page-hit</li>
          </ul>
          Looked up user-agent setting, verified scrapy generates a default value.<br><br>
          Readings:<br>
          Deep Learning with Python (Francois Chollet) Chapter 2
      </td>
    </tr>
    <tr>
      <td>October 30</td>
      <td>
          Ran Depth vs Width Comparisons on Boston UNI from depth 1-5<br><br>
          Readings:<br>
          Deep Learning with Python (Francois Chollet) Chapter 3<br>
          Learning Scrapy (Dimitrios Kouzis-Loukas) Chapter 7
      </td>
    </tr>
    <tr>
      <td>November 6</td>
      <td>
        Portfolio preparation.
      </td>
    </tr>
    <tr>
      <td>November 13</td>
      <td>
        Technical Report and wrap-up meeting.
      </td>
    </tr>
    

  </tbody>
</table>

