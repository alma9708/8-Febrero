# 8-Febrero
Encendido y apagado de LEDs con delay controlado por entrada del usuario a monitor serial.
int AZUL=13;
int VERDE=11;
int ROJO=9;
int t1;
int t2;
int t3;

void setup() {
// put your setup code here, to run once:
Serial.begin(9600);
Serial.println("¿cuanto tiempo quieres?");
delay (5000);
while(Serial.available () ==0){

}
t1=Serial.parseInt();
pinMode(AZUL, OUTPUT);

Serial.begin(9600);
Serial.println("¿cuanto tiempo quieres?");
delay (5000);
while(Serial.available () ==0){

}
t2=Serial.parseInt();
pinMode(VERDE, OUTPUT);

Serial.begin(9600);
Serial.println("¿cuanto tiempo quieres?");
delay (5000);
while(Serial.available () ==0){

}
t3=Serial.parseInt();
pinMode(ROJO,OUTPUT);

}

void loop() {
// put your main code here, to run repeatedly:
digitalWrite(AZUL,HIGH);
delay (t1);
digitalWrite(AZUL,LOW);
delay (t1);

digitalWrite(VERDE,HIGH);
delay (t2);
digitalWrite(VERDE,LOW);
delay (t2);

digitalWrite(ROJO,HIGH);
delay (t3);
digitalWrite(ROJO,LOW);
delay (t3);
