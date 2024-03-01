sayi=int(input("Piramit tabanını belirleyiniz: "))
if(sayi%2==1):
    tek_baslangic=int((sayi-1)/2)
    for i in range(1,sayi+1,2):
        print(" "*tek_baslangic, end="")  # end="" koymamızın sebebi; end koymazsak farklı print fonksiyonuna yazmaya 
        tek_baslangic=tek_baslangic-1     # başladığımızda alta geçiyo yani boşluk atsa bile yeni print fonksiyonunda   
        print("*"*i)                      # alt satıra geçiceği için satırın başından başlıcak.

if(sayi%2==0):
    cift_baslangic=int((sayi/2)-1)
    for i in range(2,sayi+1,2):
        print(" "*cift_baslangic, end="")
        cift_baslangic=cift_baslangic-1
        print("*"*i)
