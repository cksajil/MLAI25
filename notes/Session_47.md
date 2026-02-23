# Sequential Models
- What are sequential models
    - RNN
    - LSTM
    - GRU
    - Seq-Seq
- Why we need sequential models
    - Real life Problems
        - One to One
        - One to Many
        - Many to One
        - Many to Many

![](https://karpathy.github.io/assets/rnn/diags.jpeg)

## RNN
![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-SimpleRNN.png)

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import SimpleRNN, Dense, Input

model_rnn = Sequential([
    Input(shape=(12,1)),
    SimpleRNN(50),
    Dense(1)
])

model_rnn.compile(optimizer='adam', loss='mse')
history_rnn = model_rnn.fit(X_train, y_train, epochs=10, validation_data=(X_test, y_test))
```


## LSTM
LSTM introduces:
- Forget gate
- Input gate
- Output gate
- Cell state

![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-chain.png)

```python
from tensorflow.keras.layers import LSTM

model_lstm = Sequential([
    Input(shape=(12,1)),
    LSTM(50),
    Dense(1)
])

model_lstm.compile(optimizer='adam', loss='mse')
history_lstm = model_lstm.fit(X_train, y_train, epochs=10,validation_data=(X_test, y_test))
```

## GRU
GRU simplifies LSTM:
- Update gate
- Reset gate
- No separate cell state

![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-var-GRU.png)

```python
from tensorflow.keras.layers import GRU

model_gru = Sequential([
    Input(shape=(12,1)),
    GRU(50),
    Dense(1)
])

model_gru.compile(optimizer='adam', loss='mse')
history_gru = model_gru.fit(X_train, y_train, epochs=10, validation_data=(X_test, y_test))
```



- Drawbacks of RNN, LSTM, GRUs
    - Vanishing Gradient
    - Exploding Gradient
    - Short term dependencies