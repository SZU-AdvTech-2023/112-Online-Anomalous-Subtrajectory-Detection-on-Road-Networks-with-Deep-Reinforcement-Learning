
# OASD

论文 "Online Anomalous Subtrajectory Detection on Road Networks with Deep Reinforcement Learning" (ICDE23)的运行代码

## 要求
* Python >= 3.5
* Tensorflow (1.8.0)

### 参数

parameter.py中有几个参数，可以尝试修改这些参数以获得更好的结果，例如threshold=0.5（对于有噪声的标签）、consider=0.4（对于正常的路线选择）和delay=8（对于延迟机制）。此外，它还包括模型中使用的其他超参数。

### Training

运行 `train.py`, 生成的RSRNet和ASDNet会自动保存至 `./data/train_rsr` 和 `./data/train_asd`。可以在文件夹里挑选表现最优的模型。
可以在`parameter.py`里面设置epoch参数。

```
python train.py
```

### Evaluation

可以通过运行`evaluation.py`文件来测试已经训练获得的模型。

```
python evaluation.py
```
