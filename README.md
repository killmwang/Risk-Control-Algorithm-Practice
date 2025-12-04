# Risk-Control-Algorithm-Practice
# Financial Fraud Detection System (金融反欺诈风控系统)

## 项目背景
基于 IEEE-CIS 高维数据集，构建机器学习模型以识别潜在的欺诈交易。

## 核心工作
1. **数据清洗**：处理 59 万条交易数据，使用内存优化策略将内存占用降低 70%。
2. **特征工程**：
   - 挖掘时间特征：发现欺诈交易在正常活跃时间段（14:00-22:00）更隐蔽。
   - 聚合特征：构建 `card1_count` (频次) 与 `amt_minus_mean` (偏离度)，在特征重要性中位列 Top 5。
3. **模型性能**：
   - 模型：LightGBM (Gradient Boosting Decision Tree)
   - 验证策略：Time-based Split (前80%训练，后20%验证)
   - **最终 AUC：0.9114**

## 运行环境
- Python 3.x
- Pandas, LightGBM, Scikit-learn
