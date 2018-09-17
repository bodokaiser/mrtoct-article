# MR to CT

## u-net losses

1. Mean Absolute Error

```
python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mae/training.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mae/model.ckpt-5663

python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mae/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mae/model.ckpt-5663
```

2. Mean Squared Error

```
python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mse/training.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mse/model.ckpt-6104

python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mse/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mse/model.ckpt-6104
```

3. 3 x Mean Absolute Error + Gradient Distance Loss

```
python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/3mae-gdl/training.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/3mae-gdl/model.ckpt-14301

python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/3mae-gdl/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/3mae-gdl/model.ckpt-14301
```

4. Mean Absolute Error + 1e-6 x Gradient Distance Loss

```
python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mae-1e-6gdl/training.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mae-1e-6gdl/model.ckpt-14301

python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mae-1e-6gdl/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mae-1e-6gdl/model.ckpt-14301
```

5. Mean Absolute Error + 1e-7 x Gradient Distance Loss

```
python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mae-1e-7gdl/training.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mae-1e-7gdl/model.ckpt-19388

python predict_unet.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/unet/mae-1e-7gdl/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/unet/mae-1e-7gdl/model.ckpt-19388
```

## pixtopix

1. Min Max

```
python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/minmax/training.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/minmax/model.ckpt-7328

python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/minmax/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/minmax/model.ckpt-7328
```

2. Least Square

```
python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/lsquare/training.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/lsquare/model.ckpt-26711


python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/lsquare/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/lsquare/model.ckpt-26711
```

3. 1e-7 x Least Square

```
python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/lsquare1e-7/training.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/lsquare1e-7/model.ckpt-18885

python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/lsquare1e-7/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/lsquare1e-7/model.ckpt-18885
```

4. 1e-7 x Least Square (trained clean)

```
python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/validation-mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/lsquare-clean/validation.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/lsquare-clean/model.ckpt-51911

python predict_pixtopix.py \
  --inputs-path data/tfrecord/cleaned/mr.tfrecord \
  --outputs-path ../mrtoct-results/pixtopix/lsquare-clean/training.tfrecord \
  --checkpoint-path ../mrtoct-results/pixtopix/lsquare-clean/model.ckpt-51911
```
