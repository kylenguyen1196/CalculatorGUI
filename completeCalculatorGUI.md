# CalculatorGUI
#Calculator GUI using tkinter

from tkinter import *

#class calculator

class Calculator:
    def __init__(self):

#creating window
        
        window = Tk()
        window.title("Calculator")
        self.equation = StringVar()
        self.expression = ""

#creating frame 1    
        
        frame1 = Frame(window)
        frame1.pack()
        results = Entry(frame1, text = self.equation)
        results.pack()

#creating frame 2
        
        frame2 = Frame(window)
        frame2.pack()

#creating all buttons for calculator
        
        btClear = Button(frame2, text = "Clear", fg = "red", width = 5,
                    command = self.delButton)
        btDivide = Button(frame2, text = "/", fg = "orange", width = 5,
                    command = lambda: self.processButton("/"))
        btMultiply = Button(frame2, text = "X", fg = "orange", width = 5,
                    command = lambda: self.processButton("*"))
        btSubtract = Button(frame2, text = "-", fg = "orange", width = 5,
                    command = lambda: self.processButton("-"))
        btAdd = Button(frame2, text = "+", fg = "orange", width = 5,
                    command = lambda: self.processButton("+"))
        btEqual = Button(frame2, text = "=", fg = "orange", width = 5,
                    command = self.equalButton)
        btDecimal = Button(frame2, text = ".", width = 5,
                           command = lambda: self.processButton(".")
        btOne = Button(frame2, text = "1", width = 5,
                       command = lambda: self.processButton(1))
        btTwo = Button(frame2, text = "2", width = 5,
                       command = lambda: self.processButton(2))
        btThree = Button(frame2, text = "3", width = 5,
                         command = lambda: self.processButton(3))
        btFour = Button(frame2, text = "4", width = 5,
                        command = lambda: self.processButton(4))
        btFive = Button(frame2, text = "5", width = 5,
                        command = lambda: self.processButton(5))
        btSix = Button(frame2, text = "6", width = 5,
                       command = lambda: self.processButton(6))
        btSeven = Button(frame2, text = "7", width = 5,
                         command = lambda: self.processButton(7))
        btEight = Button(frame2, text = "8", width = 5,
                         command = lambda: self.processButton(8))
        btNine = Button(frame2, text = "9", width = 5,
                        command = lambda: self.processButton(9))
        btZero = Button(frame2, text = "0", width = 5,
                        command = lambda: self.processButton(0))

        
        btClear.grid(row = 5, column = 1)
        btDivide.grid(row = 1, column = 1)
        btMultiply.grid(row = 1, column = 2)
        btSubtract.grid(row = 1, column = 3)
        btAdd.grid(row = 1, column = 4)
        btEqual.grid(row = 5,column = 4)
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

#processes for buttons      
    
    def processButton(self,num):
        self.expression += str(num)
        self.equation.set(self.expression)

    def delButton(self):
        self.expression = ""
        self.equation.set("")

    def equalButton(self):
        try:
            total = str(eval(self.expression))
            self.equation.set(total)
            self.expression = ""

        except:
            self.equation.set("Err")
            self.expression = ""
    
Calculator()
