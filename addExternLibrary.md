# my attempt at implementing a universal C++ library for Moun River Studio.

MRS supposedly has a way to add externally linked libraries but so far I have not been successful in getting it to work. (except once accidently)

So I have several options of various complexity.  I am assuming that you have all of my classes in one single directory calld "libraries".

1. <b>Brute force</b> - this works because MRS defaults to looking for header files in the "Peripheral/inc" subdirectory and their associated source files in "Peripheral/src".  So you can just manually copy all of my ".h" files that interest you into "inc" and the corresponding ".cpp" source files into "src".  This can be done from within MRS or externally in the file system, in which case you may want to do a refresh in MRS before yu try a build.<br><br>  
2. <b>use a file system link</b> - this involves creating a symbolic link in your project's directory tree to the a common instance of "libraties", and then telling MRS to look in this subdirectory. I typically put "libraries" under the Peripheral directory mostly because they are all peripheral classes, but you could also put it at a higher level. To make the symbolic link outside of MRS open a terminal session in the Peripheral directory and enter "ln -s PATH_to_libraries.  ie: ln -s /home/moun/mylibraries/libraries.<br>You then need to modify the MRS search path by going to: Project->Properties->C/C++ General->Paths and Symbols->Includes->GNU C++  where you can add the Path to "libraries" ie: /${ProjName}/Peripheral/libraries. Then hit the Apply and Close button. This makes "libraries" common to all projects linking to it.  You can change it's contents in MRS and the change will be reflectd in all projects linking to it.<br><br>
3. I think the accidant I did involved changing the "Source Location" using the "Link Folder..." option - more on this as I investigate further.  Xmas is coming and I need to get the NEOpixels going..

