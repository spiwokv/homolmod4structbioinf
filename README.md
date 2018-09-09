# Homology modelling tutorial for Structural biology course

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
For `1AK0` use PHYRE2. Go to the directory and edit sequence alignment in `alignment.ali`. The alignment must strictly
follow the required format:
```
C; A sample alignment in the PIR format; used in tutorial

>P1;5fd1
structureX:5fd1:1    :A:106  :A:ferredoxin:Azotobacter vinelandii: 1.90: 0.19
AFVVTDNCIKCKYTDCVEVCPVDCFYEGPNFLVIHPDECIDCALCEPECPAQAIFSEDEVPEDMQEFIQLNAELA
EVWPNITEKKDPLPDAEDWDGVKGKLQHLER*

>P1;1fdx
sequence:1fdx:1    : :54   : :ferredoxin:Peptococcus aerogenes: 2.00:-1.00
AYVINDSC--IACGACKPECPVNIIQGS--IYAIDADSCIDCGSCASVCPVGAPNPED-----------------
-------------------------------*
```
- Line 1: Do not change.
- Line 2: Leave empty.
- Line 3: Name of the template - change to PDB ID, e.g. change 5fd1 to 4CXP.
- Line 4: Replace 5fd1 to 4CXP, change 1 and 106 to initial and final residue number, respectively.
  Change A and A to initial and final chain ID. Other fields may be ignored. Don't manipulate with colons!
- Line 5 and 6: Replace the sequence to sequence of 4CXP FROM THE ALIGNMENT (WITH ALL GAPS!). Add star at the end.
  You can add more lines.
- Line 7: Leave empty.
- Line 8 and so for: make corresponding changes for the model sequence. Number 54 may be replaced by `@`
  (it is calculated automatically).

Then edit `model-default.py` and make necessary changes:
- Change 5fd1 to 4CXP.
- Change 1fdx to anything you want.

3. Run modeller by:
```
python model-default.py
```
In case of errors make necessary corrections. Download the resulting file by scp (command in PC console), e.g.:
```
pscp.exe root@IP_address:/root/homolmod4structbioinf/basedon4CXP/model.B99990001.pdb .
```

4. Compare the model with the experimental structure.
