#include<Servo.h>
Servo myServo;
void setup() {
    myServo.attach(2);  // Enter the pin (any pin as u set in arduino)
    Serial.begin(9600);
}

void loop() {
  // for clockwise 180 degree movement
  int i;
  for(i=0;i<=180;i++)
  {
    Serial.println(" Rotation in clockwise direction");
    myServo.write(i);
    delay(10);   //  delay is added to control the speed of the servo movement
  }
  // for 180 degree anti-clockwise movement
  for(i=180;i>=0;i--)
  {
    Serial.println(" Rotation in anit-clockwise direction");
    myServo.write(i);
    delay(10);   //  delay is added to control the speed of the servo movement
  }
}