
#include<stdio.h>
#include<stdlib.h>
#include <18F4620.h>
#fuses HS, NOFCMEN, NOIESO, PUT, NOBROWNOUT, NOWDT
#fuses NOPBADEN, NOMCLR, STVREN, NOLVP, NODEBUG
#use delay(clock=16000000)

#define __DEBUG_SERIAL__ //Si comentas esta linea se deshabilita el debug por serial y el PIN_C6 puede ser usado en forma digital I/O

#ifdef __DEBUG_SERIAL__
   #define TX_232        PIN_C6
   #use RS232(BAUD=9600, XMIT=TX_232, BITS=8,PARITY=N, STOP=1)
   #use fast_io(c)
#endif

void main (void){
   setup_oscillator(OSC_16MHZ);
#ifdef __DEBUG_SERIAL__
   void clean(void);   //012  3
   char cadena[13];    //1+2(13)
   int c=0,i=0;
   int iniciar=0;
   int a=0;
   char palabra[10]
   int contador=0;
   void main(void){  
   printf("Introduzca los datos de la siguiente forma (1+2 enter): ");
   while(TRUE){
       if(kbhit()){
              cadena[a]=getch();
              if(cadena[a]>=65 && cadena[a]<=122 || cadena[a]==13){
              printf("%c",cadena[a]);
              if(cadena[a]==13)
              {
                  iniciar=1;   
              }
         a++;
      }
}
    while(cadena[i]!=32 && cadena[i]!=13){
    contador++;
    i++;
}
}
