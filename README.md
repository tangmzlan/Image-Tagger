# AI Image Tag Tool For SD LoRA Training
The Image-Tagger is designed to automate image batch tagging for SD LoRA training. 

This tool refers to working principles of other image tag tools, but aims to further improving ease of use and accuracy. Therefore:
- it uses **model API** instead of deploying models locally, so it's much more convenient to use and has **no requirement for GPU**.
- it allows you to use your preferred vision and LLM models on Aliyun Platform. After tests, **qwen-vl-max** can achieve pretty good result as vision recognition model. (better than Llama and CLIP)

Below are brief introduction of how the tool works:

**1. Vision Recognition:** Under the guidance of **Vision Prompt**, it first calls the visual recognition model to recognize the relevant content in the pictures;
**2. Tag Refinement:** Under the guidance of **Refine Prompt**, it then calls the large language model to refine the generated tag texts (the tag texts may be in natural language, which could be simplified into keywords to reduce the weight of irrelevant words). 
**3. Prompt Pre-editiing:** Prompt needs to be edited in excel file beforehand, and after importing the excel file, you can select the visual recognition as well as refining prompts. The prompt template file is currently provided for interior design scenarios.

Please refer to the illustration below:

**HOW TO GET MODELS (VISION & REFINE) AND API ON ALIYUN:**
1. go to [aliyun Bailian (阿里云百炼)](https://www.aliyun.com/product/bailian). Or [Alibaba Cloud Modelstudio](https://www.alibabacloud.com/zh/product/modelstudio) if you're outside China.

2. Register your account.

3. go to console(控制台)  
