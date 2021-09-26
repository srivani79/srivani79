#include<iostream>
using namespace std;

int main()
{
char msg[100],ch;
int k;
cout<<"Enter a message to decrypt:";
cin.getline(msg,100);
int j=0;
while(j<=25)
{
for(k=0;msg[k]!='\0';k++)
{
ch=msg[k];
if(ch>='a'&&ch<='z')
{
ch=ch-j;
if(ch<'a')
{
ch=ch+'z'-'a'+1;
}
msg[k]=ch;
}
else if(ch>='A'&&ch<='Z')
{
ch=ch-j;
if(ch>'a')
{
ch=ch+'Z'-'A'+1;
}
msg[k]=ch;
}
}
cout<<"Decrypted msg:"<<j<<""<<msg<<endl;
j++;
}
}


