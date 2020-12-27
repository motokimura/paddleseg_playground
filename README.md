# paddleseg_playground

This repository provides Docker environment with which
you can play around with [PaddleSeg framework](https://github.com/PaddlePaddle/PaddleSeg).

## Setup

Prepare the container with CUDA 11.0:

```
docker-compose run --rm --service-ports paddleseg bash
```

Or, prepare the container with CUDA 10.2:

```
docker-compose run --rm --service-ports paddleseg_cuda10 bash
```

## Quick Training

Check if the container has been correctly setup:

```
python train.py \
       --config configs/quick_start/bisenet_optic_disc_512x512_1k.yml \
       --do_eval \
       --use_vdl \
       --save_interval 500 \
       --save_dir output
```

This will be finished within ~5 min.

You can monitor the progress via
[VisualDL](https://github.com/PaddlePaddle/VisualDL).
After starting VisualDL server as follows, open http://localhost:8040 from your web browser.

```
visualdl --logdir output/ --port 8040 --host 0.0.0.0
```


## PaddleSeg Tutorials

Setup has been done!

Follow [PaddleSeg official tutorial](https://github.com/PaddlePaddle/PaddleSeg#tutorials).
