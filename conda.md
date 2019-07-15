# jupyter kernal keeps dying
Can you try uninstalling all of:

```
ipykernel
ipython
jupyter_client
jupyter_core
traitlets
ipython_genutils
```

And then install again. If you're doing this inside a conda env, it might be easiest to create a new environment and start from scratch. Also, if you're going to install with conda, run conda clean -tipsy to clean up conda caches before you start.

[source](https://github.com/jupyter/notebook/issues/1892#issuecomment-260403964)
