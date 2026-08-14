# ECP

To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in

AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in
keil.

APPARATUS REQUIRED

Keil.
Personal Computer
Keil μVision Software
Serial Transfer of Single Byte / Character using 8051 (Keil)


PROGRAM
(i) Serial Port Transfer a Single Character
```c
#include<reg51.h>
void main(void)
{
TMOD=0X20;
TH1=0XFA;
SCON=0X50;
TR1=1;
SBUF='A';
while (T1==0);
T1=0;
while(1);
}
```

(ii) Serial Port to Transfer a Message
```c
#include <reg51.h>
void main(void)
{
unsigned char msg[] = "Aswinth";
unsigned char i;
TMOD = 0x20; // Timer1 Mode2
TH1 = 0xFD; // 9600 baud rate
SCON = 0x50; // Serial mode1
TR1 = 1; // Start Timer1
for(i = 0; msg[i] != '\0'; i++)
{
SBUF = msg[i];
while(TI == 0);
TI = 0;
}
while(1);
}
```
OUTPUT
(i) Serial Port Transfer a Single Character
<img width="1913" height="1192" alt="Screenshot 2026-08-14 084659" src="https://github.com/user-attachments/assets/6a11da91-9037-4e25-9e65-b13744e24930" />








(ii) Serial Port to Transfer a Message
<img width="1399" height="859" alt="Aswinth_Keil_tra" src="https://github.com/user-attachments/assets/8add45b7-af47-4417-9156-633a6acff31d" />










RESULT

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
