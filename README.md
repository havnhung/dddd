from tkinter import *
def NewFile() :
    print("New File !")
def About() :
    print("This is a simple example of a menu")
def OpenFile() :
    print("Open File !")
def InsText() :
    print("Insert Text !")
def InsPic() :
    print("Insert Picture !")

root = Tk()
menu = Menu(root)
root.config(menu=menu)

filemenu = Menu(menu)
menu.add_cascade(label="File", menu=filemenu)
filemenu.add_command(label="New", command=NewFile)
filemenu.add_command(label="Open", command=OpenFile)
filemenu.add_command(label="Exit", command=root.quit)

insertmenu = Menu(menu)
menu.add_cascade(label="Insert", menu=insertmenu)
insertmenu.add_command(label="Text", command=InsText)
insertmenu.add_command(label="Picture", command=InsPic)

helpmenu = Menu(menu)
menu.add_cascade(label="Help", menu=helpmenu)
helpmenu.add_command(label="About...",  command=About)

mainloop()
