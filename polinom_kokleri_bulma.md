print("\nax^2+bx+c formatında bir polinom icin a, b ve c degerlerini giriniz!!")
a=int(input("a= "))
b=int(input("b= "))
c=int(input("c= "))
delta=b**2-4*a*c
if(a!=0):
    if(delta>=0):
        x1=(-b+pow(delta,1/2))/2*a
        x2=(-b-pow(delta,1/2))/2*a
        print("Polinom= ",end="")
        if(b==0 and c==0):
            print("x1,x2= 0")
        elif(b==0):
            print(f"({a})x^2+({c})")
            print(f"Bu denklemin kokleri: x1= {x1}, x2= {x2}")
        elif(c==0):
            print(f"({a})x^2+({b})x")
            print(f"Bu denklemin kokleri: x1= {x1}, x2= {x2}")
        else:
            print(f"({a})x^2+({b})x+({c})")
            print(f"Bu denklemin kokleri: x1= {x1}, x2= {x2}")
    elif(delta<0):
        print("Denklemin reel kökü yoktur.")
    else:
        print("Hatalı işlem!!")
elif(a==0):
    print("a sıfır olamaz!!")
else:
    print("Hatalı işlem!!")
