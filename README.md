                           SerialPortLib User Guide
    This lib is made base on the Google android-serialport-api project. I only simplify its implementation by comprising those core codes into a .jar so that anybody can just dump the .jar into the libs dir and uses it without going through any transplanting troubles.
　　Building Up Environment
　　Step.1
　　Add sourceSets .main{jniLibs.srcDirs = ['libs']} into your app¨s build.gradle. 
　　
　　Step.2
　　Dump all the files into your libs.
　　
　　Step.3
　　Rebuild the project,and the .jar is supposed to be working fine.
　　How to Use the Classes
　　To add to the flexibility of its utility, I cease to formulate its usage by avoiding integrating it with any activities or applications. The user need to understand the SerialPort class and SerialPortFinder class in order to use them properly. 
　　Use SerialPortFinder class to enumerate available serial ports:
    
    
    The serial ports you get are mere options that you may try to achieve serial port communication but not a guarantee. You must make sure the one you pick is permission-authorized and is correctly connected. When you are sure:
　　Use SerialPort class to open certain serial port. 
    
   The input params are defined as followed:

   Know that: The path of the serial port can be either obtained via SerialPortFinder or your device manual.
   When you open your serial port successfully, get its I/O Streams via the following methods:
    
    Then use the IO Streams to do whatever you intend to do.
　　And finally but not last, remember to close your serial port when it¨s no longer needed. For if you don¨t, your app will keep occupying the serial port, and may preventing other programs from using it.
　　
    I must emphasize that I¨m, too, the beneficiary of Google¨s android-serialport-api project. This .jar could not be made if not for our programmers¨ selfless contribution. And if you feel that this .jar could be improved in any other way and are willing to share it with me, you are welcome to contact me via leoliao2008@163.com. 
