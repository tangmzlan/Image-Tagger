# AI Image Tag Tool For SD LoRA Training
The Image-Tagger is designed to automate image batch tagging for SD LoRA training. 

This tool refers to working principles of other image tag tools, but aims to further improving ease of use and accuracy. Therefore:
- it uses **model API** instead of deploying models locally, so it's much more convenient to use and has **no requirement for GPU**.
- it allows you to use your preferred vision and LLM models on Aliyun Platform. After tests, **qwen-vl-max** can achieve pretty good result as vision recognition model. (better than Llama and CLIP)

Below are brief introduction of how the tool works:

**1. Vision Recognition:** Under the guidance of **Vision Prompt**, it first calls the visual recognition model to recognize the relevant content in the pictures;
**2. Tag Refinement:** Under the guidance of **Refine Prompt**, it then calls the large language model to refine the generated tag texts (the tag texts may be in natural language, which could be simplified into keywords to reduce the weight of irrelevant words). 
**3. Prompt Pre-editiing:** Prompt needs to be edited in excel file beforehand, and after importing the excel file, you can select the visual recognition as well as refining prompts. The prompt template file is currently provided for interior design scenarios.
**4. Tag Images:** Copy paste your image folder path, and click *Run Image Tagger* button. The tool will generate *Original Tags* and *Refined Tags* for each image in the folder, and a .txt file will be generated for each image of the same name, with *Refined Tags" in it.

Please refer to the illustration below:
![Illustration](https://github.com/user-attachments/assets/4ffc6783-14a7-4942-96d1-fb34da04681c)


**HOW TO GET MODELS (VISION & REFINE) AND API ON ALIYUN:**
1. go to [Aliyun Bailian (阿里云百炼)](https://www.aliyun.com/product/bailian). Or [Alibaba Cloud Modelstudio](https://www.alibabacloud.com/zh/product/modelstudio) if you're outside China.
![image for Aliyun Bailian](https://github.com/user-attachments/assets/7bd8659f-0814-444b-b40d-fc926319bb88)

2. Register your account and sign in.

3. go to [bailianconsole(百炼控制台)](https://bailian.console.aliyun.com/) you can select workspace, models, and get your API for all models here. You can also check the token costs.
![bailian console](https://github.com/user-attachments/assets/cbdfcd85-58ff-4898-b1ce-b1eef2e4c134)

4. Copy paste the name and API of your selected model to the *Model Info* section of the tool

WIP. The tool will be continuously improved upon advices.

