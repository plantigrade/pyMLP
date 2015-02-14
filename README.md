## pyMLP: Molecular Lipophilicity Potential evaluator

### Presentation

pyMLP is a program computing the molecular lipophilicity
potential map of proteins.

### References

Please include this reference in published work using pyMLP:

* Broto P., Moreau G., Vandycke C. - 
*Molecular structures: Perception, autocorrelation descriptor and sar studies.
 System of atomic contributions for the calculation of the n-octanol/water 
 partition coefficients*, Eu. J. Med. Chem. 1984, 19.1, 71-78

* Laguerre M., Saux M., Dubost J.P., Carpy A. -
*MLPP: A program for the calculation of molecular lipophilicity potential in
 proteins*, Pharm. Sci. 1997, 3.5-6, 217-222

This program was developed in python as a platform independent equivalent of 
MLPP (see references). As a result pyMLP may run on any platform supported by
Python and Numpy.


### INSTALLATION

In order to launch pyMLP you will need:
* a working python installation (http://www.python.org) (tested with version
  2.4 and 2.5) (any desktop oriented Linux distribution should have already one installed)
* a working numpy installation (http://numpy.scipy.org/)
  (any scientific friendly Linux distribution should have it in its repository)

(pyMLP was reported to work on win32 with Enthought's Python Sumo-Distribution
for Windows (http://www.enthought.com/))

With a properly configured python + numpy install, you just have to input this
command to the CLI (command line interface):
```
python pyMLP.py
```
#### Optional

In order to have pyMLP.py available from any directory you can copy it in your
PATH (after enabling direct execution):
```
chmod +x pyMLP.py
cp pyMLP.py /usr/local/bin/
```

Then you can directly launch pyMLP that way:
```
pyMLP.py
```

### USAGE

pyMLP takes a .pdb file as input and output a .dx map file easily visualized in
many molecular visualization packages such as VMD, Pymol, Chimera, ...

Please run `pyMLP.py --help` for detailed instructions.

Simple examples:

* Command to calculate foo.dx the lipophilicity potential map of foo.pdb:
  (assuming pyMLP.py is in your PATH and foo.pdb in the current directory
   this command will create foo.dx in the current directory)
```
pyMLP.py -i foo.pdb
```
* Command that will achieve exactly the same thing as the one above but be
  more verbose about what is being done:
```
pyMLP.py -v -i foo.pdb
```

### FOOTNOTE

Feel free to criticize pyMLP code: it needs some serious refactoring and way
more comments ... alas it works for me ... sorry

(from the quick-n-dirty-dev-dpt)

last modified March 28, 2007 by Julien Lefeuvre

