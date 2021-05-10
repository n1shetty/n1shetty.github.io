---
published: true
---
## Probability Primer

In this post I will list and explain some results from probability that will help with the derivations of the Bellman equations for the state and action value functions.


$$ \mathbb{E}[X|Y=y] = \sum_{z} \mathbb{E}[X|Y=y, Z=z] p_{Z|Y}(z|y)$$

$$ \mathbb{E}[X|Y=y] = \sum_{z} \mathbb{E}[X|Y=y, Z=z, A=a] p_{Z, A|Y}(z, a|y)$$

$$ v_{\pi}(s) = \mathbb{E}_{\pi} [G_{t}|S_t = s]$$
