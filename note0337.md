# QUESTION
##hyperopt tuning: why the best loss in the trail is the samm as the last trail when this trail is not worse??
best loss看起来像是历史表现最好的分数，而不是在每一轮中表现最好的分数
？？ 是hyperopt本身调参的特点吗
？？还是因为加了restore; 因此恢复到了历史最好的model；但是我每一轮都清空了ckpt啊

##callback到底有没有发挥作用？？？？
为什么每次都跑完了3600个epoch

##tensorboard 为什么还是用不了
明明加了port/8080

##能不能尝试成功nnl

## 大小为600的数据集，MSE 1.6；2000的数据集，MSE 200；为什么差别这么大

##bdmal
A文件掉B文件时 numpy找不到的问题怎么解决
！python A.py放终端有没有用  看不出来


# good findings
## MPNN 运行不了：因为deepchem 加不了 model.train();那别人是怎么跑的

##MSE若变化不大（且很小），很可能是这个模型不好：可以选用更简单的
##先粗调：神经架构；激活函数。 再细调：LR dropout

##benchmark怎么用：for循环

##bdmal
git clone http ranther than ssh
to use web portal: add /port/8080



