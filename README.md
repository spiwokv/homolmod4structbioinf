# Homology modelling tutorial for Structural biology

The aim of this tutorial is to learn homology modelling. Tomato nuclease will be used as an example.
This structure has been solved experimentally (3SNG, Koval et al. 2013, Acta Crystallogr.,Sect.D 69, 213-226
<doi:10.1107/S0907444912043697>) but for the purpose of this tutorial we will forget it and we will
pretend that it has not been solved. Instead, we will predict it on the basis of *Arabidopsis* nuclease
(4CXP, easy task) or bacterial nuclease (1AK0, more advanced task).

1. Clone this repository by typing:
```
git clone https://github.com/spiwokv/homolmod4structbioinf.git
```
This will create a directory `homolmod4structbioinf`. Go to this directory. It contains two subdirectories, `basedon4CXP`
and `basedon1AK0 `. Let us start with the easier one (`basedon4CXP`) and follow with the more advanced one (`basedon1AK0`).

2. Make a binary sequence alignment of the tomato nuclease (`Q0KFV0 `) and the template. For `4CXP ` you can use BLAST.
For `1AK0` use PHYRE2. Go to the directory and edit sequence alignment in `alignment.ali`. Then edit `model-default.py`
and make necessary changes.

3. Run modeller by:
```
python model-default.py
```
In case of errors make necessary corrections. Download the resulting file by scp (command in PC console), e.g.:
```
pscp.exe root@IP_address:/root/homolmod4structbioinf/basedon4CXP/model.B99990001.pdb .
```

