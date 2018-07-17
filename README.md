# Getting Started
If you are unfamiliar with doing data science with python (I recommend python3):

I find that virtual environments solve a lot of headaches with pip, set one up to have an isolated copy of an environment for your projects

Check to see if you have it already: `virtualenv --version`

```
pip3 install virtualenv
mkdir ~/env
virtualenv ~/env/app
source ~/env/app/bin/activate # inside bin directory
deactivate # when you are done
```

When you have activated your virtual environment:

```
pip3 install tensorflow, numpy, pandas, keras, jupyter
```

To open up the notebook:

```
jupyter notebook
```

**If you already have the above set up:**

You can look at the last generated results file and load pre-existing model weights.

## A Brief Explanation

Goal: Generate pokemon names

I downloaded my pokemon table from Kaggle (https://www.kaggle.com/rounakbanik/pokemon).

This demo runs off 3 LSTM layers each with ` vocal_size` hidden layers to avoid losing information in an information bottleneck

I use the same dropout mask because Yarin Gal determined that using the same dropout mask at every timestep allows my network to propagate learning error through time whereas a random one would disrupt the error signal

Eventually, I want to be able to not only generate a name, but types and descriptions like a real pokedex.

Many thanks to Trung Tran for: https://github.com/ChunML/text-generator

