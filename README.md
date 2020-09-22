# 2020F_EE_552_WS_assignment3
Understanding JDK, JRE, JVM

Collaborators: Leonel Joseph, Jeffrey Monsalve
 

1. What are JDK, JRE and JVM? It should be in your own words and not more than two unambiguous sentences for each.

   JDK, which stands for Java Development Kit, It is a package used to develop Java applications and convert Java code to Byte Codes. The conversion is usually done by using Java compilers.

   JRE, which is Java Runtime Environment, is used to execute Java applications. It converts the java byte code to the necessary native code based on the underlying platform. For each platform, there is a JRE version for example: Linux, Windows, Unix and so on.

   JVM, which stands for Java Virtual Machine, It is the heart of Java technology. It's an abstract computer that loads class files using class loader, executes the class file using the execution engine.


2. What is the relation between the three (JDK, JRE, JVM)? How is Java code executed in a Java program. Explain by assuming that the program was written on one platform (e.g., Windows) and executed on another (e.g., Linux). Small paragraph of 6-9 sentences.
  
   There is a close relationship between JDK, JRE, and JVM. The JDK provides the environment to develop and execute the Java program. The JRE, which is included in the Java Development Kit, allows to run the Java program. In addition, the Java Virtual Machine known as the interpreter, plays an important role in both JDK and JRE, since it is incorporated in the development kit. When using either JDK or JRE to execute a java program, the JVM is the one that executes the program line by line. A Java program compiled in Windows for example "HelloWorld.java" is transformed in Bytecode format when "Javac" is called, the "Java" command executed the class. The class loader searches the class form class path and loads the Bytecode(OS Independent), and the JVM calls the native method invocation for the host operating system.

      

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

    To be able to execute the source code of HelloWorldApp application, JDK is needed   in that case to compile it, to get the class file. Once the HelloWorldApp is converted into class file and the Bytecodes, JRE can be used to execute the program. Lastly, If the program HelloWorldApp is written in Windows, with the Bytecode, there is no need to write another application, we can use execute the HelloWorldApp Bytecode file on Linux by using the JVM. 

    
4. Modify the document at least twice each person to make it better and show your competency to do version control using github.


Question: How Java is Portable?(Trivial Question Proposition?)

Question: How does the program data change when a program is handed from JDK to JRE to JVM? (Sample)