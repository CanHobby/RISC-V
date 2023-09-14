# RISC-V MCU examples for CH32Vxxx
How to program RISC-V MCUs such as the CH32Vxxx family from WCH, using 'C' or 'C++'.

After some early teething problems as documented at the <a href="https://github.com/openwch/ch32v003/issues/16" target="_blank"> openwch github</a> and my <a href="https://hackaday.io/project/191172-using-ch32vxxx-risc-v-and-moun-river" target="_blank">hackaday</a>, I am happy to submit some example code.  I am using the Moun River IDE under Linux (Mint) even though I am no Eclipse expert, so my attempts at sharing projects may seem clumsy.  Any suggestion are more than welcome.

I plan to open separate repositories for each board...  CH32V003, CH32V103, <a href="https://github.com/CanHobby/CH32V203">CH32V203</a>...

### How to set up a C++ workspace for Moun River... (using my "clumsy")...

- the individual MCU directories at <a href="https://github/openwch/ch32v20x" target=_blank>openwch github</a> each have a C++ directory which contains a C++ example and instruction PDF.
- the instructions are TOO complicated and, I think, were written for an old version of MRS - better ignored.
- the example has a typo - I have taken the time to fix this and put together a full workspace as an example.
- there are too many files to add to my github repo so I have it all in a ".zip"
To setup a C++ workspace create a new directory to use and unzip "V203C++_template.zip" into this directory.
Open MRS and specify this directory to use as a workspace.
It should be ready to go. My example includes a small example class for those who may not be totally familiar with C++.
- Do NOT change the project name - MRS will not update all of the ".*" files properly.
- I have yet to figure out how to add multiple projects to a workspace - they will clash in the linker.

Go ahead and build the project and upload using F8.


### How to add 'C' code to Moun River... (using my "clumsy")...

 1). Create a separate directoy in your filesystem to be used as a "workspace" by Moun River.
 2). Open Moun River specifying this new workspace - do not set to "default workspace".
     you may wish to set a theme at this point - Window->Preferences->General->Appearance to enable themeing and select dark theme.  If you do change the defualt theme you will need to restart MRS.
 3 Create a New Moun River project - doing things in this order..
 - deselect "ARM Core"
 - select the MCU family and the variant.
 - go to top of the dialogue and add your project name..
 - click on FINISH

   The IDE will have set up a basic template which includes setting up the clock, delay functions and USART complete with printf.
   Look under >User and you should find "main.c" - this is where things start...  you will probably want to replace this "main/c" with the one from my examples..
   
   Right Clicking on "User" should give yo the option add a Directory  ......  TBCont'd

   ### How to use freeRTOS in Moun River... (no "clumsy")...
   1).  see my <a href="https://github.com/CanHobby/freeRTOS">freeRTOS</a> repo. -- real easy..
   
   


