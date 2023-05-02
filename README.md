Download Link: https://assignmentchef.com/product/solved-cop3502-lab-05-the-cow-says
<br>
<h1>Overview</h1>

This lab is designed to introduce students to the Bash Command Line Interface (CLI) and the concept of CLI arguments and give them practice writing classes. For (only) this lab, you are not allowed to use any windowed editor (such as IntelliJ, Eclipse, or Notepad++). Instead, you will use a Unix-based command line editor.




The cowsay utility is a popular Unix program from the 20<sup>th</sup> century (see <u>https://en.wikipedia.org/wiki/Cowsay</u>). You will write a slightly simplified cowsay program that takes in several arguments and prints out different text depending on the arguments. You must log in to the school computers using your CISE account to do this lab.




<h1>Tools</h1>

Please note that tou must use a text editor and the terminal to edit and run your program and its directories. It is advised students learn/review basic Unix shell commands before beginning; a good run-through can be found here: <u>https://linuxjourney.com/lesson/the-shell</u>.




Follow these steps to get started on the lab:




<ul>

 <li>Open a terminal and enter the pwd command to identify the <u>p</u>ath to the <u>w</u>orking (current) <u>d</u>irectory (folder)</li>

 <li>Enter ls to <u>lis</u>t the contents of the current directory</li>

 <li>Use the mkdir command to <u>m</u>a<u>k</u>e a new <u>dir</u>ectory called Lab05.</li>

 <li>Use ls to see the change, then cd to <u>c</u>hange to the <u>d</u>irectory Lab05</li>

 <li>Do your lab work in that folder. Use your googlefu skills to find more commands</li>

</ul>




Recommended text editors include nano and joe. (If you hate yourself, you can use vi or emacs too.) You’ll also need to use the javac program for <u>Java c</u>ompilation and the java command to run <u>Java</u> programs.




You can guide more information about some of these commands here:

<u>https://www.howtogeek.com/howto/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/</u> <u>https://introcs.cs.princeton.edu/java/15inout/linux-cmd.html</u>




<h2>History of Command Line Names (Just for Fun)</h2>

In case you are wondering: nano is a free-software version of a program called pico, which is the stand-alone editor for <u>Pi</u>ne at the <u>co</u>mmand line. The pine email program was an alternative version of Elm – you see, <u>P</u>ine <u>I</u>s <u>N</u>ot <u>E</u>lm. The elm program was an earlier <u>e</u>mai<u>l m</u>anager. (If you think my jokes are bad, you cannot fathom the depths of terrible humor present in computer science and engineering! This is but the beginning of a terrible humor journey.)

<h1>Specification</h1>

Students will construct two classes: a driver class with a main() entry point (Cowsay) and a data class (Cow). Note that HeiferGenerator.java is provided for you; you code must use this class to create the cow objects. <u>All</u> <u>attributes / methods must be private unless noted in the specification!</u>

<h2>Provided For Students – HeiferGenerator</h2>




public static Cow[] getCows()

Returns an array of cow objects from the built-in data set. This will call the Cow constructor and setImage() methods of the cow class to properly initialize new cow objects uniquely for each data set.




<h2>Cowsay Class (Program Driver)</h2>

Your program must accept <u>command line arguments</u>. Command line arguments are captured as part of the String[] variable passed into the main() method of the driver class. (Review lecture slides for examples!)




The command line arguments that must be supported are as follows:




java cowsay -l                                Lists the available cows

java cowsay MESSAGE Prints out the MESSAGE using the default COW java cowsay -n COW MESSAGE Prints out the MESSAGE using the specified COW




If a user calls for a cow that does not exist, the program should print out “Could not find [COWNAME] cow!”




<u>Output Samples</u>

<table width="694">

 <tbody>

  <tr>

   <td rowspan="2" width="180">


    <table width="179">

     <tbody>

      <tr>

       <td width="179">&gt;java Cowsay I am a potato! I am a potato!\^__^(oo)_______(__)       )/||—-w |||     ||</td>

      </tr>

     </tbody>

    </table></td>

   <td rowspan="2" width="313">


    <table width="309">

     <tbody>

      <tr>

       <td width="309">&gt;java Cowsay -n kitteh I am a pritteh. I am a pritteh.\(“`-‘  ‘-/”) .___..–‘ ‘ “`-._` *_ *  )    `-.   (      ) .`-.__. `)(_Y_.) ‘ ._   )   `._` ;  “ -. .-‘_.. `–‘_..-_/   /–‘ _ .’ ,4( i l ),-”  ( l i),’  ( ( ! .-‘</td>

      </tr>

     </tbody>

    </table></td>

   <td width="201">


    <table width="199">

     <tbody>

      <tr>

       <td width="199">&gt;java Cowsay -lCows available: heifer kitteh</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

  <tr>

   <td width="201">


    <table width="199">

     <tbody>

      <tr>

       <td width="199">&gt;java Cowsay -n ninja WUT Could not find ninja cow! </td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>




<u>Suggested Methods</u>

The following methods are suggested to make development easier, but are not required:




private static void listCows(Cow[] cows)

Displays the list of available cows from an array of Cow objects.




private static Cow findCow(String name, Cow[] cows)

Given a name and an array of Cow objects, return the Cow object with the specified name.




<h2>Cow Class</h2>

The Cow class facilitates the creation and use of cow objects by providing the following methods (which students must implement):




public Cow(String name)

This method should be the only constructor for this class. <u>There should not be a default constructor!</u>




public String getName() Returns the name of the cow




public String getImage()

Returns the image used to display the cow (after the message)




public void setImage(String name)

Sets the image used to display the cow (after the message)

<h1>Testing</h1>

Run the L05_test.sh script provided. To run it, place it in the same folder as the rest of your files and make it executable via chmod +x L05_test.sh. Then run it: ./ L05_test.sh. This script contains a series of commands to run Cowsay in various ways, streaming the results into the text file Output.txt. It then uses less command to view the output. Your output file should match the sample output in this document.




<h1>Submissions</h1>

NOTE: Your output must match the example output *exactly*. If it does not, you will not receive full credit for your submission!




Files:               Cowsay.java, Cow.java, HeiferGenerator.java

Method: Submit on ZyLabs

<h1>Sample Output</h1>




&gt;javac Cowsay.java

&gt;java Cowsay Hello World!




Hello World!







^__^

(oo)_______

(__)       )/

||—-w |

||     ||




&gt;java Cowsay -n kitteh Hello World!




Hello World!







(“`-‘  ‘-/”) .___..–‘ ‘ “`-._

` *_ *  )    `-.   (      ) .`-.__. `)

(_Y_.) ‘ ._   )   `._` ;  “ -. .-‘

_.. `–‘_..-_/   /–‘ _ .’ ,4

( i l ),-”  ( l i),’  ( ( ! .-‘




&gt;java Cowsay -l

Cows available: heifer kitteh




&gt;java Cowsay -n ninja Hello world!

Could not find ninja cow!




&gt;java Cowsay Hello -n kitteh




Hello -n kitteh







^__^

(oo)_______

(__)       )/

||—-w |

||     ||