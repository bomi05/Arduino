// include the library code:
#include <LiquidCrystal.h>

// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  Serial.begin(9600);
  // Print a message to the LCD.
}

void loop()
{
  lcd.clear();
  int read = analogRead(A0);
  float temperature = (5.0 * read * 100) / 1024;
  Serial.print("Temperature : ");
  lcd.print(temperature);
  Serial.println(temperature);
  
  if (temperature >= 100)
  {
    lcd.setCursor(0,1);
    lcd.print("DANGER");
    delay(50);
  }
  else if (50 <= temperature && temperature <= 80)
  {
    lcd.setCursor(0,1);
    lcd.print("GOOD");
  }
  else if (temperature <= 15)
  {
    lcd.setCursor(0,1);
    lcd.print("BAD");
  }
  delay(1500);
}
 
