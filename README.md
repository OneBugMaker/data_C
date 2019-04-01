# data_C
这是什么东西，有什么用？
答：这是用卷积神经网络来分类图片的一个案例，准确率可达到0.97。

本设计的数据来源于“http://hydinin.com:8086/phm/article11.html ”。
感谢，比赛举办方提供的数据。
数据共有初赛和复赛两组,分别存放在 data_C1 和 data_C2 这两个文件夹下，每个文件夹
下又有子文件夹neg和pos分别存放有裂纹和无裂纹的轨枕图片。如下所示：
data_C1
	neg
	pos
data_C2
	neg
	pos

初赛数据中含500neg和500+pos的已知类别图片，选取500neg和500pos，共1000张图片。
复赛数据中含800neg和800+pos的已知类别图片，选取800neg和800pos，共1600张图片。

在做这个项目的时候，当加入 data_C2 数据集后发现训练结果变差，这一点困扰了我很久。 
最后检查样本时发现，由于 data_C2 的样本中存在约百分之二的标注错误，导致训练结果不
理想，所以本设计保存的模型参数是在 dataC1 的数据集上训练出来的。

在设计中，利用tensorflow.data 和 tensorflow.keras 这两个API来分别构造数据集的输入
管道，和ResNet模型。

在运行时若要加载之前训练的weights，请保证含有 './save/ResNet/my_model_weights' 。

What's this? What's the use?
Answer: This is a case of using convolutional neural network to classify pictures. The accuracy can reach 0.97.
The design data comes from "http://hydinin.com:8086/phm/article11.html".
Thank you for the data provided by the organizers.
There are two groups of data, the preliminary and the semi-finals, which are stored in data_C1 and data_C2 folders, each folder.
There are sub-folders Neg and POS to store cracked and non-cracked sleeper pictures respectively. As follows:
Data_C1
Neg
POS
Data_C2
Neg
POS
The preliminary data contains 500 neg and 500 + POS pictures of known categories. Select 500 neg and 500 pos, a total of 1000 pictures.
The second round data contains 800 neg and 800 + POS pictures of known categories. Select 800 neg and 800pos pictures, a total of 1600 pictures.
When I was working on this project, when I joined the data_C2 data set, I found that the training results became worse, which troubled me for a long time.
Finally, when checking the samples, it was found that about 2% of the data_C2 samples were labeled incorrectly, resulting in no training results.
Ideal, so the model parameters saved in this design are trained on dataC1 data set.
In the design, tensorflow. data and tensorflow. keras APIs are used to construct the input of data sets respectively.
Pipeline, and ResNet model.
To load weights trained before running, be sure to include'. / save / ResNet / my_model_weights'.
