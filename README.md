# stylegan2-ada-pokemon
# Network
Stylegan2-ada

https://github.com/NVlabs/stylegan2-ada


# Datasets
Pokemon Images Dataset

Dataset of 819 Pokemon images

https://www.kaggle.com/kvpratama/pokemon-images-dataset

# Settings
100kimgs

# Result
![1](1.jpg)
![2](2.jpg)

# More
遠目に見るとしっかりした新種のポケモンに見えるが近づくと不気味なポケモンが生成されてしまっている  
fid(Frechet Inception Distance)が
※生成画像と元の画像の分布の近さを示す指標  
tick:fid:  
50:192  
100:138  
150:83  
200:61  
248:58  

で収束しきっていないので学習を進めるともっと高品質な画像が生成できる可能性がある。
ただ、同じようなフォルムのポケモンが生成されてしまっているのでモード崩壊を起こしている可能性がある。

