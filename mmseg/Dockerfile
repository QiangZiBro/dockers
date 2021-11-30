FROM qiangzibro/mmlab-fundamental:torch18-cu102-cudnn7
RUN git clone https://github.com/open-mmlab/mmsegmentation.git /mmsegmentation
WORKDIR /mmsegmentation
ENV FORCE_CUDA="1"
RUN pip install -r requirements.txt
RUN pip install --no-cache-dir -e .
WORKDIR /workspace
