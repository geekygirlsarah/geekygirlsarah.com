---
title: How to Install Eclipse (for C++) in Windows
date: 2012-10-16T13:52:43+00:00
permalink: /2012/10/16/how-to-install-eclipse-for-c-in-windows/
# canonical_url: "https://yoursite.com/custom-canonical-url"
categories:
  - Software
  - Tutorials
  - Uncategorized
tags:
  - C++
  - Eclipse
  - MinGW
  - Windows
---

This post was originally from the blog site Binary Girls that my friends Abbey, Sarah, and I started. I’m saving it here for archival reasons.
{: .notice--info}

<img class="alignright wp-image-282 size-full" src="/assets/images/eclipse_pos_logo_fc_med2-150x150.jpg" alt="Eclipse logo" width="150" height="150" /> If you&#8217;ve used Eclipse, you know it&#8217;s Java-based. And it&#8217;s easy to get it running in Windows to compile Java programs. But what about C++? If you&#8217;ve downloaded the CDT (C/C++ Development Tooling), you may see that it lets you write C++ programs, but they don&#8217;t compile and the #includes act all confused. Of course there are directions online, but they&#8217;re all out of date.

Binary Girls to the rescue!

**But Why Not Download Eclipse with CDT?**

The CDT is only a plugin that lets you write C/C++ programs, but it doesn&#8217;t include the compiler or the includes needed. So if you want your program to work, you&#8217;ll need more than just that.

**Part I: Install Eclipse** (for Java)  
Latest version as of writing: <a href="http://www.eclipse.org/downloads/packages/eclipse-classic-421/junosr1" target="_blank" rel="noopener"><u><span style="color: #0066cc;">http://www.eclipse.org/downloads/packages/eclipse-classic-421/junosr1</span></u></a>

  1. Download Eclipse. I recommend Eclipse Classic. Grab either the 32-bit or 64-bit version depending on which your system is.
  2. Extract the eclipse folder to your Desktop.
  3. Move the folder to your Program Files. In Vista/Win7/Win8 you will have to give it administrative privileges. If can also leave it in a folder on your Desktop or My Documents, but other users won&#8217;t be able to use it.

**Part II: Install MinGW** (for C/C++ compilers)  
Latest version as of writing: <a href="http://sourceforge.net/projects/mingw/files/latest/download?source=files" target="_blank" rel="noopener"><u><span style="color: #0066cc;">http://sourceforge.net/projects/mingw/files/latest/download?source=files</span></u></a>

MinGW is the Minimalist GNU for Windows. Basically it contains the compiler you need. (You can use the Visual Studio compiler, but that&#8217;s a pain to set up and this is easier.) As of this writing, version 20120426 was the latest, but you can grab something newer.

  1. Download MinGW&#8217;s installer and run it
  2. It will ask if you want to use the pre-packaged repository catalogs or download the latest ones. That&#8217;s up to you.
  3. If you agree to the GPL license, continue.
  4. By default it wants to install to C:\MinGW. I would leave it here as it will save you some troubles later.
  5. It will want to create some Start menu shortcuts in MinGW. Change it if you like.
  6. Here you can select the components you want to install. By minimum, you need the **C++ compiler**, and **MSYS Basic System.** If you want more languages, select those. If you want some more tools, feel free to select the MinGW Developer Toolkit as well.
  7. Start the install. If you requested the latest catalogs online, it will download those before installing. Either way, grab a cup of coffee/tea/Dr Pepper, it may take a few minutes.
  8. It&#8217;s done! Close the installer.
  9. Go to your System control panel applet (or right-click on My Computer, then click on Properties. Or press Windows Logo+Pause.)  
    Windows XP: Click on the Advanced tab, then on Environment Variables.  
    Windows 7/8: Click on the Advanced system settings link on the left side, then Environment Variables&#8230;
 10. Under System Variables, one called PATH should be listed. Click on it and click on Edit.
 11. Somewhere in the Variable Value box, you need to add in the install directories for MinGW and MSYS at the beginning of the string.  
    So, if you installed MinGW in C:\MinGW, then add:</p> 
    <pre>C:\MinGW\bin;C:\MinGW\msys\1.0\bin;</pre>

 12. Click OK, then OK, then close the control panel applet.  (Windows XP only: You should probably restart and come back.)
 13. Test it out! Open a command prompt (WinXP: It&#8217;s under Accessories in the start menu. Win7/Win8: Just click start and type in &#8220;cmd&#8221; and enter.) You should be able to type: 
    <pre>gcc --version</pre>
    
    and get a response. You should be able to also type:
    
    <pre>make --version</pre>
    
    and get another response. If you&#8217;re getting errors saying it can&#8217;t find the program, then either you didn&#8217;t install it right, or you didn&#8217;t add the right paths to the PATH variable.</li> 
    
      * Close the command prompt. Congratulations, you&#8217;re done!</ol> 
    
    **Part III: Install Eclipse&#8217;s CDT** (for C/C++ support in Eclipse)  
    Eclipse repository: <a href="http://download.eclipse.org/eclipse/updates/4.2/" target="_blank" rel="noopener"><u><span style="color: #0066cc;">http://download.eclipse.org/eclipse/updates/4.2/</span></u></a>  
    CDT: <a href="http://download.eclipse.org/tools/cdt/releases/juno" target="_blank" rel="noopener"><u><span style="color: #0066cc;">http://download.eclipse.org/tools/cdt/releases/juno</span></u></a>
    
    So Eclipse is installed, and so is MinGW. You&#8217;re practically done. This is one of the easiest steps.
    
      1. Open Eclipse, then click on the Help menu, then on Install New Software.
      2. Click on the Add button. For Name, put in &#8220;Eclipse CDT Repository&#8221; and for location, put in http://download.eclipse.org/tools/cdt/releases/juno then click on OK
      3. It should list CDT Main Features and CDT Optional Features. Click the arrow next to the CDT Main Features.
      4. Check the box next to C/C++ Development Tools. You can click on more options, but this is the minimum. Then click on Next.
      5. It should list several things it&#8217;s going to install. You want all of those.  So click on Next.
      6. If you agree with the Eclipse Foundation Software User Agreement, then click on the I accept button, then Finish.
      7. It will download the updates, then want to restart Eclipse. Do that.
    
    **Part IV: Testing**
    
    Great, all the steps are complete. Let&#8217;s make sure they all work, though.
    
      1. Eclipse should have restarted. Click on the File menu, then New, then Project.
      2. Choose the arrow next to C/C++, then C++ Project. Click on Next.
      3. Give it a name at the top under Project name (how about HelloWorld), then under Project Type, choose Executable->Empty Project. The toolchain should list MinGW GCC. Then click on Finish.
      4. It may ask you about switching to the C++ perspective. I would allow that.
      5. If it is still up, close the Start page with the X on the top at the top.
      6. Alright, you should see the Project Explorer on the left with your project (HelloWorld). Right-click on that, click New, then on Source File.
      7. Put a filename in the Source file field. _Be sure to include the .cpp extension!_ How about HelloWorld.cpp ?
      8. Double-click on Test on the left side. Then, you can type this in: 
        <pre>#include &lt;iostream&gt;
using namespace std;

int main() {
   cout &lt;&lt; "The Binary Girls say 'Hello world!'";
   return 0;
}</pre>
    
      9. Be sure to save your file, then click on the hammer (&#8220;build&#8221;) icon. That will build the app, and it should build properly.
     10. Click on the green circle with the white play button on it (&#8220;run&#8221;). This will run the program you just built.
     11. If all works right, the console window at the bottom, should show show &#8220;The Binary Girls say &#8216;Hello world!'&#8221;
    
    Ta-da! And that&#8217;s it for this tutorial.
    
     _Did this work for you? Are you having problems? Feel free to leave some comments about the tutorial below._
    
    ~ Sarah