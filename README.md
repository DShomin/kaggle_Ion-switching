# [kaggle Ion-Switcing](https://www.kaggle.com/c/liverpool-ion-switching)

private rank : 79


## use model : Wavenet


## use optimizer : AdamW

## use FE : power signal, bi-directional shift signal
```python

power_signal = signal**2

```


## Ensemble : Flip model ensemble
1. Forward model
  forward X / forward y
2. Reverse model
  reverse X / reverse y
  
The output of the two models was averaged and submit.

