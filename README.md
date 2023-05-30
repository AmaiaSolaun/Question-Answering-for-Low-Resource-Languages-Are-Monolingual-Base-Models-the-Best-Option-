# Question-Answering-for-Low-Resource-Languages-Are-Monolingual-Base-Models-the-Best-Option-

## Description of the project
When researchers for low-resource languages train monolingual models for their language, they tend to use base size models. Consequently, when they evaluate the performance of the model, they compare it with a base size multilingual model (among other base size models). Results show that, in this setting, monolingual models tend to outperform multilingual ones in most NLP tasks (e.g., Agerri et al., 2020; Martin et al., 2020; Armengol-Estapé et al., 2021). However, Agerri and Agirre (2022) recently found that large multilingual models can outperform monolingual base models in various NLP tasks in Spanish, one of them being Question Answering (QA). Agerri and Agirre (2022) report that XLM-RoBERTa improves over the results of five monolingual and four multilingual base models for QA. Thus, for this project we follower this finding and explored whether a large multilingual model can outperform base monolingual models for low-resource languages.

## Methods and materials
For this purpose, we fine-tuned a total of 9 language models, 3 for each of the languages analysed (Basque, French and Catalan). We fine-tuned a monolingual base model, a multilingual base model and a multilingual large model and compared the results. All models were fine-tuned with a batch-size of 16, for 5 epochs and with a learning-rate of 5e<sup>-5</sup>. In these two table we collect the specific materials used for fine-tuning the models:


| language | monolingual base model | multilingual base model | multilingual base model | dataset          |
|----------|------------------------|-------------------------|-------------------------|------------------|
| catalan  | [BERTa](https://huggingface.co/projecte-aina/roberta-base-ca-v2)                  | [XML-RoBERTa-base](https://huggingface.co/xlm-roberta-base)        | [XLM-RoBERTaL](https://huggingface.co/xlm-roberta-large)            | ViquiQuAD-v2     |
| basque   | [BERTeus](https://huggingface.co/ixa-ehu/berteus-base-cased)                | [XML-RoBERTa-base](https://huggingface.co/xlm-roberta-base)        | [XLM-RoBERTaL](https://huggingface.co/xlm-roberta-large)           | ElkarHizketak-v1 |
| french   | [CamemBERT](https://huggingface.co/camembert-base)              | [XML-RoBERTa-base](https://huggingface.co/xlm-roberta-base)        | [XLM-RoBERTaL](https://huggingface.co/xlm-roberta-large)           | FQuAD-v1         |

In this github we also make available the notebooks used to fine-tune the models, which are based on the [Huggingface tutorial](https://github.com/huggingface/notebooks/blob/main/examples/question_answering.ipynb) for fine-tuning transformer for QA tasks.

## Results
We have collected the results obtain in .csv files to make simplify the comparison and analysis of the results. We make those results available in this github-

## References

