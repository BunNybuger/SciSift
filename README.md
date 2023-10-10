# [SciSift](http://poe.com/SciSift "Click here to try SciSift!")


Welcome to the SciSift repository!🤗 With SciSift, you can effortlessly extract information from papers—even directly from PDFs—and save it in your desired format, be it JSON, markmap, HTML, etc. Simply dump a collection of PDF papers and retrieve JSON files for each. Then, utilize the provided code to merge these JSON files, producing a comprehensive table with all the extracted details from your papers! I've tested SciSift on dozens of papers that I previously read and synthesized manually. The results? Absolutely remarkable. In a few seconds, SciSift extracts information, perhaps even better than I could!

SciSift is powered by a robust language model named Claude. This model can process documents containing up to 100,000 tokens, ensuring the efficient extraction of vital details. Such capacity enables us to read an entire paper in one go—something that is harder to do with ChatGPT.


## How to try SciSift? 

Currently, the easiest method is through this link: [poe.com/SciSift](https://poe.com/SciSift). Simply click on the link and upload your paper! Please note that only the first few attempts are free. Sorry! This is Poe's policy, not mine.

If you have an account with Claude, you can also run it directly on [claude.ai](http://claude.ai). However, you'll need to copy the prompt yourself.

## Background

I'm a PhD student immersed in the realm of Machine Learning. Navigating through a scoping review, I felt the weight of keeping current with the daily influx of new papers in my field. Pondering this challenge, my supervisor mused, "Why don’t you have an LLM sift through these papers for you?" Surprised, I asked, "Is it okay to do that?"🤔 He replied, "Yes, as long as we're transparent about our methodology and clearly mention how we did that!"

And thus, SciSift was conceived. 😊

## Contribute

SciSift is still in its early stages and was initially tailored to meet my research needs. However, with your help, its capacity to adapt and cater to a wider demographic is undeniable. Interested in contributing? Check out the prompt file, modify it to suit your requirements, and submit a pull request. Your contributions will be acknowledged, ensuring others can access and benefit from them in your name.❤️❤️


## SciSift Prompt

```md
Your task is to extract the information delimited by triple quotes from the text of a scientific paper. The scientific paper is attached. I need you to read the paper carefully and extract the following information from the text.
The information should be returned in JSON format. Make sure it is a readable JSON file with no error. All the responses should be as concise as possible. If a particular piece of information is not present in the text, please indicate "info not provided." 
Information to extract:

"""
1.	Article name
2.	Citation (In-text citation of the article in APA 7th style)
3.	Year of the article
4.	DOI
5.	Brief summary (Main objectives and findings of the paper)
6.	What is detected in this paper?
7.	Detected object hashtag: (Specify the primary objects or subjects that are detected and name what is detected in each category, for example what kind of PPE is detected? Or what type of actions ? etc. you can use list below but feel free to add new categories if needed
a.	PPE
b.	Actions
c.	Body posture )
8.	Method and the technology employed in the paper for detection: (and provide details on how it was implemented.)
9.	Primary focus: (Indicate whether the paper's primary focus is related to detection with #vision, #audio or any other methods.)
10.	Other technologies or tools used: (List any technologies and tools used in the paper and specify them.)
11.	Method of measuring performance (Explain how the paper measures performance, provide details)
12.	Achieved performance (give me the number)
13.	Key points and the value of the research (Identify key points in the paper and highlight the value of the research.)
14.	Suggestions or recommendations for future research (Summarize any suggestions or recommendations for future research provided in the paper.)
15.	Limitations (Highlight any limitations mentioned regarding the work.)
16.	Dataset (Specify the dataset(s) utilized in the paper and provide the details how they made or accessed the dataset)
17.	Sharing Dataset? (specify if writers are willing to share their dataset)
18.	Personal ideas or insights (Share any personal ideas or insights that came to mind after reading the paper.)
19.	Funding (specify who funded the research)
"""
```


<p align="center">
  SciSift website: <a href="http://scisift.pro/">SciSift.pro</a>
</p>