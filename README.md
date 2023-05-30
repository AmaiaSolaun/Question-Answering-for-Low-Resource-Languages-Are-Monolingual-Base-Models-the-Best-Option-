# Question-Answering-for-Low-Resource-Languages-Are-Monolingual-Base-Models-the-Best-Option-

##Description of the project
When researchers for low-resource languages train monolingual models for their language, they tend to use base size models. Consequently, when they evaluate the performance of the model, they compare it with a base size multilingual model (among other base size models). Results show that, in this setting, monolingual models tend to outperform multilingual ones in most NLP tasks (e.g., Agerri et al., 2020; Martin et al., 2020; Armengol-Estapé et al., 2021). However, Agerri and Agirre (2022) recently found that large multilingual models can outperform monolingual base models in various NLP tasks in Spanish, one of them being Question Answering (QA). Agerri and Agirre (2022) report that XLM-RoBERTa improves over the results of five monolingual and four multilingual base models for QA. Thus, for this project we follower this finding and explored whether a large multilingual model can outperform base monolingual models for low-resource languages.

##Methods and materials
For this purpose, we fine-tuned a total of 9 language models, 3 for each of the languages analysed (Basque, French and Catalan). We fine-tuned a monolingual base model, a multilingual base model and a multilingual large model and compared the results. All models were fine-tuned with a batch-size of 16, for 5 epochs and with a learning-rate of 5e<sup>-5</sup> In these two table we collect the specific materials and setting used for fine-tuning the models:

| language | monolingual model | multilingual model | dataset          |
|----------|-------------------|--------------------|------------------|
| catalan  | BERTa             | XLM-RoBERTaL       | ViquiQuAD-v2     |
| basque   | BERTeus           | XLM-RoBERTaL       | ElkarHizketak-v1 |
| french   | CamemBERT         | XLM-RoBERTaL       | FQuAD-v1         |



##Results
