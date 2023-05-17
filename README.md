# Huatuo-26M

## 👩🏻‍⚕Introduction

Huatuo-26M is the largest Chinese medical Q&A dataset to date. This dataset contains over 26 million high-quality medical Q&A pairs, covering a wide range of topics such as diseases, symptoms, treatments, and drug information. Huatuo-26M serves as a valuable resource for researchers, developers, and companies looking to enhance AI applications in the medical field, such as chatbots, intelligent diagnosis systems, etc.


## 📚Data Content

The Huatuo-26M dataset is collected and integrated from multiple sources, including:

- Online Medical Encyclopedia [huatuo_encyclopedia_qa](https://huggingface.co/datasets/FreedomIntelligence/huatuo_encyclopedia_qa)
- Online Medical Knowledge Bases [huatuo_knowledge_graph_qa](https://huggingface.co/datasets/FreedomIntelligence/huatuo_knowledge_graph_qa)
- Online Medical Consultation Records（answer in the form of URLs） [huatuo_consultation_qa](https://huggingface.co/datasets/FreedomIntelligence/huatuo_consultation_qa) 



ps: Due to some reasons, we are currently unable to publicly release the text format data from the Online Medical Consultation Records, which constitutes the largest proportion of the Huatuo-26M dataset.



Each question-answer pair in the dataset contains the following fields：

- questions：Problem Description 
- answers：Doctor/Expert Answers



The following is the huatuo test set we used in the paper, which consists of random sampling of data from multiple sources.

- Testdatasets：[huatuo26M-testdatasets](https://huggingface.co/datasets/FreedomIntelligence/huatuo26M-testdatasets)



## 🤖Data Usage

The Huatuo-26M dataset can be used for a variety of AI research and applications in the medical field, such as:

- Natural Language Processing: Including but not limited to Q&A systems, text classification, sentiment analysis, etc.
- Machine Learning model training: Such as disease prediction, personalized treatment recommendation, etc.
- AI applications in the medical field: Such as intelligent diagnosis systems, medical consultation chatbots, etc.



## 🚀Quick Start

To start using the Huatuo-26M dataset, you can follow the steps below:

```python
import datasets
# part 1
knowledge_graph_dataset = datasets.load_dataset('FreedomIntelligence/huatuo_knowledge_graph_qa')
# part 2
encyclopedia_dataset = datasets.load_dataset('FreedomIntelligence/huatuo_encyclopedia_qa')
# part 3 (only url)
consultation_dataset = datasets.load_dataset('FreedomIntelligence/huatuo_consultation_qa')

# testdatasets (6k)
huatuo_testdatasets = datasets.load_dataset('FreedomIntelligence/huatuo26M-testdatasets')
```



## 👩🏻‍🔬Experiment Record



- #### Retrieve：


![image-20230517135907642](img/retrieve.png)

- #### NLG：

![image-20230517135907642](img/NLG.png)


- #### Zero-shot：

![image-20230517140031586](img/zero-shot.png)

- #### RAG：

![image-20230517140124397](img/rag.png)


- #### CBLUE：


![image-20230517140420680](img/cblue.png)



## 🚁License

The Huatuo-26M dataset is licensed under Apache 2.0. Please make sure you have read and agreed to the license terms before using it.



## 👷🏻‍Contribution

We welcome and appreciate all contributions! If you find problems in the dataset or have new ideas and suggestions, please feel free to communicate with us through Issues or Pull Requests.



## 📱Contact Us

If you have any questions or need help, please feel free to ask us via email （[anon2010@163.com](mailto:anon2010@163.com)）or in the Issues section.

------

The project is named after Hua Tuo, a famous physician in ancient China, reflecting our dedication to the advancement of medical knowledge and technology.



## 😁Citation

```
@misc{li2023huatuo26m,
      title={Huatuo-26M, a Large-scale Chinese Medical QA Dataset}, 
      author={Jianquan Li and Xidong Wang and Xiangbo Wu and Zhiyi Zhang and Xiaolong Xu and Jie Fu and Prayag Tiwari and Xiang Wan and Benyou Wang},
      year={2023},
      eprint={2305.01526},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```