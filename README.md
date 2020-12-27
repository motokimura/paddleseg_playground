# paddleseg_playground

This repository provides Docker environment with which
you can play around with [PaddleSeg framework](https://github.com/PaddlePaddle/PaddleSeg).

## Setup

Prepare the container with CUDA 11.0:

```
docker-compose run --rm paddleseg bash
```

Or, prepare the container with CUDA 10.2:

```
docker-compose run --rm paddleseg_cuda10 bash
```

## Quick Training

Check if the container has been correctly setup:

```
python train.py --config configs/quick_start/bisenet_optic_disc_512x512_1k.yml
```

This will be finished within ~5 min.


## PaddleSeg Tutorials

Setup has been done!

Follow [PaddleSeg official tutorial](https://github.com/PaddlePaddle/PaddleSeg#tutorials).
