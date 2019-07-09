#CX on Windows 10

## Installation

Download latest version of cx.exe from https://github.com/skycoin/cx/releases

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/1.jpg)

unzip in the destination you want to have your CX-files\

*For example, D:\Programme\CX*

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/2.jpg)

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/3.jpg)

To have access to the cx.exe in the terminal set Global Variable\

Either search in Windows-Search-Bar or press **WIN + R** and type in **C:\Windows\System32\systempropertiesadvanced.exe**
and press **Enter**

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/4.jpg)

Go to **Environment Variables**

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/5.jpg)

Select **Path** and **Edit**

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/6.jpg)

Press **New** and type in the Path you put in the cx.exe\ 
*For example, D:\Programme\CX*

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/7.jpg)

Now Press **WIN + R**, type in **cmd.exe** and press **Enter** to open terminal\

Then type in **cx -v**, press **Enter** and you should get back the version


## Hello World!

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/8.jpg)

Make new folder **‘examples’** 

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/9.jpg)

Create new file **’hello-world.cx’** in folder **‘examples’**

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/10.jpg)

Type in the words: \
**package main\
\
func main() {\
str.print("Hello World!")\
}**\

Save (**Ctrl + S**) and close\

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/11.jpg)


Now open terminal again, move to the direction where the **hello-world.cx** is or

![Alt text](https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20windows%20installation/12.jpg)

type in cx then press Space and drag & drop the file you want to run and press Enter
