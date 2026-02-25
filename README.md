# podcast-to-ebook 
A Claude Code skill for Convert an English podcast transcript into a Chinese business biography eBook,in Walter Isaacson style. 

# How it Works
Designed for English podcast lovers who perferred reading texts with storylines other than spending hours listening to the full episode, often without fully understanding them. 

Best for English podcast manuscripts exceeding 20,000 words. The process automatically completes three stages: **translation and structuring, biography writing, and cover design prompt generating**（*Note that this skill does not include image generation.*）. Each stage proceeds only after manual review and confirmation before moving on to the next step. 

To generate a complete ebook, you need to combine the transcribed text and the cover. You can use Calibre or Typore, but Calibre is more recommended.

# Installation 
1. Required downloads：SKILL.md、translation_gudie.md、biography_writing_style.md、style_examples.md
2. Optional downloads：cover_google02.jpg、封面.jpg，for references only.

# File Structure Reference
<img width="1384" height="782" alt="image" src="https://github.com/user-attachments/assets/79b52ba3-9109-4b8c-9aa8-caa5e89d7e0c" />

## Description for file structure
⚠️ Just create a folder named "output"; the image is just a placeholder.

⚠️ "cover_[名称].png" is just a placeholder.

⚠️ You can omit the "scripts" section. I initially wanted to write a script to directly call Imagen 4（Nano Banana）, but abandoned the idea because the API was too expensive.

⚠️ Image generation can also use Claude (but I didn't want to waste my tokens for image generation...). If you want to call other image generation models, you can write a Python or JSON script under "scripts." Please consult AI for details.

# Usage
⚠️ Before coverting, please ensure your file structure is set up correctly.

⚠️ The transcript you want to convert needs to be placed in the src folder.

## user-triggered command“
-Start processing, transcript filename: [your specified name]

## Covert the transcript in three stages
### Stage one: Translation
1. Ask if you want to use the recommended model Claude Sonnet4.6, or you can change it to another model you like，which means you need to ensure that Anthropic can call the model's API.
   
2. After selecting a model, this stage will consist of four steps. The first step is Chapter Planning, the 2nd is Chapter-by-chapter translation, the 3rd is Merging all chapters to output the complete version, and the fourth step, reviewing, is to allow you to cross-check using other models to see if any factual errors have occurred.

3. Because models have a limited context window to handle, and the longer the window, the more prone they are to **Hallucinations**, I chose this chapter-by-chapter translation approach. Furthermore, each chapter will have subheadings, allowing you to clearly see the content structure of the episode, which will help you learn and understand better.

### Stage two
1. Ask if you want to use the recommended model Claude Opus4.6 or Opus4.5. **The Opus model** is the best choice. Extensive practical results show that Opus currently has the strongest ability to process long texts, while other models may not perform as well in writing.

2. You can modify the writing style to your preferred style by directly editing it in the Markdown file.It would be best to provide some reference excerpts from the original book.

3. If you are not satisfied with the output, you can retry it several times; or simply list the changes and let Claude execute them automatically. Try plan mode; you might find it inspiring.

### Stage three 
1. Ask if you want to switch to Sonnet 4.6，since the limit of Anthropic is terrifying.
   
2. Before generating the prompt, Claude will output 2-3 design proposals. You can then provide feedback and requests, including what text should be placed on the cover.

3. Based on my own experience, Imagine 4 produces the best image generation results. However, this requires a paid API call, which I opted out of (since I already have a Gemini Pro membership). If anyone has a cheaper method, please let me know.

# Output example
You will find two final files in the output folder: a translation file and a biography file, both in Markdown format.
<img width="668" height="678" alt="截屏2026-02-25 12 03 34" src="https://github.com/user-attachments/assets/9e69e7d8-ca0c-4376-a126-0681132e14e5" />

## features included:
- Book title
- A brief introduction of 500-600 words
- Title page containing 4-5 famous quotes
- Chapter Title and its subtitles
- Open-ended closing statement
- optional features which require your request: character lists below every chapter title；blocker concepts explanations
  
# Requirements
- Claude Code CLI or Claude code + VS Code（A graphical interface suitable for beginners）
- For Ebook generation: Calibre is recommended.

# Credits
Created by @hanyu-815 with Claude Code.
Credits to @zarazhangrui's prompt for turning @AcquiredFM podcast into a 300-page DIY physical book. 




