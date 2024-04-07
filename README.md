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

Research based on our small-scale, non-intrusive polling of websites to determine the lack of existing alt-text can be found in the [research](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/tree/main/research) folder along with the [code](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/blob/main/research/webscrape.py) and the [raw data results](https://github.com/KeshavChawla/CS492-OpenAI-Alt-Text/blob/main/research/output.csv).
