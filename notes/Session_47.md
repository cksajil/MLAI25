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


$$h_t = \tanh(W_x x_t + W_h h_{t-1} + b)$$

$$y_t = W_yh_t$$


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

Let the concatenated input be:

$$z_t = [h_{t-1}, x_t]$$


- Forget Gate

$$f_t = \sigma(W_f z_t + b_f)$$
![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-f.png)
- Input Gate
$$i_t = \sigma(W_i z_t + b_i)$$

- Cell State
$$\tilde{C}_t = \tanh(W_c z_t + b_c)$$

![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-i.png)

- Cell State Update

$$ C_t = f_t \odot C_{t-1} + i_t \odot \tilde{C}_t$$

![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-C.png)

- Output Gate

$$o_t = \sigma(W_o z_t + b_o)$$

- Hidden State

$$ h_t = o_t \odot \tanh(C_t)$$

![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-o.png)

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