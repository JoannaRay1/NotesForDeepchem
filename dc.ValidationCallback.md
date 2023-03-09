
params:<br/>
class ValidationCallback(dataset, interval, metrics, output_file=sys.stdout, save_dir=None, save_metric=0, save_on_minimum=True, transformers=[])
save_on_minimum：
if save_on_minimum=False，则会在每个epoch之后保存checkpoint文件，即使性能没有提高。
所以在save_dir中保存的文件不一定是性能最优的。 记该checkpoint文件集合为A
if save_on_minimum=True，则只有当性能指标优于先前最佳性能时，才会保存checkpoint文件。记该checkpoint文件集合为B
A包含B

save_dir：
不写即不保存checkpoint
鉴于ValidationCallback 引用了save_checkpoint()函数
该路径等价于 model_dir  in save_checkpoint()
不建议同时使用save_dir 和 model_dir
但如果同时使用，且指定了不同路径，那么结果是？

显式加载：
model.fit(train_dataset, nb_epoch=100, callbacks=[validation_callback], max_checkpoints_to_keep=1)
model.restore()
如果没有显式地加载best_model，则model的参数是在最后一个epoch结束时的参数，而不是性能最优的参数。


