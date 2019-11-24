.. :Authors: - Anthony Liu

.. title:: Representation Learning

Representation Learning
=======================

Manifold Learning
-----------------

Hyperspherical Variational Auto-Encoders
****************************************

https://arxiv.org/abs/1804.00891

- Variational autoencoders typically sample from convenient gaussian prior
  for variational inference.
- This can break in non-homeomorphic cases --
  imagine dataset on a circle :math:`\mathcal{Z} = \mathcal{S}^1`,
  is embedded into :math:`\mathcal{X} \subset \mathbb{R}^N`.
  An autoencoder can easily discover the circle, whereas VAE becomes unstable.
- Manifold mismatch.
- In many modern problems, data is normalized to focus on the directional
  distribution, but the spherical nature of data is not addressed.
- This paper proposes *von Mises-Fisher* distribution as alternative to
  gaussian prior. (also uninformative prior).

*X*-Shot Learning
-----------------

Infinite Mixture Prototypes for Few-Shot Learning
*************************************************
https://arxiv.org/abs/1902.04552

.. bibliography:: repl.bib
