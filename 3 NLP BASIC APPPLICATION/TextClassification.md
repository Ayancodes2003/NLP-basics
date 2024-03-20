# Text Classification in Natural Language Processing (NLP)

Text classification is a fundamental task in natural language processing (NLP) where the goal is to automatically assign predefined categories or labels to textual documents. In simple terms it is processing of labeling or organizing text data into groups. There might be text from various sources whose texts are unstructured, it is very important that we structure them.
Even when it comes to businesses it proves to be of great use as it allows to easily get insights from data and automate business processes.

# Practical use of Text Classification.
Text classification finds diverse applications across various domains. Some popular uses include:
* Spam Detection in Emails: Automatically categorizing emails as spam or non-spam based on their content.
* Sentiment Analysis of Online Reviews: Determining the sentiment (positive, negative, or neutral) expressed in user reviews to gauge customer satisfaction.
* Topic Labeling Documents like Research Papers: Automatically assigning categories or topics to research papers based on their content.
* Language Detection like in Google Translate: Identifying the language of a given piece of text to facilitate language translation.
* Age/Gender Identification of Anonymous Users: Predicting the age group or gender of users based on their online interactions or content.
* Tagging Online Content: Automatically tagging or categorizing online content such as articles, blog posts, or social media posts.
* Speech Recognition Used in Virtual Assistants like Siri and Alexa: Understanding and classifying spoken commands or queries in virtual assistant applications.
**Details and code explained in the Applications.md file**


Before we actually get into the application of Text Classificatiom in details, let's dive a bit into the approaches of text classification.

### **Rule based approach**:
 Rule based approach as the name suggest is dependent on certain predefined rules by a domain expert to classify text. The rules might be limguisitc, patterns, keywords etc. If you are still not clear an _example_ might help. Text is evaluated against the set of rules to determine its category. If certain conditions specified in the rules are met, the text is assigned to the corresponding category.
> Consider the task of classifying news articles into categories such as Politics, Sports, and Entertainment. A rule-based approach might involve creating rules like:
  If the article contains keywords like "election," "government," or "policy," classify it as Politics.
  If the article mentions sports teams, players, or events, classify it as Sports.
  If the article discusses movies, celebrities, or entertainment events, classify it as Entertainment. 

### Let's get going into the **mathematical** part of it because what's NLP without math, also you can skip and jump to the next approach, this part is completely optional. 

Text classification using rules involves evaluating the input text against the set of predefined rules. This evaluation can be represented mathematically as:

$$category(text)=argmax_c( ( \sum_{i=1}^n Rule_i(Text).weight_i)$$

Category(text) represents the predicted category for the input text.

Rule_i represents the evaluation of the i_th rule 
