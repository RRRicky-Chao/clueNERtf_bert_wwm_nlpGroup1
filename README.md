  # CLUENER_bert_wwm_nlpGroup1
  
  自然语言处理导论第一小组期末作业。
  
  硬件：CPU：AMD R7 3700X & GPU：MSI GeForce RTX 2070 SUPER
  
  环境：Python 3.7 & Tensorflow 1.14
  
  主要参考：https://github.com/CLUEbenchmark/CLUENER2020
  
  技术报告链接：https://arxiv.org/abs/2001.04351
  
  ```
  @article{xu2020cluener2020,
    title={CLUENER2020: Fine-grained Name Entity Recognition for Chinese},
    author={Xu, Liang and Dong, Qianqian and Yu, Cong and Tian, Yin and Liu, Weitang and Li, Lu and Zhang, Xuanwei},
    journal={arXiv preprint arXiv:2001.04351},
    year={2020}
   }
  ```
  ## 运行前准备工作与文件夹说明
      
      1. 下载[BERT-wwm](https://drive.google.com/open?id=1RoTQsXp2hkQ1gSRVylRIJfQxJUgkfJMW/)预训练模型，下载后置于bert_wwm文件夹下；
      
      2. 数据集已预先下载，置于data文件夹下；
      
      3. ner_bert_wwm文件夹用于存放训练后生成的模型；
      
      4. nlpGroup1Submit文件夹中存放待提交CLUE网站线上评价的、对测试集的预测。
      
  ## 运行及评分步骤
      
      第一步， 生成tf_record；
      运行 data_processor_seq.py
      
      第二步， 训练ner模型
      运行 train_sequence_label.py
       
      第三步， 加载模型进行预测
      运行 predict_sequence_label.py
      
      第四步，评分
      运行 score.py

  ## 补充说明
      
      predict_sequence_label.py 与 score.py 默认预测与评价的对象是验证集（./data/dev.json）。若要对测试集（./data/test.json）进行预测以及后续上传CLUE网站进行线上评价，将predict_sequence_label.py里涉及的文件名中的“dev”改为“test”即可。
