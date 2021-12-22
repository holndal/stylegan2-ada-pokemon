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
あとは初期設定。

# Requirements
※stylegan2 adaをコピーしました。
- Linux and Windows are supported, but we recommend Linux for performance and compatibility reasons.
- 64-bit Python 3.6 or 3.7. We recommend Anaconda3 with numpy 1.14.3 or newer.
- We recommend TensorFlow 1.14, which we used for all experiments in the paper, but TensorFlow 1.15 is also supported on Linux. TensorFlow 2.x is not supported.
- On Windows you need to use TensorFlow 1.14, as the standard 1.15 installation does not include necessary C++ headers.
- 1–8 high-end NVIDIA GPUs with at least 12 GB of GPU memory, NVIDIA drivers, CUDA 10.0 toolkit and cuDNN 7.5.
- Docker users: use the provided Dockerfile to build an image with the required library dependencies.

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

# Install
```
git clone https://github.com/NVlabs/stylegan2-ada

cd stylegan2-ada
python train.py --outdir={出力ディレクトリ} --gpu={GPUのid} --data={データセット}
# (option一覧) python train.py --help
```
