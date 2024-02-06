// basit kullanisli hesap makinesi
#include <stdio.h>
#include <math.h>
int topla(int a,int b);
int cikar(int a,int b);
int carp(int a,int b);
int bolme(int a,int b);
int us(int a,int b);
int faktoriyel(int x);
int kare(int x);
int kup(int x);
float karekok(int x);
int main() {
    int a,b,kontrol;
    char c;
    printf("!!!!!!!!NOT!!!!!!!\nu: us almak\nf: faktoriyel almak\nk: kare almak\nl: kup almak\ns: karekok almak");
    printf("\nBasit islemler(+,-,*,/,u) icin 1'e;\nBaska islemler icin(!,kare,kup,karekok) 2'ye basin:");
    scanf("%d",&kontrol);
    if(kontrol==1){
        printf("\niki sayiyi isleme sokun(+,-,*,/,u) --> orn; 5u3 = 125\n");
        for(int i=0;i<100;i++){
            scanf("%d",&a);
            scanf(" %c",&c);
            scanf("%d",&b);
            if(c=='+'){
                printf("%d",topla(a,b));
            }
            else if(c=='-'){
                printf("%d",cikar(a,b));
            }
            else if(c=='*'){
                printf("%d",carp(a,b));
            }
            else if(c=='/'){
                printf("%d",bolme(a,b));
            }
            else if(c='u'){
                printf("%d",us(a,b));
            }
            else {
                printf("hatali islem");
                break;
            }
            printf("\n");
        }
    }
    else if(kontrol==2){
        printf("Yapmak istediginiz islemi yazin(!,k,l,s) --> orn; 16s = 4\n");
        for(int i=0;i<100;i++){
            int x;
            char c2;
            scanf("%d",&x);
            scanf(" %c",&c2);
            if(c2=='!'){
                printf("%d",faktoriyel(x));
            }
            else if(c2=='k'){
                printf("%d",kare(x));
            }
            else if(c2=='l'){
                printf("%d",kup(x));
            }
            else if(c2=='s'){
                printf("%f",karekok(x));
            }
            
            
            printf("\n");
        }
    }
    
    return 0;
}
int topla(int a,int b){
    return a+b;
}
int cikar(int a,int b){
    return a-b;
}
int carp(int a,int b){
    return a*b;
}
int bolme(int a,int b){
    return a/b;
}
int us(int a,int b){
    return pow(a,b);
}
int faktoriyel(int x){
    int carpim=1;
    for(int i=2;i<=x;i++){
        carpim=carpim*i;
    }
    return carpim;
}
int kare(int x){
    return x*x;
}
int kup(int x){
    return x*x*x;
}
float karekok(int x){
    return sqrt(x);
}
