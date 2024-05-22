//# arduino_LCD_HelloWorld
//Test Drive for first time using Arduino

#include <LiquidCrystal_I2C.h>

LiquidCrystal_I2C lcd(0x27, 16, 2); 

void setup() {
  lcd.init();                      
  lcd.backlight();                 
}

void loop() 
{
  for (int i = 0; i < 16; i++) {
    lcd.clear();
    lcd.setCursor(i, 0);
    lcd.print("Hello World");
    delay(200);  
  }

  for (int i = 16; i >= 0; i--) {
    lcd.clear();
    lcd.setCursor(i, 1);
    lcd.print("Welcome");
    delay(200);
  }

  for (int i = 0; i < 13; i++) {
    lcd.clear();
    lcd.setCursor(i, 0);
    lcd.print("My Name Is");
    delay(200);  
  }

  for (int i = 12; i >= 0; i--) {
    lcd.clear();
    lcd.setCursor(i, 1);
    lcd.print("SabakunZ");
    delay(200); 
  }

