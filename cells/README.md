# Skywater 130nm gridded cells for ACT flow

This directory contains gridded cells for use with the Skywater 130nm process
and the ACT tools---in particular, bundled-data circuits generated using 
`chp2prs`. There are two groups of cells: explicitly instantiated cells
from logic synthesis that use the ACT standard cell library, and a second
group of control cells and register cells needed for asynchronous design.

The cells used to construct bundled-data datapath logic (combinational logic)
are in the `comb` directory.  The `control` directory contains the remaining
cells. 

**NOTE:** we are still working on these cells and they are not yet
ready to use.

Thanks to the students from Yale's EENG 426 (Silicon Compilation) class
from Fall 2021 for contributing these cells to the community!

## generate rect and mag files for new cells

create act that instanciates all the cells you want,
```
interact -Tsky130l

interact> act:read <file with instances>.act
interact> act:expand
interact> act:top <name of defproc containing instances>
interact> ckt:cell-map 
interact> ckt:map
interact> load-scm "phydb.scm"
interact> phydb:create 2.0 1.0 "output2.lef"
interact> act:layout:rect
```
now magic, first generate the tech file for magic, than convert the rect to a drawing script and source it in magic
```
techgen -Tsky130l > sky130l.tech
mag.pl <filename>.rect > <filename>.tcl
magic -Tsky130l
magic> source <filename>.tcl
```