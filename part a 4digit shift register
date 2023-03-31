# Lab_2 1.	Display different number on four 7-seg using 74HC595
int data= 13;//information pin first wire from left
int latch= 12;//latch pin  middle wire
int cl= 11;///clock pin first wire from right
int digitPins[4]={11,10,9,8};// pin controlling digits in order of(4-3-2-1).
const byte digits[10]={ //leds number's showing state
  B00111111, //0
  B00000110,//1
  B01011011,//2
  B01001111,//3
  B01100110,//4
  B01101101,//5
  B01111101,//6
  B00000111,//7
  B01111111,//8
  B01101111,//9
  };

void setup(){
 pinMode(latch,OUTPUT);
pinMode(cl,OUTPUT);
pinMode(data,OUTPUT);
pinMode(11,OUTPUT);
pinMode(10,OUTPUT);
pinMode(9,OUTPUT);
pinMode(8,OUTPUT);
}
void loop(){
  digitalWrite(11,HIGH);
digitalWrite(10,HIGH);
digitalWrite(9,HIGH);
digitalWrite(8,LOW);
digitalWrite(latch,LOW);
shiftOut(data,cl,MSBFIRST,digits[8]);
digitalWrite(latch,HIGH); 
delay(5);
///second digit
digitalWrite(11,HIGH);
digitalWrite(10,HIGH);
digitalWrite(9,LOW);
digitalWrite(8,HIGH);
digitalWrite(latch,LOW);
shiftOut(data,cl,MSBFIRST,digits[6]);
digitalWrite(latch,HIGH); 
delay(5);
///third digit
digitalWrite(11,HIGH);
digitalWrite(10,LOW);
digitalWrite(9,HIGH);
digitalWrite(8,HIGH);
digitalWrite(latch,LOW);
shiftOut(data,cl,MSBFIRST,digits[5]);
digitalWrite(latch,HIGH); 
delay(5);
//fourth digit
digitalWrite(11,LOW);
digitalWrite(10,HIGH);
digitalWrite(9,HIGH);
digitalWrite(8,HIGH);
digitalWrite(latch,LOW);
shiftOut(data,cl,MSBFIRST,digits[2]);
digitalWrite(latch,HIGH); 
delay(5);
}
