# AAE-Detection

# NLP-Influence-of-Word-Choice-on-AAE
## Breaking Down Bias: Investigating the Influence of Word Choice on Hate Speech Classification of African American English (AAE) and Spam detection on social media platforms

Breaking Down Bias: Investigating the Influence of Word Choice on Hate 
Speech Classification of African American English (AAE) and Spam 
detection on social media platforms

# Introduction

The challenge of controlling hate speech has always been difficult; the scope, and speed of today's hate speech 
make it a particularly contemporary problem. The use of language on social media differs greatly among American 
English speakers, and varies depending on factors such as location, age, ethnicity, and online community. 
However, most natural language processing systems rely heavily on "Standard American English" (SAE), which 
is the dialect most used by white Americans. Previous studies have examined how this affects the performance of 
these systems when processing African American English (AAE) text. These studies suggest that hate speech 
classification systems and sentiment analysis tend to classify AAE text as more likely to contain hate speech or 
other forms of toxic speech. This is particularly problematic because it reinforces existing prejudices and 
stereotypes against African American individuals, portraying them as aggressive and inherently dangerous [1].
Most of our works in this domain focus on identifying these biases or proposing various strategies to mitigate 
bias, like by including more AAE samples while training the model which can subsequently reduce the biases.
Online forums, chat rooms, and social media have seen a particularly high prevalence of hate speech.
Moreover, spam poses issues which could not only cause misinformation to spread quickly but can easily deviate 
platform users to deviate from one website to another. Which also creates security issues for site users like 
phishing, etc. Therefore, it is crucial to ascertain if online chatter represents actual human discussions or if it is 
instead susceptible to being affected by bots or other spammers. Also, censoring comments on platforms, 
especially YouTube, can make a site a safe place for content creators and viewers. Our project will classify the 
comments into four categories: hate, offensive, spam, and neutral.

# Literature Review
In recent years, scholars have increasingly focused on identifying and addressing bias in natural language 
processing systems. Previous studies have highlighted biases towards African American English (AAE) and 
African American names in sentiment analysis and English language identification applications, as well as 
towards Black Twitter users in hate speech classification systems, regardless of their use of AAE. One proposed 
approach to reducing bias is racial priming, which involves educating data annotators on racial and dialectical 
differences prior to annotating training data [2, 3]. This has been shown to decrease bias in some studies. Other 
strategies for bias mitigation have also been suggested in the literature, such as predicting users' demographic 
information to inform other predictions, including identifying offensive speech. However, common debiasing 
techniques have been found to be less effective in mitigating bias towards AAE than debiasing the training data 
itself.
Moreover, an ocean of text data exists on social media and various other platforms that is free to access but 
extremely complex to analyze. However, in recent times, there have been numerous attempts to understand this 
data and use the information to benefit content creators and general users. One such platform is YouTube, which 
has an abundance of content and receives significant daily traffic. Users provide feedback on every video they 
watch through likes and comments, which can be analyzed to help platform users. YouTube has been intensively 
working on hate speech and terminated over 54,000 channels in the last quarter of 2019 due to hate speech [4].
However, spam comments on YouTube channels have also become a problem, as users promote their channels, 
other social media platforms, or themselves, creating a nuisance for the creators and preventing them from 
receiving the desired feedback. This trend seems to be increasing in the coming years, creating a need for research 
to more effectively identify these types of comments and remove them to improve the feedback system for 
creators. Our research will focus primarily on this research gap [5].

# Objective
The following two problem statement shows the utility for our objective: <br />
➔ “Demonstrate the prejudice against African American English that exists on social media, with 
instances of it being categorized as hate speech” <br />
➔ “How detecting spams on social media can prevent user from cyber-attack like phishing and 
increase viewers retention time on platform. Moreover, increase retention time for video.” <br />

# Methodology
We plan to train 3 models on different datasets which will perform crucial part on various stages of our architecture 
shown in Figure 1.
## Dataset
We will use 3 datasets. Firstly, FDCL18 (LINK) which contains Twitter datasets that categorize tweets by the 
various speech terms. The categorization is done as “Abusive”, “Hate”, “Spam” or “Normal”. Also, the datasets 
contain only the tweets id and tags. So will create the function to retrieve the tweet data from Twitter API for 
formation of training dataset. This is the most common problem with Twitter data.
Secondly, we will use African American Tweet Dataset (LINK) for training our African American English (AAE) 
Model. Finally, we will use LIWC swear word dictionary (LINK) to train our word2vec model.


## Models
From Figure 1, we can see, initially, the main model will be trained on the FDCL18 dataset, and it will classify 
tweets into the following categories: "Abusive," "Hate," "Spam," or "Normal." Then, we will take all the hateful 
and abusive speech to our AAE model.
In the AAE model, we will detect tweets with African American origins (words and grammar related to African 
and American English) and ignore those that are not. The model will be trained on AAE tweet data, which contains 
African American tweets.
Finally, we will take all the AAE tweets to the word2vec model. This model is trained on the LIWC swear word 
dictionary. In this stage, we will replace the words in the tweets that are close to non-positive or abusive words 
with words that have similar meanings.
We will then pass the tweets through our main model again and see if it is classified as hate speech or not. If it is 
classified as hate speech again, we can see that there is no bias. However, if the tweet is classified as normal, we 
will see that the model is biased against African American users.

# References
[1] Harris, C., Halevy, M., Howard, A., Bruckman, A., & Yang, D. (2022). Exploring the role of grammar and 
word choice in bias toward African American English (AAE) in hate speech classification. 2022 ACM 
Conference on Fairness, Accountability, and Transparency. https://doi.org/10.1145/3531146.3533144 <br />
[2] Groenwold, S., Ou, L., Parekh, A., Honnavalli, S., Levy, S., Mirza, D., & Wang, W. Y. (2020). Investigating 
African-American vernacular English in Transformer-based text generation. Proceedings of the 2020 
Conference on Empirical Methods in Natural Language Processing (EMNLP). 
https://doi.org/10.18653/v1/2020.emnlp-main.473 <br />
[3] Kiritchenko, S., & Mohammad, S. (2018). Examining gender and race bias in two hundred sentiment 
analysis systems. Proceedings of the Seventh Joint Conference on Lexical and Computational Semantics. 
https://doi.org/10.18653/v1/s18-2005 <br />
[4] Alexander, J. (2020, December 3). YouTube will ask commenters to rethink posting if their message seems 
offensive. The Verge. Retrieved March 3, 2023, from 
https://www.theverge.com/2020/12/3/22150197/youtube-comments-posting-hurtful-hate-videosdiscrimination-monetization-search <br />
[5] Peters, J. (2022, April 8). Youtubers are sick of comment spam, so YouTube is testing a stricter moderation 
system. The Verge. Retrieved March 3, 2023, from 
https://www.theverge.com/2022/4/8/23016861/youtube-comment-spam-testing-moderation
