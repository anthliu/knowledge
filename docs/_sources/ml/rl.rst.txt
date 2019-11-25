.. :Authors: - Anthony Liu

.. title:: Reinforcement Learning

Reinforcement Learning
======================

Human Supervision
-----------------

Reward Shaping
**************

- COACH - Interactive learning from policy-dependent human feedback :cite:`macglashan2017interactive` https://arxiv.org/abs/1701.06049
- TAMER - :cite:`warnell2018deep` https://arxiv.org/abs/1709.10163
- End2end robotic RL without reward engineering https://arxiv.org/abs/1904.07854
- Learning from human preferences https://openai.com/blog/deep-reinforcement-learning-from-human-preferences/

Imitation Learning
******************

- Hierarchical Imitation and Reinforcement Learning https://arxiv.org/pdf/1803.00590.pdf
- Imitation learning tutorial ICML 2018 https://sites.google.com/view/icml2018-imitation-learning/
- Third-Person Visual Imitation Learning viaDecoupled Hierarchical Controller https://pathak22.github.io/hierarchical-imitation/

Off-policy
----------

- Soft Actor Critic :cite:`haarnoja2018soft` https://arxiv.org/pdf/1801.01290.pdf

Soft Actor Critic
*****************

:cite:`haarnoja2018soft`
https://arxiv.org/pdf/1801.01290.pdf

.. math::
   :label: max-ent-rl
   
   J(\pi) = \sum_{t=0}^T \mathbb{E}_{(s, a) \sim \rho_\pi} [r_t(s_t, a_t) + \alpha \mathcal{H}(\pi( \cdot | s_t))]

- Maximize objective and entropy :eq:`max-ent-rl`

Hierarchical Reinforcement Learning
-----------------------------------

- (2002) Learning Options in Reinforcement Learning https://arxiv.org/abs/1805.08296
- Option Critic Architecture https://arxiv.org/pdf/1609.05140.pdf

    - Uses policy gradient methods in options learning
    - Passes gradients through high level policy and option policies
    - Need termination for each function
    - (From efficient HRL - prone to learning options that terminate after one step)

- (HIRO) Data efficient HRL https://arxiv.org/abs/1805.08296

(HIRO) Data efficient HRL
*************************
:cite:`nachum2018data`
https://arxiv.org/abs/1805.08296

- Off policy training for high/low level policy
- Parameterized goals and rewards

    - High level policy produces goals g_t
    - :math:`g_t` directs low level policy to try to reach state :math:`s_t + g_t`, from :math:`s_t`
    - (Natural setting - position of agent in grid)
    - Intrinsic reward = :math:`-||s_t + g_t - s_{t+1}||`
    - Many prior works generally require some on-policy training, as changing behavior of lower level policy changes how high level behaves
    - HIRO takes correction (makes true goal more likely to happen)

Intrinsic Reward
----------------

* (VIC) variational intrinsic control https://arxiv.org/pdf/1611.07507.pdf
* (DIAYN) diversity is all you need https://arxiv.org/abs/1802.06070
* (SNN4RL) Stochastic Neural Networks for HRL https://github.com/florensacc/snn4hrl
* Dynamics aware unsupervised discovery of skills https://arxiv.org/pdf/1907.01657.pdf
* Unsupervised Control Through Non-Parametric Discriminative Rewards https://arxiv.org/pdf/1811.11359.pdf

(DIAYN) diversity is all you need
*********************************
:cite:`eysenbach2018diversity`
https://arxiv.org/abs/1802.06070

- No reward, only diversity
- Distinguish skill from state only

Dynamics aware unsupervised discovery of skills
***********************************************

https://arxiv.org/pdf/1907.01657.pdf
:cite:`sharma2019dynamics`

- Like DIAYN
- Distinguish skill from state and predictability of next state (dynamics)

(SNN4RL) Stochastic Neural Networks for HRL
*******************************************
:cite:`florensa2017stochastic`
https://github.com/florensacc/snn4hrl

- Learning skills under a single task reward that generalizes to other skills

Unsupervised Control Through Non-Parametric Discriminative Rewards
******************************************************************
:cite:`warde2018unsupervised`
https://arxiv.org/pdf/1811.11359.pdf

- Model free architecture - learn a goal state conditioned policy:

    - :math:`\pi_\theta (a | s; s_g)` - reach any state :math:`s_g` from :math:`s`
    - Goal achievement reward :math:`r(s, s_g)` measures how similar :math:`s` and :math:`s_g` are using mutual information
    - Is able to deal with states out of reach


Natural Language in Reinforcement Learning
------------------------------------------

* A Survey of Reinforcement Learning Informed by Natural Language https://arxiv.org/pdf/1906.03926.pdf
* Language as an Abstraction for Hierarchical Deep Reinforcement Learning https://arxiv.org/pdf/1906.07343.pdf


.. bibliography:: rl.bib

