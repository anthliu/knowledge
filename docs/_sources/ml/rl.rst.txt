.. :Authors: - Anthony Liu

.. title:: Reinforcement Learning

Reinforcement Learning
======================

Human Supervision
-----------------

COACH - Interactive learning from policy-dependent human feedback
*****************************************************************

:cite:`macglashan2017interactive`
https://arxiv.org/abs/1701.06049


TAMER
*****

:cite:`warnell2018deep`
https://arxiv.org/abs/1709.10163

Off-policy
----------

Soft Actor Critic
*****************

:cite:`haarnoja2018soft`
https://arxiv.org/pdf/1801.01290.pd

.. math::
   :label: max-ent-rl
   
   J(\pi) = \sum_{t=0}^T \mathbb{E}_{(s, a) \sim \rho_\pi} [r_t(s_t, a_t) + \alpha \mathcal{H}(\pi( \cdot | s_t))]

- Maximize objective and entropy :eq:`max-ent-rl`

Hierarchical Reinforcement Learning
-----------------------------------


Intrinsic Reward
----------------


Natural Language in Reinforcement Learning
------------------------------------------

.. bibliography:: rl.bib

