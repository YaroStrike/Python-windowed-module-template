# Python-windowed-module-template
that's how my tkinter apps looks like 💩
----------------------------------------
```python
# Import what we need from the tkinter library...
import tkinter as tk
from tkinter import *
from tkinter import ttk
from tkinter import font

# This is a function (main thing for programming math code as example) for manipulation and getting a result based on input windows! 
def calc(): 
    input1 = float(e1.get())
    input2 = float(e2.get())
    result = round(input1 + input2, 2) # I just wanna see the rounded to hundredth sum of these floats as result.
    output_label.config(text=f"Result: {result}")

# Module's window settings (science of geometry is resolution for now, yea):
root = tk.Tk()
root.title("variant2")
root.geometry("600x100")

# Edit input labels' meaning:
label1 = tk.Label(root, text="Well, firstly: ").grid(row=0)
label2 = tk.Label(root, text="and secondly: ").grid(row=1)

# Declaring input windows' text as text with custom position:
text1 = tk.StringVar()
text2 = tk.StringVar()

# Customizing font for some text (I tried... but this looks like just bold):
semibold = font.Font(family="Arial", size=11, weight="bold", slant="roman", underline=False, overstrike=False)

# Text settings (windows' input for me)
e1 = tk.Entry(root, textvariable=text1, font=semibold)
e1.grid(row=0, column=1)
e2 = tk.Entry(root, textvariable=text2, font=semibold)
e2.grid(row=1, column=1)

# Button settings (result output button for me)
calc_button = tk.Button(root, text="Find out", command=calc) 
calc_button.grid(row=2, column=1)

# Output label settings that is stand instead of print() in our def calc()
output_label = tk.Label(root, text="")
output_label.grid(row=3, column=1)

# I don't give a sht what it does, but it usually written at the end.
root.mainloop()
```
