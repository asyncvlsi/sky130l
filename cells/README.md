# Skywater 130nm gridded cells for ACT flow

This directory contains gridded cells for use with the Skywater 130nm process
and the ACT tools---in particular, bundled-data circuits generated using 
`chp2prs`. There are two groups of cells: explicitly instantiated cells
from logic synthesis that use the ACT standard cell library, and a second
group of control cells and register cells needed for asynchronous design.

The cells used to construct bundled-data datapath logic (combinational logic)
are in the `comb` directory.  The `control` directory contains the remaining
cells. 

**NOTE** we are still working on these cells and they are not final.

Thanks to the students from Yale's EENG 426 (Silicon Compilation) class
from Fall 2021 for contributing these cells to the community!
