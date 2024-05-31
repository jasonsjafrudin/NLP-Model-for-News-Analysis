# NLP Model for News Analysis
This repo contains code to build a NLP Model that uses the following techniques:
1. Topic Modeling (k-train LDA)
2. Sentiment Analysis (flair- state of the art)
3. Entity Identification (NER spacy)

The purpose of this NLP Model is to identify jobs and tasks that are likely to be replaced by AI through analyzing over 200,000 news articles regarding AI, published between 2018-2023. Additionally, it identifies the technologies and entities that are driving the revolutionary movement of AI in this day and age. 

## Data cleaning and filtering:
1. Filter articles for English language only
2. Remove URLs from articles
3. Remove newlines from articles
4. Remove tabs from articles
5. Remove hashtags from articles
6. Remove HTML tags from articles
7. Remove script content from articles
8. Eliminate duplicate articles
9. Remove extra white spaces from articles
10. Remove special characters
(below points are not applicable to feeding the NLP Models)
11. Remove punctuations
12. Remove numbers
13. Lowercase text
14. Remove stopwords
15. Filtered out articles that do not contain Key Words at all in the text/content. (-4,262)
16. Filtered out articles where the percentage of Key Word mentions in the text/content is less than 1%. (-28,883)
17. Filtered out articles where the percentage of Key Word mentions in the title is less than 3%. (-3,236)


## Topic Detection Key Results:
<img width="404" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/5d877cfe-88fc-4487-a741-37d63562419f">

topic:1 | count:10,069 | market report analysis global growth research forecast industry key players
This topic seems to be related to market analysis and research in the field of AI, data science, or machine learning. It mentions "market report," "global growth," "research forecast," and "industry key players," indicating discussions about the market trends, growth forecasts, and key players in the industry.

topic:2 | count:14,665 | learning models machine model human language cloud like systems using 
This topic appears to focus on machine learning models and their applications. It mentions "language," "cloud," and "systems," suggesting discussions around machine learning models deployed in cloud environments or used for natural language processing tasks. The mention of "human" could imply discussions about human-like AI or AI systems designed to interact with humans.

topic:3 | count:9,710 | health medical science research healthcare care students clinical learning patients 
This topic likely pertains to the intersection of data science and healthcare or medicine. It could involve discussions about how data science techniques are utilized in healthcare settings, such as predictive analytics for patient care, analyzing medical research data, optimizing clinical processes, or personalized medicine through machine learning algorithms.

topic:4 | count:35,033 | gray group press platform release prnewswire solutions customers generative music 
This topic appears to focus on generative AI in music, likely discussing advancements, platforms, or solutions related to music generation. The mention of "gray group press platform release" suggests it might be a press release or news related to this topic.

topic:5 | count:4,768 | products industry overviewview public newswires services releases consumer distribution entertainment 
This topic appears to be related to product releases, industry overviews, and public newswire services. It mentions "products," "industry overview," "public newswires," "services," "releases," "consumer," "distribution," and "entertainment," suggesting discussions about new product launches, industry trends, press releases, consumer services, and entertainment industry updates (potentially surrounding AI).

topic:6 | count:14,679 | openai security tech systems companies privacy law altman risks ceo 
This topic seems to be centered around discussions related to AI ethics, security, and privacy concerns. It mentions OpenAI, which is known for its work in AI research, and keywords like "privacy," "risks," "security," and "law" indicate discussions around the ethical and legal implications of AI technologies.

topic:7 | count:5,638 | china forwardlooking statements republic october september july june january world 
This topic seems to involve discussions related to China and possibly forward-looking statements regarding something (potentially AI). The mention of months from January to October suggests temporal aspects, and "world" indicates discussions with a global perspective

topic:8 | count:28,230 | chatgpt google best users search tech email microsoft app like 
This topic seems to revolve around various AI applications and technologies, including chatbots like ChatGPT, Google's services, optimizing search algorithms, and email drafting using AI. It encompasses a broad range of AI-related functionalities and services offered by different tech companies such as Microsoft.

topic:9 | count:8,130 | digital industry customer services management companies global innovation technologies solutions 
This topic seems to revolve around solutions (potentially AI) in customer service and management within digital industries.

topic:10 | count:23,443 | ago hours public weather days day says people chatgpt like
The keywords "public," "weather," "days," "day," and "hours" suggest a focus on weather-related information, possibly including forecasts, current conditions, or weather updates. Additionally, the mention of "ChatGPT like" may indicate discussions about AI-generated weather forecasts or the integration of AI technologies like ChatGPT in providing weather-related information or services.

topic:0 | count:7,777 | stock price market share stocks nasdaq trading investment shares investors
This topic appears to be related to stock markets and investment. Keywords such as "stock," "price," "market share," "stocks," "NASDAQ," "trading," "investment," and "investors" suggest discussions about stock market analysis, trading strategies, investment opportunities, and the performance of various stocks and indices like NASDAQ. It might involve AI impact on stock and investment market.


## Sentiment Analysis Key Results:
Sentiment Analysis by Industries on AI Related Articles:

<img width="288" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/72e5262c-e292-4244-b747-7f1691a416de">

Sentiment Analysis on Jobs:

<img width="260" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/1b852198-1a6b-48e8-b0a5-01dcbeadb8c1">
Image represent most frequently mentioned jobs through AI related Articles

<img width="318" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/c9c9d9d7-7e93-4030-bc65-9c40beae3311">
Image represent % of negative articles by Job


## NER Key Result:
<img width="283" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/3504f96a-0e32-4605-b766-e5c1d55b810a">
<img width="281" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/e42d76a6-69cd-4ed8-bf14-0262941ccba5">
<img width="272" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/0368632a-c230-44e6-bcc2-422bb2a719db">
<img width="287" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/db2d4a03-8054-4208-9660-bf98f595085f">

- The most frequently mentioned organizations are primarily large and well-established entities.
- Amongst the top mentioned organizations, big tech companies such as Facebook, Meta, Twitter, Google, Microsoft, Apple, and Amazon have the highest % of negative articles, exhibiting more or less similar sentiments towards AI, data science, and machine learning. That being said, the majority (>50%) of the articles associated with them still exhibit positive sentiments, which does not seem too promising.
- The most frequently mentioned individuals predominantly include CEOs or leaders of major big tech companies, such as Elon Musk (for Twitter), Sundar Pichai (for Google), Mark Zuckerberg (for Facebook), and Satya Nadella (for Microsoft), as well as recent political figures, notably the Presidents of the United States, Donald Trump and Joe Biden.
- Amongst the top mentioned people, within the realm of big tech, Elon Musk and Sundar Pichai are notable for expressing predominantly negative perspectives on AI, data science, and machine learning, with over half of their mentions reflecting this sentiment. Conversely, Mark Zuckerberg and Satya Nadella tend to convey predominantly positive perspectives on AI, data science, and machine learning, with over half of their mentions reflecting this sentiment.


<img width="264" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/feec172f-0c5f-42f3-a997-2192b8973ad0">
<img width="274" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/6a205aab-a391-47e7-b2c6-1d4fae28b7ad">
<img width="272" alt="image" src="https://github.com/jasonsjafrudin/NLP-Model-for-News-Analysis/assets/61297201/7e5c05f4-aa17-43f6-8402-a3456669d2a0">

- When considering the overall trend across the years since 2020, Ukraine holds the top spot as the most skeptical to AI, while Russia emerges at the top for the most recent year.
- Across all countries, the prevalence of articles exhibiting positive sentiments outweighs those with negative sentiments. This trend suggests a significant shift in the world perceptions and acceptance toward AI, data science, and machine learning since 2020 and is projected to continue this trend moving forward.
- ChatGPT, GPT3.5, Vertex AI, and JavaScript are some of the main AI solutions that might be affecting the employment landscape today.
- All products boast a majority (>50%) of articles portraying positive sentiments, signaling substantial investment in AI-driven transformation since 2020. Leading the charge is Xeon, a brand of x86 microprocessors manufactured by Intel Corporation, with an impressive 91% of articles reflecting positive sentiments.
- Although all products demonstrate significant investment in AI-driven transformations, PlayStation, today, while still showing a positive outlook on AI integration, appears to be the least likely to undergo AI-driven transformations compared to the other products.



## Actionable Recommendations:
### Ensuring Job Security in the Age of AI:
1. Specialized Recommendations:
Consider pursuing a career as an attorney while avoiding representation of Big Tech companies.
Explore opportunities for politicians in the Republican Party, ideally within Donald Trump's team.
Aim to become a Judge presiding over court proceedings in Russia.
2. General Guidelines:
Focus on industries such as Politics, Law, or Finance.
Prefer professions such as Attorney, Politician, Judge, or Lawyer.
If working in the political industry, lean towards affiliations with the Republican Party.
Avoid employment with Big Tech companies and Gray Television, Inc. If interested in Big Tech, prioritize companies like Twitter or Google.
3. Geographic Considerations:
Consider working in countries such as Russia, Ukraine, or Israel.

Key Takeaway:
Pursuing careers in specific industries, professions, organizations, and geographic regions can enhance job security amidst AI advancements.

### Facilitating Efficiency Gains and Job Automation in the Age of AI
Specialized Recommendations- Consider investing in the following technologies to streamline operations and enhance efficiency:
- 3D Printing: Automate manufacturing processes such as molding, casting, or machining for office use.
- Autonomous Vehicles: Implement autonomous vehicles for navigating and operating without human input or intervention, especially beneficial for vehicle manufacturing companies.
- Smart Buildings: Automate building systems control, including HVAC, lighting, and security, to improve efficiency and comfort in office environments.
- AI-Powered Devices and Wearables: Utilize these for early detection and prevention of health issues, reducing the need for costly interventions or hospitalizations, particularly beneficial for healthcare companies.
- Personalized Treatment Systems: Implement systems to identify biomarkers and genetic variants influencing patient responses to treatment, reducing trial-and-error approaches and unnecessary treatments, saving time and resources for healthcare companies.
- Automated Underwriting Systems (AUS): Automate the underwriting process for loan applications, particularly advantageous for financial companies.
- Credit Scoring Models: Employ models to automate the analysis of borrower data and predict creditworthiness, offering efficiency benefits for financial companies.

Integration of AI Solutions: 
- Explore integrating leading AI solutions such as ChatGPT, JavaScript, GPT3.5, and Vertex AI into your company. These technologies are revolutionizing job automation:
- ChatGPT: Automate routine tasks such as answering customer inquiries, generating reports, and scheduling appointments.
- GPT3.5: Serve as a virtual assistant for employees, providing answers to common questions and assisting with task management.
- Vertex AI: Explore its capabilities for machine learning and automation, offering potential efficiency gains across various business functions.

AI-Driven CRM Integration- If your company is a consumer of a CRM product, investigate opportunities for creative integration with AI technologies:
- Streamline repetitive and time-consuming tasks within CRM processes, such as data entry, lead scoring, and email communications, through AI-powered automation.
- Free up time for sales and marketing teams to focus on strategic activities by leveraging AI to automate routine tasks within CRM workflows.

By implementing these recommendations, your company can leverage AI technologies to enhance efficiency, streamline operations, and drive innovation in the age of AI.





