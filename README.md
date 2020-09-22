# 2020F_EE_552_WS_assignment3
Understanding JDK, JRE, JVM

Collaborators: Leonel Joseph, Jeffrey Monsalve
 

1. What are JDK, JRE and JVM? It should be in your own words and not more than two unambiguous sentences for each.

   JDK, which stands for Java Development Kit, is a package used to develop Java applications and convert Java code to Byte Codes through the java compiler commonly invoked via the command line using `javac Filename.java`. The JDK also includes the debugger, it is platform dependent and can be installed in Linux, Microsoft, and Macos. 

   
   JRE is the Java Runtime Environment and it is used to execute Java applications. It contains class libraries, JVM, and other supporting files, important packages included are math, swingetc, util,lang, awt, and runtime libraries. 

    JVM stands for Java Virtual Machine and it is the heart of the Java Technology. It's an abstract computer, that allows for an platform independent way of executing Java source, it contains the Just In Time compiler that is enabled by default via an environment variable that allows Java bytecode to be further compiled to low-level machine language.


2. What is the relation between the three (JDK, JRE, JVM)? How is Java code executed in a Java program. Explain by assuming that the program was written on one platform (e.g., Windows) and executed on another (e.g., Linux). Small paragraph of 6-9 sentences.
    
    There is a close relationship between JDK, JRE, and JVM. The JDK provides the environment to develop and execute the Java program. The JDK allows developers to create Java programs that can be executed and ran by the JRE and JVM, through the Java Compiler and Java Debugger. The JRE which is included in the Java Development Kit, allows developers to run their Java programs it provides the environment to execute source code. The JVM (Java Virtual Machine) is know as the interpreter, plays an important role in both JDK and JRE, it is included in the development kit. When executing a Java Program in bytecodes, it executes the program line by line converting it into the respective machine-specific code(linux, windows, etc). JVM also allows you to customize the memory allocation for a program. A Java program compiled in Windows for example "HelloWorld.java" is transformed in Bytecodes format when the cli tool javac bundled by the JDK is called pointing to the absolute path of the source code file. The java command executes the class included in the bytecode file. The class loader searches the class from the class path and loads the Bytecode(OS Independent), and then the JVM calls the native method invocation for the host operating system.
  
      

3. With the help of the code for Hello World program in Java (you can copy code with citation), explain when this program needs JDK (and not JRE and JVM), JRE (and not JVM) and JVM.

     **
    * The HelloWorldApp class implements an application that
    * simply prints "Hello World!" to standard output.
    */
    class HelloWorldApp {

    public static void main(String[] args) {

    System.out.println("Hello World!"); // Display the string.
        }
     }

    To be able to execute the source code of HelloWorldApp application, JDK is needed in that case to compile it, to get the class file. This can be achieved by using the following command in your terminal `javac HelloWorldApp.java`. Once the HelloWorldApp is converted into class file and Bytecodes, the JRE can be used to excute the program. Lastly, if the program HelloWorldApp is written in Windows, with the Bytecode, there is no need to write another application, we can execte the HelloWorldApp Bytecode file on Linux through the JVM. 


Question: How does the JVM infer how to convert bytecodes into low-level machine language allowing bytecodes to be portable across different operating systems? 
