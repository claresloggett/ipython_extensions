# Miscellaneous IPython extensions

You can install each extension individually, or you can link the extension directories
into your IPython directories (what I do):

    ln -s $(pwd)/extensions $(ipython locate profile)/extensions
    ln -s $(pwd)/nbextensions $(ipython locate profile)/nbextensions

If you want to install into a profile other than default, you can replace 
`$(ipython locate profile)` with e.g. `$(ipython locate profile nbserver)` here and below.

## Gist

Add a gist button to the notebook toolbar:

    $ curl https://rawgithub.com/minrk/ipython_extensions/master/nbextensions/gist.js > $(ipython locate profile)/nbextensions/gist.js

and load it by adding to your custom.js, found in `$(ipython locate profile)/static/custom/custom.js`:

```javascript
IPython.load_extensions('gist');
```


## Retina Figures

Enable 2x display of matplotlib figures (no longer necessary on IPython master)

install the extension:

    %install_ext https://rawgithub.com/minrk/ipython_extensions/master/extensions/retina.py

load the extension:

    %load_ext retina

## Table of Contents 

Generates floating table of contents inside your notebook from the heading cells.
Adds a button to the toolbar to toggle the floating table of contents.

install the extension:

    $ curl https://rawgithub.com/minrk/ipython_extensions/master/nbextensions/toc.js > $(ipython locate profile)/nbextensions/toc.js
    $ curl https://rawgithub.com/minrk/ipython_extensions/master/nbextensions/toc.css > $(ipython locate profile)/nbextensions/toc.css

and load it with this in your custom.js:

```javascript
IPython.load_extensions('toc');
```
