# supermarketproject
 Excited to share my latest mini-project: Supermarket Bill Generation System!  I've created a simple Python program that generates bills amount based on the items purchased and their prices, app 💳✨ Key features: 📝 Inputting items and their prices 🔢 Quantity tracking 💸 Discount calculations 📄 Detailed bill generation
 import datetime as ds
print()
print(25*"*","welcome to our store","*"*25)
items='''
rice    Rs.20/kg
sugar   Rs.30/kg
egg     Rs.7/each
maggi   Rs.5/each
boost   Rs.5/each
wheat   Rs.40/kg
paneer  Rs.80/kg
'''
plist=[]
qlist=[]
pricelist=[]
ilist=[]
price=0
total_amount=0
final_amount=0
items_list={
    'rice':20,
    'sugar':30,
    'egg':7,
    'maggi':5,
    'boost':5,
    'wheat':40,
    'paneer':80
}
name=input("Enter your name:")
option=int(input("if you want to see the List,click 1:"))
while True:
    if option==1:
        print(items)
        inp=input("Did you want to buy:")
        if inp=='yes':
            inp2=input("enter the Item:")
            if inp2 in items_list:
                qauntity=int(input("enter the qauntity:"))
                price=qauntity*(items_list[inp2])
                pricelist.append((inp2,qauntity,price,items_list))
                plist.append(price)
                qlist.append(qauntity)
                ilist.append(inp2)
                total_amount+=price
                gst=(total_amount*5)/100
                final_amount=gst+total_amount
            else:
                print("Entered Item is not AVailable/Out of Stock")
        else:
            print("OK Did want to bill:")
            bill=input()
            if bill=='yes':
                pass
                if final_amount!=0:
                    print(25*"*","PAVAN'S SUPER MARKET","*"*25)
                    print(25*"*","MADANAPALLI","*"*25)
                    print(30*"-","BILL","-"*30)
                    print("Name:",name,30*" ","DATE&TIME:",ds.datetime.now())
                    print("S.NO", 10 * " ", "ITEMS", 10 * " ", "QUANTITY", 10 * " ", "Price", 10* " ")
                    for i in range(len(pricelist)):
                        print(i, 15 * " ", ilist[i], 15 * " ", qlist[i], 15 * " ", plist[i])
                    print(75*"-")
                    print(50*" ","TOTAL_AMOUNT:","RS.",total_amount)
                    print(50*" ","GST:","RS.",gst)
                    print(75*"-")
                    print(50*" ","FINAL_AMOUNT:","RS.",final_amount)
                    print(75*"-")
            break
print(10*"😂","THANKS FOR VISITING","💕"*10)
            
                
