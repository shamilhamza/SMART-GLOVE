#include <LiquidCrystal_I2C.h>
#include <Wire.h>

LiquidCrystal_I2C lcd(0x3F, 20, 4); // set the LCD address to 0x27 for a 16 chars and 2 line display
//
int thumb;
int first_finger;
int second_finger;
int third_finger;
int fourth_finger;

void setup() {
  // put your setup code here, to run once:
  pinMode(A0, INPUT);
  pinMode(A1, INPUT);
  pinMode(A2, INPUT);
  pinMode(A3, INPUT);
  Serial.begin(9600);
  lcd.init();                      // initialize the lcd
  lcd.init();
  lcd.backlight();
  lcd.setCursor(3, 0);
  lcd.print("Welcome !");
  delay(1500);
  lcd.clear();
}

void loop() {

  // put your main code here, to run repeatedly:
  int thumb = analogRead(A0);
  int first_finger = analogRead(A1);
  int second_finger = analogRead(A2);
  int third_finger = analogRead(A3);

  Serial.print(thumb);
  Serial.print("\t");
  Serial.print(first_finger);
  Serial.print("\t");
  Serial.print(second_finger);
  Serial.print("\t");
  Serial.print(third_finger);
  Serial.print("\t");
  Serial.println(fourth_finger);
  Serial.print("\t");

  if (thumb <= 20 )
  {
    lcd.clear();
    lcd.setCursor(1, 0);
    lcd.print("I NEED WATER");
    delay(500);

  }
  else if (first_finger <= 20 )
  {
    lcd.clear();
    lcd.setCursor(1, 0);
    lcd.print("I NEED FOOD");
    delay(500);

  }
  else if (second_finger <= 20 )
  {
    lcd.clear();
    lcd.setCursor(1, 0);
    lcd.print("RESTROOM");
    delay(500);
  }

  else if (third_finger <= 20 )
  {
    lcd.clear();
    lcd.setCursor(1, 0);
    lcd.print("SMART GLOVE");
    delay(500);
  }

  else if (third_finger <= 20 && second_finger<=20)
  {
    lcd.clear();
    lcd.setCursor(1, 0);
    lcd.print("I AM FROM HR");
    delay(500);
  }

  else {
    lcd.clear();
    lcd.setCursor(1, 0);
    lcd.print("NOTHING");

  }

}
