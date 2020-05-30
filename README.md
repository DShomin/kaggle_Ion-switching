# [kaggle Ion-Switcing](https://www.kaggle.com/c/liverpool-ion-switching)

private rank : 79</br>
This code was created from [Mobassir's](https://www.kaggle.com/mobassir) [public kernel](https://www.kaggle.com/mobassir/understanding-ion-switching-with-modeling) base.

## model : Wavenet

## optimizer : AdamW

## FE(Feature Engineering)
power signal, bi-directional shift signal
```python

# power signal
power_signal = signal**2

# bi-directional shift signal per batch
df['signal_shift_pos_' + str(window)] = df.groupby('group')['signal'].shift(window).fillna(0)
df['signal_shift_neg_' + str(window)] = df.groupby('group')['signal'].shift(-1 * window).fillna(0)

```


## Ensemble : Flip model ensemble
1. Forward model
  forward X / forward y
2. Reverse model
  reverse X / reverse y
  
The output of the two models was averaged and submit.

