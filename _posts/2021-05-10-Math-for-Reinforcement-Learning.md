---
published: true
---
## Probability Primer

In this post I list some results from probability and derive the Bellman equations for the state and action value functions.


$$ \mathbb{E}[X|Y=y] = \sum_{z} \mathbb{E}[X|Y=y, Z=z] p_{Z|Y}(z|y)$$

$$ \begin{equation}
\mathbb{E}[X|Y=y] = \sum_{z} \mathbb{E}[X|Y=y, Z=z] p_{Z|Y}(z|y)  \tag{eqnt}\label{eq:one}
\end{equation}
$$

$$ \mathbb{E}[X|Y=y] = \sum_{z} \mathbb{E}[X|Y=y, Z=z, A=a] p_{Z, A|Y}(z, a|y)$$

$$ G_t = R_{t+1} + \gamma G_{t+1} $$

$$ v_{\pi}(s) = \mathbb{E}_{\pi} [G_{t}|S_t = s] = \mathbb{E}_{\pi} [ R_{t+1} + \gamma G_{t+1}|S_t = s]$$

$$ q_{\pi}(s, a) = \mathbb{E}_{\pi} [G_{t}|S_t = s, A_t=a] = \mathbb{E}_{\pi} [ R_{t+1} + \gamma G_{t+1}|S_t = s, A_t = a]$$

From e\eqref{eq:one} we get
$$ v_{\pi}(s) = \mathbb{E}_{\pi} [G_{t}|S_t = s] = \sum_{a} \pi(a|s)\mathbb{E}_{\pi} [ R_{t+1} + \gamma G_{t+1}|S_t = s, A_t = a] = \sum_{a} \pi(a|s)q_{\pi}(s, a)$$
