# container_notes

## lico user guide
see pdf file

## 用singularity 创建镜像
https://www.cnblogs.com/lisuhang/p/16159475.html

- 创建python镜像

singularity build --sandbox pytorch docker://python:3.8

- 交互模式运行

singularity shell -w pytorch

- 安装包
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

- 打包镜像

sudo singularity build pytorch.sif pytorch/

- 镜像测试

singularity exec --nv ../pytorch.sif python train.py
