while(True):

    try:
        asal=int(input("sayı:"))
        if(asal<=0 or asal == 1):
            print("0 , 1 , veya negatif sayı girmeyiniz!!")
            continue
    except(ValueError):
        print("Tam sayı giriniz!!")
        continue
    else:
        asal_kontrol=True
        for i in range(2,asal):
            if(asal%i==0):
                asal_kontrol=False
                break
            else:
                continue
    if(asal_kontrol):
        print("sayi asal")
    else:
        print("sayı asal değil")

