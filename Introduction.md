# Introduction

![Daniel Gregoire via Unsplash](https://images.unsplash.com/photo-1540187334920-54e87c2771c0)

## Why Google Colab

TLDR: [Google Colab](https://colab.research.google.com/) is (kind of) a standardized environment, it's free and it is instantly available.

### Price
Let's get this out of the way; first of all, Colab is free (as in beer).


### It's a standardized Python (and Linux) Environment

While theoretically you _might_ have a Python installation (or many) already on your own comnputer, version management can be a pain.

You would need to (and you should) learn about virtualenvs (if you're on macOS, [this guide](https://medium.com/marvelous-mlops/the-rightway-to-install-python-on-a-mac-f3146d9d9a32) is great), then once you set up a new one for a project, you'd still need to install your prerequisites (as we'll see in the next section, Colab comes with lots of scientific computing libraries pre-installed), and on top of this, create an environment for notebooks (e.g. with JupyerLab). (Impossible? I am not saying that -- just that Colab is also a great tool.)

But here is the thing: assume you possess or just aquired the above knowlege. How about sharing your work with someone else? You'd now need to take your friend(s) on the above journey first before they end up with the same environment -- and this is assuming they are also on the same OS. And as much fun as virtualenvs might be for you, it is less fun for your friend to listen to you lecturing them about it. On the other hand, If your code works in a fresh Colab compute, so should it for your friend. Within reason, see next paragraph:

Are there limits to this argument? Surely. Google can decide any moment (and probably many times a month does decide) that certain libraries are removed, added, updated (to mitigate this, it can be good practice to capture the output of `pip freeze`), or the whole offering is [closed down](https://killedbygoogle.com/). Don't rely on it for long-term, critical work. But for short-term learning and experimentation? It is great.

### Availability

All you need is a browser: you could even run Colab from an iPad, more or less. If you need to shut your laptop for a few minutes (not hours), your Colab session would probably survive that and keep churning in the meantime. And if you have to put up with VM startup times in other envs, not in Colab.

## Why DuckDB

[DuckDB](https://duckdb.org/) is a formidable new single-machine analytics tool, tracing its origins to the same Dutch research institute as Python. Crucially for this guide, it comes with a remarkably good [Spatial extension](https://duckdb.org/docs/stable/core_extensions/spatial/overview.html) (and comes pre-installed on Colab).

## In/Out of Scope

In scope: vector data

Out of scope: raster data, data bigger than what fits in (free) Colab, ML/AI
