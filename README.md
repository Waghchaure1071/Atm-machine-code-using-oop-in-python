# Atm-machine-code-using-oop-in-python
#Basically it in an ATM machine operating code which is written in python by using oop concept  .
class atm:
    def __init__(self):
        self.pin=""
        self.balance=0
        self.menu()
        
    def menu(self):
        user_input=input(''' Hello.... How you like to protocall
                           1) Enter 1 to create a pin
                           2) Enter 2 to deposit
                           3) Enter 3 to withdraw
                           4) Enter 4 to cheak balance
                           5) Enter to Exit
            ''')
        
        if user_input =="1":
            self.create_pin()
        elif user_input=="2":
            self.deposit_cash()
        elif user_input=="3":
            self.withdraw_cash()
        elif user_input== "4":
            self.cheak_balance()
        else:
            print(" bye.... Have a good day" )
    def create_pin(self):
        self.pin=input("Enter 4 digit pin for set a pin ")
        print("Pin set successfully")
    def deposit_cash(self):
        temp=input("Enter a pin : ")
        if temp==self.pin:
            amount=int(input("Enter the amount : "))
            self.balance=self.balance + amount
            print("Amount deposit successfully..")
        else:
            print("Invalid pin ")
    def withdraw_cash(self):
        temp=input("Enter a pin : ")
        if temp==self.pin:
            amount=int(input("Enter the amount : "))
            if amount<self.balance:
                self.balance=self.balance - amount
                print("Amount withdraw successfully..")
            else:
                print("Insufficent balance ")
  
        else:
            print("Invalid pin ")
    def cheak_balance(self):
        temp=input(("Enter yout 4 digit pin "))
        if temp== self.pin:
            print(self.balance)
        else:
            print("invalid pin ")

        
        
    
  
    
