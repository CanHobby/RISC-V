# RISC-V
Some commrnts and examples on RISC-V MCUs such as the CH32Vxxx family from WCH.

After some early teething problems as documented at the <a href="https://github.com/openwch/ch32v003/issues/16" target="_blank"> openwch github</a> and my <a href="https://hackaday.io/project/191172-using-ch32vxxx-risc-v-and-moun-river" target="_blank">hackaday</a>, I am happy to submit some example code.  I am using the Moun River IDE under Linux (Mint) even though I am no Eclipse expert, so my attempts at sharing projects may seem clumsy.  Any suggestion are more than welcome.

I plan to open separate repositories for each board...  CH32V003, CH32V103, <a href="https://github.com/CanHobby/CH32V203">CH32V203</a>...

### How to add this code to Moun River... (using my "clumsy")...

 - Create a separate directoy in your filesystem to be used as a "workspace" by Moun River.
 - Open Moun River specifyinh this new workspace - do not set to "default workspace".
 - Create a New Moun River project
 - deselect "ARM Core"
 - select the CU family and the variant.
 - go to top of the dialogue and add your project name..
 - click on FINISH
 - ....  here I normally go toe Window->Preferences->Geeral->Appearance  to enable themeing and select dark theme.
     Apply and close...   Yu will need to Close the IDE and Restart it.
   The IDE will have set up a basic template which includes setting up the clock, delay functions and the USART complete with printf.
   Look under >User and you should find "main.c" - this is where things start...
   Right Clicking on "User" should give yo the option add a Directory
   


