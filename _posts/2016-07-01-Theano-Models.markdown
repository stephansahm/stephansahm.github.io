---
layout: default
github: https://github.com/schlichtanders/theano_models
keywords: python, theano, symbolic programming, numpy, gpu
description: Lightweight package for building machine learning models, on top of theano.
---

theano_models is a high-level package around theano which implements a ``Model``
type to pre-structure the (occasionally rather big) theano expression graphs.
It is meant for clean programming of symbolic models, for instance Multilayer
Perceptrons (MLP) or probabilistic modeling.

The package was developed as part of my master thesis.

##### Its Strength
The ``Model`` gives a powerful view on the graphs,
ready for interactive coding / prototyping, while being transparent and
lightweight. It strengthens the underlying simplicity of theano.

For those, who know about the OpFromGraph by theano, this is a generic, faster,
and better integrable alternative, at least I think so.
It offers maximum control, while still making
higher-level pre-structuring as simple as working with theano expressions
directly.


##### Visualization

Please enjoy the visualization of a Multi Layer Perceptron Model,
consisting out of three layers (AffineNonLinear Model),
which is fed into a GaussianNoise Model. The interactive visualization corresponds to the loss function, here the negative loglikelihood.
It is build from the probability distribution function of the GaussianNoise.

Try to click on the yellow nodes:
<iframe src="{{ "/examples/tmp/loss.html" | prepend: site.baseurl }}" height="500">
  - sorry iframe does not work -
</iframe>
