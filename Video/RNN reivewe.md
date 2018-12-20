# RNN
* Same hidden function and weight are re-use in every time stamp

## Vanishing/Exploding Gradients
* Backpropagation from ht to ht-1 multiplies by W 
* Computing gradient of h0 involves many factors of W (and repeated tanh)
* Largest singular value > 1:
Exploding gradients
* Largest singular value < 1:
Vanishing gradients

### SOlution
* Gradient clipping: Scale gradient if its norm is too big ( For gradient explosion)
* Change RNN architecture, LSTM etc (Gradient vanishing)
![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Selection_006.png)
* Truncated Backpropagation through time: Run forward and backward through chunks of the sequence instead of whole sequence

## LSTM 
i: Input gate, whether to write to cell
f: Forget gate, Whether to erase cell
o: Output gate, How much to reveal cell
g: Gate gate, How much to write to cell

![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Selection_005.png)

