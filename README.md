# Huatuo-26M Dataset


【[English](README_en.md)】    


## 👩🏻‍⚕️项目简介

- Huatuo-26M 是目前为止最大的中文医疗问答数据集。此数据集包含了超过2600万个高质量的医疗问答对，涵盖了各种疾病、症状、治疗方式、药品信息等多个方面。
- Huatuo-Lite 是在Huatuo26M数据集的基础上经过多次提纯和重写而精炼优化的数据集。它具有更多的数据维度和更高的数据质量。


## 📚数据内容

Huatuo-26M 数据集主要包括：

- 在线医疗百科 [huatuo_encyclopedia_qa](https://huggingface.co/datasets/FreedomIntelligence/huatuo_encyclopedia_qa)
- 医疗知识图谱 [huatuo_knowledge_graph_qa](https://huggingface.co/datasets/FreedomIntelligence/huatuo_knowledge_graph_qa)
- 网络上的公开医疗问答论坛（答案为url形式） [huatuo_consultation_qa](https://huggingface.co/datasets/FreedomIntelligence/huatuo_consultation_qa)
- 精简版本Huatuo-Lite [Huatuo-Lite](https://huggingface.co/datasets/FreedomIntelligence/Huatuo26M-Lite)


数据集中的每个问答对包含以下字段：

- Question：问题描述 
- Answer：医生/专家的答案
- Huatuo-Lite 数据集还具有**医院科室**和**相关疾病**字段



以下为我们在论文中使用的huatuo测试集，由多个来源中数据随机抽取组成。

- Testdatasets：[huatuo26M-testdatasets](https://huggingface.co/datasets/FreedomIntelligence/huatuo26M-testdatasets)



## 🚀快速开始

为了开始使用 Huatuo-26M 数据集，你可以按照以下步骤操作：

```python
import datasets
# part 1
knowledge_graph_dataset = datasets.load_dataset('FreedomIntelligence/huatuo_knowledge_graph_qa')
# part 2
encyclopedia_dataset = datasets.load_dataset('FreedomIntelligence/huatuo_encyclopedia_qa')
# part 3 (only url)
consultation_dataset = datasets.load_dataset('FreedomIntelligence/huatuo_consultation_qa')
# Huatuo-Lite
lite = load_dataset("FreedomIntelligence/Huatuo26M-Lite")

# testdatasets (6k)
huatuo_testdatasets = datasets.load_dataset('FreedomIntelligence/huatuo26M-testdatasets')
```



## 👩🏻‍🔬实验记录

### 测评

- 检索测评：
  <details><summary>Click to expand</summary>
      
  <img src="img/retrieve.png" alt="retrieve" style="zoom:100%;" />
      
  </details>

- 答案生成测评：

  <details><summary>Click to expand</summary>
      
  <img src="img/NLG.png" alt="retrieve" style="zoom:100%;" />
      
  </details>

### 应用

- Zero-shot迁移至其他QA数据集：

  <details><summary>Click to expand</summary>
      
  <img src="img/zero-shot.png" alt="retrieve" style="zoom:100%;" />
      
   </details>

- 作为外部知识进行RAG：

  <details><summary>Click to expand</summary>
            
  <img src="img/rag.png" alt="retrieve" style="zoom:100%;" />
      
      
  </details>

- 作为语言模型(LM)的预训练数据：

  <details><summary>Click to expand</summary>
  <img src="img/cblue.png" alt="retrieve" style="zoom:100%;" />
      
  </details>


- 作为医学LLM的微调数据：
  <details><summary>Click to expand</summary>
  <img src="img/sft.png" alt="retrieve" style="zoom:100%;" />
      
  </details>

## 🚁许可

Huatuo-26M 数据集遵循 Apache 2.0 许可。使用前请确保你已阅读并同意许可条款。



## 📱联系我们

如果你有任何问题或者需要帮助，欢迎通过电子邮件（[xidongw@163.com](mailto:xidongw@163.com)）或者在 Issues 区向我们提问。

------



## 😁引用

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
