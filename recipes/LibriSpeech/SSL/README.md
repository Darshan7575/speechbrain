# wav2vec 2.0 pretraining with SpeechBrain

To run call `python train.py hparams/train_wav2vec.yaml --find_unused_parameters --max_grad_norm 0.0`

See config file for model definition.

The model is split into two parts, the latent extractor (typically a CNN) and the latent encoder (typically a transformer). The latter outputs a dictionary with the encoded embeddings under the "embeddings" key. See `compute_forward()` in `train.py` for usage.