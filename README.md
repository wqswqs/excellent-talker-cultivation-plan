# excellent-talker-cultivation-plan
doing  
用困惑度选取最佳的模型参数 2h -> wqs  
应用attention模型，丰富上下文表示 5h -> wqs  
低频词设置为unknown，以减少显存占用，设cutoff为可调的超参数 4h -> wz  
应用中文词向量 2h -> wz  

高  
弄清目前各参数的显存占用情况 3h
对GPU实现作梯度检查 3h
应用GRU模型到对话 2h  
检查cuda各计算过程的执行时间，看有无需优化之处 1h  
对对话的GPU实现做梯度检查 1h  
应用GPU实现解码过程 1h  
在词表为五万的情况下试试batch能开多大（gpu）

中  
beam size 增大到500  
应用BERT 20h  
  
低  
应用page locked memory，提升cuda加速效果 3h  
改变参数的存取方式 3h  
增加中文字特征 4h  
使用人工标注的数据作为开发集和测试集。1h  

done  
开发交互模式 1h -> wqs 1h  
选取BLUE值最佳的模型 5h -> wqs 10h 只计算了BLEU值，没有据此选择最佳模型，判断不合适  
