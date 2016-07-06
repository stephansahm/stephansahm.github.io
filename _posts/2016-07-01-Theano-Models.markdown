---
layout: default
keywords: python, theano, symbolic programming, numpy, gpu
description: Lightweight package for building machine learning models, on top of theano.
---

theano_models is a high-level package around theano which implements a ``Model``
type to pre-structure the (occasionally rather big) theano expression graphs.
It is meant for clean programming of symbolic models, for instance Multilayer
Perceptrons (MLP) or probabilistic modeling.

##### Its Strength
The ``Model`` gives a powerful view on the graphs,
ready for interactive coding / prototyping, while being transparent and
lightweight. It strengthens the underlying simplicity of theano.

For those, who know about the OpFromGraph by theano, this is a generic, faster,
and better integrable alternative, at least I think so.
It offers maximum control, while still making
higher-level pre-structuring as simple as working with theano expressions
directly.


##### Preview

It was developed as part of my master thesis, which is not done yet, and hence
the code is still private. It will be open sourced afterwards, extending also
this little introduction.

As a preview, please consider this visualization of a MLP Model,
consisting out of three layers (AffineNonLinear Model),
which is fed into a GaussianNoise Model. You see / interact with the loss function,
which is build from the probability distribution function of the GaussianNoise,
in log space (for numeric reasons).

Try to click on the yellow nodes:
<iframe src="{{ "/examples/tmp/loss.html" | prepend: site.baseurl }}" height="500">
  - sorry iframe does not work -
</iframe>

The code will follow as soon at it is open source.
