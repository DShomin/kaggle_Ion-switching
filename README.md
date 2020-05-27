# kaggle Ion-Switcing

private rank : 79


## use model : Wavenet


## use optimizer : AdamW

## use FE : power signal, bi-directional shift signal

## Ensemble : Flip model ensemble
1. Forward model
  forward X / forward y
2. Reverse model
  reverse X / reverse y
  
The output of the two models was averaged and submit.

