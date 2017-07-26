# insuranceqa-corpus-zh
保险行业语料库

## Welcome

该语料库包含从网站[Insurance Library](http://www.insurancelibrary.com/) 收集的问题和答案。

据我们所知，这是保险领域首个开放的QA语料库：

* 该语料库的内容由现实世界的用户提出，高质量的答案由具有深度领域知识的专业人士提供。 所以这是一个具有真正价值的语料，而不是玩具。

* 在上述论文中，语料库用于答复选择任务。 另一方面，这种语料库的其他用法也是可能的。 例如，通过阅读理解答案，观察学习等自主学习，使系统能够最终拿出自己的看不见的问题的答案。

欢迎任何进一步增加此数据集的想法。

## 语料数据

| - | 问题      |  答案  | 词汇  | 
| ------------- |-------------| ----- |   ----- |           
| 训练      | 12,889 | 21,325  |    107,889        |
| 验证      | 2,000     |  3354 |   16,931          |
| 测试       | 2,000      |    3308 |  16,815            |

一共有 27,413 个回答， (TODO 补充词汇数量)，数据格式为 ```json```:

```
{
    "INDEX": {
        "zh": "中文",
        "en": "英文",
        "domain": "保险种类",
        "answers": [""] # 答案Index列表
        "evidences": [""] # 证据Index列表
    },
    more ...
}
```

训练：```corpus/train.json```

验证：```corpus/valid.json```

测试：```corpus/test.json```

答案：```corpus/answers.json```

```
{
    "INDEX": {
        "zh": "中文",
        "en": "英文"
    },
    more ...
}
```

### 中英文对照文件

```
格式 INDEX ++$++ 保险种类 ++$++ 中文 ++$++ 英文
```

训练：```corpus/train.txt```

验证：```corpus/valid.txt```

测试：```corpus/test.txt```

## 声明

声明1 : [insuranceqa-corpus-zh](https://github.com/Samurais/insuranceqa-corpus-zh)

本数据集使用翻译 [insuranceQA](https://github.com/shuzi/insuranceQA)而生成，代码发布证书 GPL 3.0。数据仅限于研究用途，如果在发布的任何媒体、期刊、杂志或博客等内容时，必须注明引用和地址。

```
InsuranceQA Corpus, Samurais, https://github.com/Samurais/insuranceqa-corpus-zh, 07 27, 2017
```

任何基于[insuranceqa-corpus](https://github.com/Samurais/insuranceqa-corpus-zh)衍生的数据也需要开放并需要声明和“声明1”和“声明2”一致的内容。

声明2 : [insuranceQA](https://github.com/shuzi/insuranceQA)

此数据集仅作为研究目的提供。如果您使用这些数据发表任何内容，请引用我们的论文：[Applying Deep Learning to Answer Selection: A Study and An Open Task](https://arxiv.org/abs/1508.01585)。Minwei Feng, Bing Xiang, Michael R. Glass, Lidan Wang, Bowen Zhou @ 2015