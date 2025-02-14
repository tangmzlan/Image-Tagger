# AI Image Tag Tool For SD LoRA Training
The Image-Tagger is designed to automate image batch tagging during SD LoRA training. 

This tool refers to working principles of other image tag tools, but aims to further improving ease of use and accuracy. Therefore:\
- it uses model API instead of deploying models locally.\
- it allows you to use your preferred vision and LLM models on Aliyun Platform. After tests, qwen-vl-max can achieve pretty good result as vision recognition model. (better than Llama and CLIP)

Under the guidance of prompt, it first calls the visual recognition model to recognize the relevant content in the pictures, and then calls the large language model to streamline the recognized text (simplify the description into keywords and reduce the weight of irrelevant descriptions). prompt needs to be edited in excel file beforehand, and after importing the excel file, you can select the visual recognition as well as streamline the corresponding prompt. The prompt template file is currently provided for interior design scenarios.
