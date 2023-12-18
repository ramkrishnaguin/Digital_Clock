from tkinter import Tk
from tkinter import Label
import time

root = Tk()
root.title("Digital Clock")

def presentTime():
    sysTime=time.strftime("%H:%M:%S")
    lbl.config(text=sysTime)
    lbl.after(1000, presentTime)

lbl=Label(root, font=('Serif',60), bg='white', fg='black')
lbl.pack()

presentTime()
root.mainloop()
