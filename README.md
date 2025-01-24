# Google-Gemma-hackathon
Kaggle competition - Google - Unlock Global Communication with Gemma
kaggle link to competition: https://www.kaggle.com/competitions/gemma-language-tuning

# About Dataset:

Introduction

The stories in this dataset are a collection of mythological, cultural, and moral stories for children that were published in popular Chandamama Telugu monthly magazines. The stories are written in simple language and use characters such as animals, thieves, saints, old men, and kings.

The stories are collected from the following 2 websites and are freely available by the publisher.
1. https://chandamama.page/stories/telugu/
2. https://tsstudies.blogspot.com/search/label/Chandamama%20Kathalu

Data Processing

- Website 1 has huge collection of stories, but are available as scanned images of the original print magazines from the publisher. Images are verified for clarity and suitable story content and then copied and arranged for text extraction.
- Website 1 has few stories already available in text format. 
- "BeautifulSoup" and "tesseract-ocr" libraries are used to extract the text from stories (not all, but a few) and the link to corresponding notebooks are mentioned at the end. Extracted stories are spell corrected and divided into logical chunks manually after thoroughly reading and understanding each story.

Column Description

The dataset is split into train, validation, test sets and has the following columns.
| Column | Description |
| --- | --- |
| Prompt | Often refers to the main characters or moral in the whole story.  |
| Title | The original title of the story in the magazine. |
| Part | The original stories are usually long, so they were split into chunks based on scene changes, sections, etc. This was done to address the context length limitations and to ensure story continuity during finetuning. Most of the stories are split into 3 or 4 parts, the longest being 9 parts. |
| Story | Part of the whole story. |

* All the column values are in Telugu.


# Notebooks:

For details on finetuning approach refer notebook google_gemma2-Finetuning

For performance evalaution and inference Usage refer notebook Gemma2_PerfEval_Inference

Notebooks used for Data collection:
- https://www.kaggle.com/code/jagadeeshvana/pre-processing-beautifulsoup
- https://www.kaggle.com/code/jagadeeshvana/pre-processing-ocr