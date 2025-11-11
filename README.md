# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**
<br>
<br>
<br>
<img width="1919" height="1139" alt="Screenshot 2025-11-11 081944" src="https://github.com/user-attachments/assets/6cbaa934-537a-4b95-ae35-39f50f4df901" />


<img width="1919" height="1139" alt="Screenshot 2025-11-11 082711" src="https://github.com/user-attachments/assets/815cf099-3e8f-4732-ad4f-a5df7ae6da6b" />


<br>
<br>

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
