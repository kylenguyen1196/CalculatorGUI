# CalculatorGUI
from tkinter import *

class Calculator:
    def __init__(self):
        window = Tk()
        window.title("Calculator")
#frame1
        frame1 = Frame(window)
        frame1.pack()
        self.results = Label(frame1, text = "100")
        self.results.pack()
#frame2
        frame2 = Frame(window)
        frame2.pack()
        self.v1 = DoubleVar()
#buttons
        btClear = Button(frame2, text = "Clear", fg = "red", width = 5,
                    command = self.delButton)
        btSign = Button(frame2, text = "+/-", fg = "red", width = 5,
                    command = self.processButton)
        btPercent = Button(frame2, text = "%", fg = "red", width = 5,
                    command = self.processButton)
        btDivide = Button(frame2, text = "/", fg = "orange", width = 5,
                    command = self.processButton)
        btMultiply = Button(frame2, text = "X", fg = "orange", width = 5,
                    command = self.processButton)
        btSubtract = Button(frame2, text = "-", fg = "orange", width = 5,
                    command = self.processButton)
        btAdd = Button(frame2, text = "+", fg = "orange", width = 5,
                    command = self.processButton)
        btEqual = Button(frame2, text = "=", fg = "orange", width = 5,
                    command = self.processButton)
        btDecimal = Button(frame2, text = ".", width = 5,
                           command = self.processButton)  
        btOne = Button(frame2, text = "1", width = 5,
                       command = self.processButton)
        btTwo = Button(frame2, text = "2", width = 5,
                       command = self.processButton)
        btThree = Button(frame2, text = "3", width = 5,
                         command = self.processButton)
        btFour = Button(frame2, text = "4", width = 5,
                        command = self.processButton)
        btFive = Button(frame2, text = "5", width = 5,
                        command = self.processButton)
        btSix = Button(frame2, text = "6", width = 5,
                       command = self.processButton)
        btSeven = Button(frame2, text = "7", width = 5,
                         command = self.processButton)
        btEight = Button(frame2, text = "8", width = 5,
                         command = self.processButton)
        btNine = Button(frame2, text = "9", width = 5,
                        command = self.processButton)
        btZero = Button(frame2, text = "0", width = 5,
                        command = self.processButton)
#buttonConfiguration        
        btClear.grid(row = 1, column = 1)
        btSign.grid(row = 1, column = 2)
        btPercent.grid(row = 1, column = 3)
        btDivide.grid(row = 1, column = 4)
        btMultiply.grid(row = 2, column = 4)
        btSubtract.grid(row = 3, column = 4)
        btAdd.grid(row = 4, column = 4)
        btEqual.grid(row = 5, column = 4)
        btDecimal.grid(row = 5, column = 3)
        btOne.grid(row = 2, column = 1)
        btTwo.grid(row = 2, column = 2)
        btThree.grid(row = 2, column = 3)
        btFour.grid(row = 3, column = 1)
        btFive.grid(row = 3, column = 2)
        btSix.grid(row = 3, column = 3)
        btSeven.grid(row = 4, column = 1)
        btEight.grid(row = 4, column = 2)
        btNine.grid(row = 4, column = 3)
        btZero.grid(row = 5, column = 2)        
        window.mainloop()

#buttonCommands
    def processButton(self):
        pass
    def delButton(self):
        self.results["text"] = "0"

Calculator()

