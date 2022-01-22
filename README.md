# M1-StarNet-PI
Install StarNet module in PixInsight on M1 MacOS

The StarNet process is needed to run most of darkarchon's EZ scripts in PixInsight, but it won't run on M1 Macs because the required tensorflow libraries are not compatible with the M1 architecture (even in Rosetta-2 emulation)

The script here replaces the StarNet module and tensorflow libraries with versions derived from the stand-alone StarNet++ program originally developed by nekitmm (https://sourceforge.net/projects/starnet/) 

Thanks to pfile (Rob) for figuring out how to do this. 

The files come with no warranty whatsoever. Use them at your own risk! 

HOW TO UPDATE YOUR PIXINSIGHT TO USE StarNet ON YOUR M1 MAC:

1. DOWNLOAD AND UNCOMPRESS THE FILE FROM DROPBOX

2. cd into the resulting folder by typing
cd M1-StarNet-PI

3. run the script by typing
./update.PI-StarNet.sh

4. Restart PixInsight. Open an image. Try Process -> Object Recognition -> StarNet. 

5. Some users also have to open "Install Modules..." and run a search.

6. If you get an error, click the "wrench" icon on the StarNet panel and make sure the starnet_weights files are correctly identified (in /Applications/PixInsight/lib)

7. Once it works, delete both the compressed and uncompressed folders named M1-StarNet-PI to free up disk space.

THAT'S IT!
