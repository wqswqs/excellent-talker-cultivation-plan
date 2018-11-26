# excellent-talker-cultivation-plan
doing  
选取BLUE值最佳的模型 5h -> wqs  
应用attention模型，丰富上下文表示 5h -> wqs

高  
低频词设置为unknown，以减少显存占用 2h  
应用GRU模型到对话 2h  
应用中文词向量 2h  
设发将训练batch增大到256 5h  
检查cuda各计算过程的执行时间，看有无需优化之处 1h  
对对话的GPU实现做梯度检查 1h
应用GPU实现解码过程 1h
  
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
