# Notes GMP

## 1st train attempt

* First train attempt: Fri. Dec. 21st, 2018. 10:51 pm
* Machine: Ubuntu 16.04
* Location: Paperspace
* [Corpus](https://github.com/guillemontecinos/tensorflow-wavenet/tree/master/corpus)
* [Corpus Reference](https://www.youtube.com/watch?v=lrcW_VGBwbM)
* `--num_steps=50000`
* `--silence_threshold=0.01`
* Command executed: `python train.py --data_dir=corpus --silence_threshold=0.01 --num_steps=50000`
* Expected end time: Mon. Dec. 24th, 2018. 4:51 am
* Actual end: Mon. Dec. 24th, 2018. 1:00 pm (approximately)

### Model generated
* `logdir/train/2018-12-21T22-50-05/model.ckpt-49999`

### Generated data
* To generate 1 sec: `python generate.py --wav_out_path=generated.wav -- samples 16000 logdir/train/2018-12-21T22-50-05/model.ckpt-49999`
* Generated examples [here](https://github.com/guillemontecinos/tensorflow-wavenet/tree/master/generated)

## 2nd train attempt

* Corpus: Radiohead raw sound in .wav (converted from .mp3 using ffmpg)
  * The Bends
  * Ok Computer
  * Kid A
  * In Rainbows
  * The King of Limbs
  * A Moon Shaped Pool
* Total corpus: 2.62 Gb
* Time/step: 20 seconds approximately
* Status: Not trained
