## CX on Windows 10

## Installation

Download the latest version of cx.exe from https://github.com/skycoin/cx/releases

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/1.jpg"         width="400">

unzip in the destination you want to have your CX-files

 
*For example, D:\Programme\CX*

  <img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/2.jpg"         width="200">

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/3.jpg" width="400">

To have access to the cx.exe in the terminal set Global Variable

Either search in Windows-Search-Bar or press **WIN + R** and type in\
**C:\Windows\System32\systempropertiesadvanced.exe** and press **Enter**

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/4.jpg" width="400">

Go to **Environment Variables**

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/5.jpg" width="400">

Select **Path** and **Edit**

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/6.jpg" width="400">

Press **New** and type in the Path you put in the cx.exe\ 
*For example, D:\Programme\CX*

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/7.jpg" width="400">

Now Press **WIN + R**, type in **cmd.exe** and press **Enter** to open terminal

Then type in **cx -v**, press **Enter** and you should get back the version

## Hello World!

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/8.jpg" width="400">

Make new folder **‘examples’** 

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/9.jpg" width="400">

Create new file **’hello-world.cx’** in folder **‘examples’**

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/10.jpg" width="400">

Type in the words:

*package main\
\
func main() {\
str.print("Hello World!")\
}*

Save (**Ctrl + S**) and close

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/11.jpg" width="400">


Now open terminal again, move to the direction where the **hello-world.cx** is or

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/12.jpg" width="400">

type in cx then press Space and drag & drop the file you want to run and press Enter
