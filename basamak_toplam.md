#5 basamaklı bir sayının, basamaklarının toplamı

sayi=int(input("5 basamakli bir sayi giriniz: "))
toplam=0
while(sayi>0):
    basamak=sayi%10
    toplam=toplam+basamak
    sayi=int(sayi/10)

print(toplam)
