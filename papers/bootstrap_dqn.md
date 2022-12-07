## [Deep Exploration via Bootstrapped DQN]([https://arxiv.org/abs/2108.09640](https://arxiv.org/pdf/1602.04621.pdf))


#### Overall impression



#### Background: Bootstrap
The bootstrap principle is, when you have a dataset D, and a parametric estimator $\phi_\theta$, $\theta$ follows the approximate posterior distribution.
To estimate the uncertainty of $\theta$, we generate bootstrap samples and estimate its mean and variance.


#### Key ideas
- The Epsilon-greedy method cannot perform temporally-extended exploration, as it's single-step. Such short-sighted exploration leads to sub-optimal results.
Bootstrapped-DQN uses a bootstrap concept in statistics for an estimatation of the uncertainty. The uncertain estimates allow the agent to direct its exploration towards potentially informative states and actions.

![image](https://user-images.githubusercontent.com/19171772/206106441-1e1641af-c23d-4a83-93cb-e08f1a5540be.png)

- The method trains a multi-head neural network as the above figure. The mean and variance of the prediction is computed as the mean and variance of prediction samples from the $K$ heads.

#### Technical details

#### Notes
