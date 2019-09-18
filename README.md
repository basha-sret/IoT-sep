int rled;
int yled;
int bled;
int wled;
void setup()
{
  pinMode(13,OUTPUT);
  pinMode(11,OUTPUT);
  pinMode(9,OUTPUT);
  pinMode(7,OUTPUT);
  Serial.begin(9600);
  
}
void loop()
{
  Serial.println("how many times u want to blink red led");
  while (Serial.available()==0){ }
  rled=Serial.parseInt();
  Serial.println("how many times u want to blinkyellow led");
  while(Serial.available()==0){}
  yled=Serial.parseInt();
  Serial.println("how many times you want to blink blue led");
  while(Serial.available()==0){}
  bled=Serial.parseInt();
  Serial.println("how many times u want to print white led");
  while(Serial.available()==0){}
  wled=Serial.parseInt();
   for(int i=0;i<rled;i++){
    Serial.print("you r on blink ");
    Serial.println(i);
    digitalWrite(13,HIGH);
    delay(100);
    digitalWrite(13,LOW);
   }
   for(int j=0;j<yled;j++){
    Serial.print("you r on blink ");
    Serial.println(j);
    digitalWrite(11,HIGH);
    delay(100);
    digitalWrite(11,LOW);
   }
   for(int k=0;i<bled;k++){
    Serial.print("you r on blink ");
    Serial.println(k);
    digitalWrite(9,HIGH);
    delay(100);
    digitalWrite(9,LOW);
   }
   for(int l=0;i<wled;l++){
    Serial.print("you r on blink ");
    Serial.println(l);
    digitalWrite(7,HIGH);
    delay(100);
    digitalWrite(7,LOW);
   }
  
}
