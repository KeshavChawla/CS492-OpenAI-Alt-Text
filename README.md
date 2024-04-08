# CS492-OpenAI-Alt-Text
Using OpenAI's GPT4-Vision-Preview to Add Alt-Text to Images Missing Them &amp; Increasing Web Accessibility

[![Chrome Web Store Screenshot of Published Chrome Extension](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/assets/21203253/55f01370-4964-4929-9e88-acc7cc89b788)](https://chromewebstore.google.com/detail/alt-text-filler/lhjopjegmkjjljgealjmckdblmmekjki)


## Loading the Chrome Extension through the Google Chrome Web Store
1. Visit [https://chromewebstore.google.com/detail/alt-text-filler/lhjopjegmkjjljgealjmckdblmmekjki](https://chromewebstore.google.com/detail/alt-text-filler/lhjopjegmkjjljgealjmckdblmmekjki) and 
2. Click "Add to Chrome"
3. From the Extensions dropdown in chrome pin the extension and open the extension's menu to add your OpenAI API Key (see the section below on obtaining a key if you do not have one)

![Chrome Extension Drop Down Menu Options and Entry Box to Add OpenAI API Key](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/assets/21203253/d5092b79-5759-49c5-9cf9-6a340f06ed8c)

## Loading the Chrome Extension Locally
1. Go to [chrome://extensions](chrome://extensions)
2. Turn on the Developer mode switch in the upper right
3. Click on "Load unpacked"
4. Select the alt-text folder within our repo

## Obtaining and Loading an OpenAI API Key
1. Visit [https://platform.openai.com/api-keys](https://platform.openai.com/api-keys) and sign up/log in
2. Generate a new API key with (at minimum) model capabilities access (we specifically need /v1/chat/completions)
3. Copy and paste the new API key into the Chrome extension toolbar/settings pane and save

---

## Survey and Anonymized Results
[![Screenshot of a survey of different alt-text provided by OpenAI's GPT 4 Vision Preview, ChatGPT 4, and existing alt-text](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/assets/21203253/cb695f0a-4a1a-4aca-a48d-ed63b16d9ba8)](https://forms.gle/1poeXuf556G8oz6P6)

The survey our team conducted to assess whether responses generated by OpenAI's GPT4 Vision Preview and ChatGPT 4 were any bit comparable to existing alt-text can be found here [https://forms.gle/1poeXuf556G8oz6P6](https://forms.gle/1poeXuf556G8oz6P6)

Anonymized results of the survey can be found in this repo under the [survey folder](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/blob/main/survey/CS_492_Alt_Text_Survey_Anonymized.xlsx).

## Govermental Website Analysis

Research-based on our small-scale, non-intrusive polling of websites to determine the lack of existing alt-text can be found in the [research](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/tree/main/research) folder along with the [code](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/blob/main/research/webscrape.py) and the [raw data results](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/blob/main/research/output.csv).

The research revealed some interesting findings. We hand-sampled 30 images each that had an empty alt-text attribute and a non-empty alt-text attribute to check for compliance. This manual verification was needed as our web scraping tool cannot decide whether an empty alt-text image belongs to a decorative image or an image that provides the necessary context. Additionally, our web scraper can not determine the quality of an alt-text attribute, it can only determine if it's non-empty. 

1. Even though images followed our definition of compliance (non-empty alt-text attribute) according to the web scraper, it didn't guarantee that the quality of the alt-text provided enough details about the image. Below are some images that did not have useful alt-text. 
   The image below had an alt-text attribute of “Nicholas Forget tile”.
 
  ![unnamed (1)](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/assets/18638226/ad9f8465-bf73-40ed-b95a-bebd6b74e78a)

  This image below had an alt-text attribute of "tab-1".
  ![unnamed (2)](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/assets/18638226/30eabb3a-e99e-4a05-90df-7a9b0401a53c)

   This image below had an alt-text attribute of "play-icon", suggesting it was something name for/by developers. 
   ![unnamed (4)](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/assets/18638226/ff6b50ea-c8f5-4ee8-8434-608bda046715)

   These images were just a few we found that had non-empty alt-text attributes but didn't contribute any useful information.  

2. After going through 60 images, 30 of which had empty alt-text attributes, and 30 that had non-empty alt-text attributes, we noticed that $\frac{54}{60}$ or $90%$ of the images we looked at use alt-text attributes correctly. To determine the accuracy of our web scraper, we created a binomial confidence interval (with our calculations below). The $z$-score that we chose was %1.96% (that corresponds to the 95% confidence interval). With $\hat{p} = $\frac{54}{60}$ and $n = 60$   


![unnamed](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/assets/18638226/dac99f8e-5a01-4069-9990-578201935e5b)

   We calculated the 95% binomial confidence interval for the accuracy of our web scraper to be [82.4%, 97.6%]

   Thus, we are 95% confident that, after accounting for the error of our web scraper, 79.1% to 93.6% of images on Canadian governmental websites follow WCAG 2.0 guidelines.
