while True:
    print("Select operation.")
    print("1.Add      : + ")
    print("2.Subtract : - ")
    print("3.Multiply : * ")
    print("4.Divide   : / ")
    print("5.Power    : ^ ")
    print("6.Remainder: % ")
    print("7.Terminate: # ")
    print("8.Reset    : $ ")
  

    choice = input("Enter choice(+,-,*,/,^,%,#,$):- ")
    print(choice)
   
    if choice== '+' or choice=='-' or choice=='*' or choice=='/' or choice=='^' or choice=='%':
            pass
    elif choice == '$':
            continue
    elif choice == '#':
            print('Done. Terminating')
            exit()
    else:
        print('Something Went Wrong')
        continue

    x = input('Enter first number: ')
    if ('$' in str(x)):
        continue
    elif ('#' in str(x)):
        exit()
    else:
        a = float(x)

    y = input('Enter second number: ')
    if('$' in str(y)):
        continue
    elif ('#' in str(y)):
        
        exit()
    else:
        b = float(y)

    
    def select_op(choice,num1,num2):
        
            if choice == '+':
                return add(num1,num2)

            elif choice == '-':
                return subtract(num1,num2)

            elif choice == '*':
                return multiply(num1,num2)

            elif choice == '/':
                return divide(num1,num2)

            elif choice == '^':
                return power(num1,num2)

            elif choice == '%':
                return remainder(num1,num2)

            elif choice == '#':
                exit()

        #elif ope == '$':
            #break

            else:
                return ('invalid mark')



    def add(num1,num2):
        sum = num1 + num2
        return str(num1) + ' + ' + str(num2) + ' = ' + str(sum)

    def subtract(num1,num2):
        sub = num1 - num2
        return str(num1) + ' - ' + str(num2) + ' = ' + str(sub)

    def multiply(num1,num2):
        mul = num1 * num2
        return str(num1) + ' * ' + str(num2) + ' = ' + str(mul)

    def divide(num1,num2):
        if num2 == 0 :
            print('float division by zero')
 
            return str(num1) + ' / ' + str(num2) + ' = ' 'None' 
        elif num2 != 0:
            div = num1 / num2
            return str(num1) + ' / ' + str(num2) + ' = ' + str(div)

    def power(num1,num2):
        pow = num1 ** num2
        return str(num1) + ' ^ ' + str(num2) + ' = ' + str(pow)

    def remainder(num1,num2):
        rem = num1 % num2
        return str(num1) + ' % ' + str(num2) + ' = ' + str(rem)

    answer=select_op(choice,a,b)
    print(answer)







   
