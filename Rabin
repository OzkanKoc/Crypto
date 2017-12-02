#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>

long hesapla(char *metin,int uzunluk){
	int i;
	long sayi=0;
	for(i=0;i<uzunluk;i++){
		sayi=(sayi*100)+((int)metin[i]);
	}
	return sayi;
}
int ebob(int r1, int s1, int n, int p, int q){
	int i,k,ebobb;
	int a=fabs(r1-s1);
	k=(a<n) ? a : n;
	for(i=2;i<=k;i++){
		if(a%i==0 && n%i==0) ebobb=i;
	}
	return ebobb;
}
int bolen(int sayi,int n){
	int i,k,ebob;
	k=(sayi<n) ? sayi : n;
	for(i=2;i<=k;i++){
		if(sayi%i==0 && n%i==0) ebob=i;
	}
	return ebob;
}
int main(int argc, char *argv[]) {
	char metin[100];
	int uzunluk,n,p=7,q=11,c,a;
	int mp,mq;
	int yp,yq;
	int r1,r2,s1,s2,sayi1,sayi2;
	
	printf("Sifrelemek istediginiz metni giriniz...\n");
	gets(metin);
	uzunluk=strlen(metin);
	long m=hesapla(metin,uzunluk);
	printf("%1d\n",m);
	m=20;
	n=p*q;
	a=m%n;
	a=a*a;
	c=a%n;
	printf("Sifreli metin: %d\n",c);
	
	mp=pow(c,((p+1)/4)); mp=mp%p;
	mq=pow(c,((q+1)/4)); mq=mq%q;
	yp=-3,yq=2;
	
	r1=(yp*p*mq + yq*q*mp)%n; r1=fabs(r1);
	r2=n-r1;	r2=fabs(r2);
	s1=(yp*p*mq - yq*q*mp)%n;  s1=fabs(s1);
	s2=n-s1;	s2=fabs(s2);
	
	sayi1=ebob(r1,s1,n,p,q);
	//sayi2=ebob(r2,s2,n,p,q);
	sayi2=ebob(s1,r2,n,p,q);

	printf("p:%d q:%d",sayi1,sayi2);
	
	return 0;
}
