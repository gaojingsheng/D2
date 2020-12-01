D2小仓库
====
包含腿腿的代码，QQ和正气的精神力<br>
<br>

### ISBI 2019 SegTHOR Challenge：<br>
<br>
该项目受到 ISBI 2019 SegTHOR Challenge: https://segthor.grand-challenge.org/ 的启发[19]。<br>
<br>
SegTHOR挑战解决了计算机断层扫描（CT）图像中处于风险分割中的器官的问题。<br>
在肺癌和食道癌中，放射治疗的规划始于目标肿瘤和位于目标肿瘤附近的健康器官（在CT图像上称为“危险器官”（OAR））的描绘。 通常，该描述主要是手动的，这是乏味的并且是解剖学错误的根源。 <br>
在此挑战中，目标是自动分割4个OAR：心脏，主动脉，气管，食道。 将为参与者提供训练集与测试集，训练集包括40台CT扫描和手动分割，测试集包括20次CT扫描。<br>
<br>
[19] Su Ruan Bernard Dubray Roger Trullo, Caroline Petitjean. Segmentation of organs at risks in thoracic ct images using a sharp mask architecture and conditional random fields. international Symposium on Biomedical Imaging, 13(4):600-612, 2004. <br>
<br>

### 我们的任务： <br>
<br>
构建一个多器官CT切片分割模型。 <br>
<br>
鼓励从decoder到encoder添加一些feedback/recurrent link[26]以获得更好的性能。 <br>
[26]Lei Xu. An overview and perspectives on bidirectional intelligence: Lmser duality, double ia harmony, and causal computation. IEEE/CAA Journal of Automatica Sinica, 6(4):865{893, 2019. <br>
<br>

### 数据集下载地址： <br>
<br>
https://jbox.sjtu.edu.cn/l/noXQob (password: eidr) <br>
<br>
数据集中的每个scan的大小为 512 x 512 x（150 x 284）体素。 <br>
整个数据集包括 40 个案例，其中第 1-30 个是训练集，而第 31-40 个是测试集。 <br>
您可能需要一些对这些数据进行预处理。<br>
<br>

### 我们fork了MLT_SegTHOR的代码到仓库进行复现，这个代码有UNet、ResUNet和DenseUNet的模型。
<br>
目前三维数据比较大，我们对数据进行可视化是通过ITK_SNAP，这是一个查看医疗三维数据的软件，可以很方便的查看CT图和标注的mask（注意文件路径地址全英文，都否软件的IO读取将会失效）。<br>
<br>
未来我们规划将模型改成lmser进行训练以期取得更好的结果。<br>
