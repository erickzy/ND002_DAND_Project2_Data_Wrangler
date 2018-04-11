# 项目描述
**你的目标：**
清洗 WeRateDogs 推特数据，创建有趣可靠的分析和可视化。推特档案很大，但是只包括基本的推特信息。对 "Wow!" 进行收集、评估和清洗，是分析和可视化应该做的。

**你在这个项目中的任务如下：**
* 清洗数据包括：
    * 收集数据
    * 评估数据
    * 清洗数据
* 对清洗过的数据进行储存、分析和可视化
* 汇报 1) 你的数据清洗过程 和 2) 你的数据分析和可视化

# 项目目的

## Uda目标

### 收集数据
* 学员能够从各种来源和文件格式中收集数据
    - （DONE）在“项目详细信息”页面上使用至少三（3）个不同来源。
    - （DONE）在“项目详细信息”页面上，使用至少三（3）种不同的文件格式。首先将每一条数据导入到一个单独的 pandas 数据框中。

### 评估数据
* 学员能够以可视化和编程方式评估数据的质量和整洁度。
    - （DONE）可视化评估：每张收集的数据都显示在 Jupyter Notebook 中，以便进行可视化评估。 一旦显示出来，数据可以在外部应用程序（如 Excel，文本编辑器）中进行评估。
    - （DONE）编程评估：使用 pandas 的功能和/或方法来评估数据。
* 学员能够彻底对数据集进行评估
    - （DONE）学员能够检测到至少 八（8）个数据质量问题和两（2）个整洁度问题，包括待清理问题以满足项目要求。每一个问题用一到几句话记录下来。

### 清理数据
* 学员根据数据清理过程中的步骤来逐步完成他们的清理工作
    - （DONE）清理过程中的定义，编码和测试步骤都有明确的记录。
* 学员能够使用编程方式彻底清理数据集
    - （DONE）在清理之前，保存原始数据的副本。
    - （DONE）评估阶段确定的所有问题都可以通过 Python 和 pandas 成功清理，并包括满足项目要求所需的清理任务。
    - （DONE）学员需要创建一个整洁的主数据集（或者多个数据集，如果有必要的话）与所有收集的数据片段。

### 存储并处理清洁过的数据
* 学员能够存储已经收集、评估并清理过的数据集
    - （DONE）学员将他们收集、评估和清理过的主数据集保存到 CSV 文件或 SQLite 数据库中。
* 学生能够根据自己所掌握的数据采取行动来得出结论（例如通过分析，可视化和/或模型)
    - （DONE）使用 Jupyter Notebook 中的 pandas 或 SQL 分析主数据集，并生成至少三（3）个独立的结论。
    - （DONE）在 Jupyter Notebook 中，使用 Python 绘图库或在 Tableau 中至少生成一（1）个标记的可视化对象。
    - （DONE）学员必须在他们的清洗数据中明确他们之后分析和可视化所依据的数据是建立在评估和清理的基础上。

### 报告
* 学员能够思考并描述他们的数据清洗过程
    - （DONE）学员需要言简意赅地介绍他们的数据清理。 这一文件（wrangle_report.pdf）大约只需要300-600字。
* 学员在他们清洗过的数据集中能够发现并描述出结论
    - （DONE）学员发现至少三（3）个结论，其中至少包含一个（1）可视化。这一文件（act_report.pdf）至少需要 250 个字。

### 项目文件
* 学员提交的文件夹中是否包含所有必需的文件
    - （DONE）[wrangle_act.ipynb](https://github.com/erickzy/ND002_DAND_Project2_Data_Wrangler/blob/master/wrangle_act.ipynb)
    - （DONE）[wrangle_report.pdf](https://github.com/erickzy/ND002_DAND_Project2_Data_Wrangler/blob/master/wrangle_report.md)
    - （DONE）[act_report.pdf](https://github.com/erickzy/ND002_DAND_Project2_Data_Wrangler/blob/master/act_report.md)
    - （DONE）并包括所有的数据集文件，如存储的主数据集，并使用在项目提交页面中指定的文件名和扩展名。  

## 个人期望结论假设
* 评分高低应该和转发数量/喜爱程度存在关系
* 评分高低和狗的种类存在关系
* 评分高低和狗的地位存在关系
* 评论的词云分析
* 各种评分的箱形分布图
* 评分的总体分布情况

**所以需要完成tweet-archive-master文档应包含以下内容，相应数据来源在括号中标识：**

* tweet_id 推特账号 （df_tweeter）
* text 推文（df_tweeter）
* timestamp 时间戳（df_tweeter）
* retweet-count 转推数（df_json）
* favorite-count 喜爱数 （df_json）
* rating 评分（df_tweeter）
* dog-name 狗名（df_tweeter）
* dog-status 狗的地位（df_tweeter）
* dog-types 狗的品种(df_pred)
* dog-prediction probabily 品种预测的概率(df_pred)


---
## Update 2018_04_03
1st review存在的问题:
我们来观察下项目动机中的要点会发现，这里有2个问题是强制要求被标记且处理的： 1），只需要原始的数据 2），只需要包含图片的数据（新的提交中已经更改）

关于狗的地位的问题 多种地位的狗，其实最好是将他们保留下来 因为text中可能有些地位是以大写开头的，部分大写的地位没有提取（新的提交中已经更改）

狗名的提取还包括This is|Meet|name is|Say hello to|named 这几种不同类型的信号词 
（但我发现更正掉named的信号词的词条后，还有错误提取了冠词的现象，而这些现象往往都是以This is|Meet|等为提取信号词而错误提取的。 由于name本身不是我研究的主要对象，故还是保留了之提取named信号词的动作。其余的还是按照元数据提供的name信息进行分析。）



