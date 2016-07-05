---
layout: default
img-preview: theano_models-preview.png
img: theano_models.png
alt: theano_models
client: theano_models
clienturl: javascript:void(0);
projecturl: javascript:void(0);
category: python, theano, symbolic programming, numpy, gpu
description: Lightweight model-building package, build upon theano.
---

theano_models is a high-level package around theano which implements a ``Model``
type to pre-structure the (occasionally rather big) theano expression graphs
It is meant for clean programming of symbolic models, for instance Multilayer
Perceptrons (MLP) or probabilistic modeling.

The ``Model`` gives a powerful view on the graphs,
ready for interactive coding / prototyping, while being transparent and
lightweight. It strengthens the underlying simplicity of theano.

For those, who know about the OpFromGraph by theano, this is a generic, faster,
and better integrable alternative, at least I think so.
It offers maximum control, while still making
higher-level pre-structuring as simple as working with theano expressions
directly.

It was developed as part of my master thesis, which is not done yet, and hence
the code is still private. It will be open sourced afterwards, extending also
this little introduction.


As a preview, please consider this visualization of a MLP Model,
consisting out of two layers (AffineNonLinear Model),
which is fed into a GaussianNoise Model.

The code will follow as soon at it is open source.

<!-- <iframe src="{{ /examples/tmp/loss.html | prepend: site.baseurl }}"/> -->
