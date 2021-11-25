## mm-lab系列的基础设施

由于每次编译整个mmlab要花较久时间，这里通过GIthub Actions预编译上层docker镜像，并发布到我的docker hub上，以方便下游应用使用。

对于新的应用需求，比如说要装**mmcls**

```Dockerfile
FROM qiangzibro/mmlab-fundamental:torch18-cu102-cudnn7
RUN git clone https://github.com/open-mmlab/mmclassification.git
WORKDIR ./mmclassification
RUN pip install --no-cache-dir -e .
```
