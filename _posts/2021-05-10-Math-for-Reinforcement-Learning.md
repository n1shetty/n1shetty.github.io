---
published: true
---
## Probability Primer

In this post I list some results from probability and derive the Bellman equations for the state and action value functions.


$$ \begin{equation} 
\mathbb{E}[X|Y=y] = \sum_{z} \mathbb{E}[X|Y=y, Z=z] p_{Z|Y}(z|y) \tag{1}\label{eq:one}
\end{equation}
$$


$$ \begin{equation}
\mathbb{E}[X|Y=y] = \sum_{z} \mathbb{E}[X|Y=y, Z=z, A=a] p_{Z, A|Y}(z, a|y) \tag{2}\label{eq:two}
\end{equation}
$$

$$ G_t = R_{t+1} + \gamma G_{t+1} $$

$$ \begin{equation}
v_{\pi}(s) = \mathbb{E}_{\pi} [G_{t}|S_t = s] = \mathbb{E}_{\pi} [ R_{t+1} + \gamma G_{t+1}|S_t = s] \tag{3}\label{eq:three}
\end{equation}
$$

$$ \begin{equation}
q_{\pi}(s, a) = \mathbb{E}_{\pi} [G_{t}|S_t = s, A_t=a] = \mathbb{E}_{\pi} [ R_{t+1} + \gamma G_{t+1}|S_t = s, A_t = a] \tag{4}\label{eq:four}
\end{equation}
$$

From equations \eqref{eq:one}, \eqref{eq:three} and \eqref{eq:four}, we get
$$ \begin{aligned}
v_{\pi}(s)& = & \mathbb{E}_{\pi} [G_{t}|S_t = s] \\
          & = & \sum_{a} \pi(a|s)\mathbb{E}_{\pi} [ R_{t+1} + \gamma G_{t+1}|S_t = s, A_t = a] \\
          & = & \sum_{a} \pi(a|s)q_{\pi}(s, a)
\end{aligned}
$$
