# Question-Answering-for-Low-Resource-Languages-Are-Monolingual-Base-Models-the-Best-Option-

## Description of the project
When researchers for low-resource languages train monolingual models for their language, they tend to use base size models. Consequently, when they evaluate the performance of the model, they compare it with a base size multilingual model (among other base size models). Results show that, in this setting, monolingual models tend to outperform multilingual ones in most NLP tasks (e.g., Agerri et al., 2020; Martin et al., 2020; Armengol-Estapé et al., 2021). However, Agerri and Agirre (2022) recently found that large multilingual models can outperform monolingual base models in various NLP tasks in Spanish, one of them being Question Answering (QA). Agerri and Agirre (2022) report that XLM-RoBERTa improves over the results of five monolingual and four multilingual base models for QA. Thus, for this project we followed this finding and explored whether a large multilingual model can outperform base monolingual models for low-resource languages.

## Methods and materials
For this purpose, we fine-tuned a total of 9 language models, 3 for each of the languages analysed (Basque, French and Catalan). We fine-tuned a monolingual base model, a multilingual base model and a multilingual large model and compared the results. All models were fine-tuned with a batch-size of 16, for 5 epochs and with a learning-rate of 5e<sup>-5</sup>. In these two table we collect the specific materials used for fine-tuning the models:


| language | monolingual base model | multilingual base model | multilingual base model | dataset          |
|----------|------------------------|-------------------------|-------------------------|------------------|
| catalan  | [BERTa](https://huggingface.co/projecte-aina/roberta-base-ca-v2)                  | [XML-RoBERTa-base](https://huggingface.co/xlm-roberta-base)        | [XLM-RoBERTaL](https://huggingface.co/xlm-roberta-large)            | [ViquiQuAD-v2](https://huggingface.co/datasets/projecte-aina/viquiquad)     |
| basque   | [BERTeus](https://huggingface.co/ixa-ehu/berteus-base-cased)                | [XML-RoBERTa-base](https://huggingface.co/xlm-roberta-base)        | [XLM-RoBERTaL](https://huggingface.co/xlm-roberta-large)           |  [ElkarHizketak-v1](http://ixa.si.ehu.es/node/12934) |
| french   | [CamemBERT](https://huggingface.co/camembert-base)              | [XML-RoBERTa-base](https://huggingface.co/xlm-roberta-base)        | [XLM-RoBERTaL](https://huggingface.co/xlm-roberta-large)           | [FQuAD-v1](https://huggingface.co/datasets/fquad)         |

In this github we also make available the notebooks used to fine-tune the models, which are based on the [Huggingface tutorial](https://github.com/huggingface/notebooks/blob/main/examples/question_answering.ipynb) for fine-tuning transformer for QA tasks.

## Results
We have collected the results obtain in .csv files to make simplify the comparison and analysis of the results. We make those results available in this github in the [Results](https://github.com/AmaiaSolaun/Question-Answering-for-Low-Resource-Languages-Are-Monolingual-Base-Models-the-Best-Option-/tree/main/Results) folder.

## References
Agerri, R., Vicente, I.S., Campos, J.A., Barrena, A., Saralegi, X.,
Soroa, A. and Agirre, E., 2020. Give your text representation
models some love: the case for basque. arXiv preprint
arXiv:2004.00033.

Agerri, R. and Agirre, E., 2022. Lessons learned from the
evaluation of Spanish Language Models. arXiv preprint
arXiv:2212.08390.

Agirre, E., 2020, May. Conversational question answering in low
resource scenarios: A dataset and case study for basque.
In Proceedings of the Twelfth Language Resources and
Evaluation Conference (pp. 436-442).

Armengol-Estapé, J., Carrino, C.P., Rodriguez-Penagos, C.,
Bonet, O.D.G., Armentano-Oller, C., Gonzalez-Agirre, A.,
Melero, M. and Villegas, M., 2021. Are multilingual models the
best choice for moderately under-resourced languages? A
comprehensive assessment for Catalan. arXiv preprint
arXiv:2107.07903.

d'Hoffschmidt, M., Belblidia, W., Brendlé, T., Heinrich, Q. and
Vidal, M., 2020. FQuAD: French question answering
dataset. arXiv preprint arXiv:2002.06071.

Martin, L., Muller, B., Suárez, P.J.O., Dupont, Y., Romary, L., de
La Clergerie, É.V., Seddah, D. and Sagot, B., 2019.
CamemBERT: a tasty French language model. arXiv preprint
arXiv:1911.03894.


Otegi, A., Agirre, A., Campos, J.A., Soroa, A. and Rodriguez-
Penagos, C., Armentano-Oller, C., Villegas, M., Melero, M.,
Gonzalez, A., Bonet, O.D.G. and Pio, C.C., 2021. The catalan
language CLUB. arXiv preprint arXiv:2112.01894.
