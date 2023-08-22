```c
int buttonPin = D2; // Butonun bağlı olduğu pin
int ledPin = D7; // LED'in bağlı olduğu pin
int buttonState = 0; // Buton durumunu tutmak için değişken

void setup()
{
  pinMode(buttonPin, INPUT_PULLUP); // Buton pini giriş olarak ayarla ve dahili pull-up direncini etkinleştir
  pinMode(ledPin, OUTPUT); // LED pini çıkış olarak ayarla
}

void loop()
{
  buttonState = digitalRead(buttonPin); // Buton durumunu oku

  if (buttonState == LOW) // Buton basıldığında
  {
    digitalWrite(ledPin, HIGH); // LED'i yak
  }
  else // Buton basılı değilse
  {
    digitalWrite(ledPin, LOW); // LED'i söndür
  }
}
```
