# payever-AI-Trial

## Project Documentation 

The project focuses on creating a new model (developed chatbot) to enhance user experience and accessibility to support documentation on our support website. 

### Steps

#### 1. Scraping
Objective to extract comprehensive content from the Support Website.
I have used selenium library of python for this purpose and utilized appropriate scraping technologies to ensure robust content extraction.
Scope Extracted all relevant content, including text, images, and multimedia elements from various pages of the website.
Developed a scraper “Web Scraping.ipynb” to systematically gather data, ensuring no content was overlooked and maintaining a high coverage of the site.
I have extracted approximately 95% of data from support website and stored that in scraped_data.json.
At first I decided to extract from home page of support website but it wasn’t that easy than I decided to take every blocks like:
https://support.payever.org/hc/en-us/categories/360002505659-payever-Account
https://support.payever.org/hc/en-us/categories/360002490100-payever-Settings
inside each block, there are many links and URLs. I tried to extract data from these links without actually opening them. Because of this, I faced Cloudflare's human verification block. It wasn't a complete block, but it only allowed me to extract data from one or two links per page.
I tried various techniques like using a 2Captcha API and adding delays, but what works is I have to initialize drive separately in a way that I have to start and quit drive in each epoch after covering one link. 

#### 2. Data Normalization
Objective to standardize extracted content for consistency and usability.
Techniques Applied data normalization techniques to handle variations in formatting, language, and metadata. I have covered this on “Data Normalizing and processing.ipynb” and stored all this in “normalized_data.csv”.
#### 3. Data Processing
Objective to prepare the normalized data for integration into the training pipeline.
Steps Taken
Data Cleaning Removed any irrelevant or redundant information. Performed all this on “Data Normalizing and processing.ipynb” and stored all this in “processed_data.csv”.

#### 4. Data Preprocessing
Objective to prepare data for the modeling phase.
Techniques Used:
Tokenization Converted text data into tokens.
Vectorization Transformed tokens into numerical vectors suitable for model input.
Padding Ensured consistent input lengths for model training. Performed all this on “Data Preprocessing and modeling.ipynb”.  

#### 5. Modeling (Chat Bot)
Objective to create a chatbot capable of interacting with users and retrieving relevant information from the support documentation.
Model Architecture Selected and implemented a model architecture that suits language processing and information retrieval tasks.


#### Model Architecture:

![image](https://github.com/user-attachments/assets/2207ee7a-4012-4d2c-ae8e-8f6b8b95970a)



#### Model Performance:

![image](https://github.com/user-attachments/assets/fced2210-0a69-49d1-9e87-f9ca43afedd0)


 

