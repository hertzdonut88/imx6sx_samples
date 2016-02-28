# Sample application to process VADC output via PXP and output to framebuffer.

Currently we assume output display supports 32 bbp (udoo neo hdmi), you will 
need to modify the code to support an LCD with 18/24 bbp. 

We don't employ GPU to output to the framebuffer therefore the capture rate 
may be limited and cpu usage high.

To build this sample you require pxp header/libraries, these are built as part 
of the imx-lib libraries. [See the bsp for more information.](http://git.freescale.com/git/cgit.cgi/imx/meta-fsl-bsp-release.git/tree/imx/meta-bsp/recipes-bsp/imx-lib?h=fido_3.14.52_1.1.0_ga)

## To build:

make clean
make

## To run:

./imx6sx_vdac_pxp

Options parameters

\-t Time in seconds to run
\-h flip image horizontally
\-v flip image vertically
\-i invert colors
