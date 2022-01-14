#### [[中文版]](./index_cn.html)

## About
Hey, guys! I am an AI engineer from China, specializing in computer vision & deep learning.
I'd like to digest theories and share what I've learned on a technical blog([https://muzhan.blog.csdn.net](https://muzhan.blog.csdn.net)), which has helped me gain over 6,000 subscribers in four years. I enjoy chasing novel and popular algorithms, and have a wide range of interests. some of my blog articles: 《[Swin Transformer全方位解读](https://blog.csdn.net/leviopku/article/details/120826980)》、《[YOLO系列之YOLOv3](https://blog.csdn.net/leviopku/article/details/82660381)》、《[GNN之图注意力网络GAT](https://zhuanlan.zhihu.com/p/112938037)》、《[令人心动的transformer](https://blog.csdn.net/leviopku/article/details/115614056)》、《[生成对抗网络——GAN（一）](https://blog.csdn.net/leviopku/article/details/81292192)》、《[目标检测中的b-box回归损失函数](https://blog.csdn.net/leviopku/article/details/114655338)》<br>

## Education
2016.9-2019.6&nbsp;&nbsp;[Peking University](https://pku.edu.cn)&nbsp;&nbsp;&nbsp;&nbsp;Integrated Circuits&nbsp;&nbsp;&nbsp;&nbsp;Mphil<br>
2012.9-2016.6&nbsp;&nbsp;[Wuhan Uni. of Sci. and Tech.](https://www.wust.edu.cn)&nbsp;&nbsp;&nbsp;&nbsp;Electronic Engineering&nbsp;&nbsp;&nbsp;&nbsp;Bachelor

## Work Experience
2022.1-now&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Microsoft](https://www.microsoft.com/zh-cn/)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WebXT&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Applied Scientist II<br>
2021.7-2021.12&nbsp;&nbsp;&nbsp;&nbsp;[TAL corp.](http://www.100tal.com/)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;AI Group&nbsp;&nbsp;&nbsp;&nbsp;Senior Image Engineer<br>
2019.6-2021.6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Intel China](https://intel.cn)&nbsp;&nbsp;&nbsp;&nbsp;[Intel Sports Group](https://www.intel.com/content/www/us/en/sports/sports-overview.html)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Machine Learning Engineer<br>
2018.7-2019.6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Intel China&nbsp;&nbsp;&nbsp;&nbsp;Intel Sports Group&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Technical Intern.<br>

## Skills
- skilled: Python/Pytorch/Git/Linux/OpenCV/
- semi-skilled: C++/JAVA/Unity3D/CUDA/TensorFlow/Keras/

## Patents
- Method and Apparatus of Game Focus Estimation in Fast Team Sports(First Owner)
- Method and Apparatus of Key Players Recognition in Team Sports(First Owner)
- Method and Apparatus of Efficient and Effective Tiny Ball Tracking
- Method and Apparatus of Game Status Detection in Team Sports
- Method and Apparatus of Estimating Ball Carrier for American Football

##  Honors
- **Intel Distinguished Invention Award.**
- **2nd place in ICCV2021 UVO segmentation competition track #2.**

## Projects
- **Monocular Human Motion Capture & Retargetting** (2021.6-2021.9)
<iframe height=300 width=500 src="//player.bilibili.com/player.html?aid=720653249&bvid=BV1WQ4y1z7bp&cid=414574687&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
<br> 
I tried two different ways to achieve motion retargetting: 1) detect human's joints and use IK to compute the joint rotation angles. 2) directly predict the joint rotation angles. And the latter is faster and more accurate.

- **2D/3D Game Focus Estimation**:<br>
In a sport game, we need to estimate an area where stories happen, to make cameras automatically focus. Game focus estimation should be quite stable, which refuses the idea that taking ball position as game focus. I did two types of game focus estimation, namely 2D and 3D, to fit different requests in our project. <br>
a demo of 3D game focus:
<iframe height=300 width=500 src="//player.bilibili.com/player.html?aid=378508007&bvid=BV1Sf4y1c7KM&cid=424336466&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe><br>


- **Key Player Recognition**:<br>
In an American Football game, some key players like Quaterback, Running Back, Wide Receiver are mostly followed by the fans. 
the rough description of 3D focus estimation is to treat every player as a node, use distance to compute node edges, and collect 55 features (including jersey number, team_id, body orientation, speed) for each node to build a graph, and use GNN to handle the graph for node classification.

- **Ball Carrier Estimation in NFL games**<br>
In most cases, the ball is invisible when occluded by player for seconds, so we estimate the player who holds ball in the gridiron instead. Ideas roughly described as: treating every player as a node of a graph, and modelling them with Graph Attention Nets.

- **Hard Negative Examples Mining for ball detection**<br>
this method is used for handling false detection in our project. Hard negatives such as bare head and arm could mightly regarded as ball by a ball detection model. Therefore, I did hard negative examples mining to mitigate false detection. roughly described as: use well-pretrained model to process train set, and save the patchs (area in bounding box) which get high score but miss the ground truth (IOU=0). I take the patchs as negatives and ball patchs as positives to train a discrimintator (a binary classifier). The discriminator could refuse most hard negatives with only subtle recall loss.  
 
- **Accelerating CNN by parallel computing on FPGAs**<br>
THis work was done at my postgraduate period. we designed a bubbling sort convolution method which can save LUTs and memories.
