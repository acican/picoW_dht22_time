# picoW_dht22_time
![IMG_1452](https://github.com/acican/picoW_dht22_time/assets/10486613/3d2ef213-c1d8-4861-bb94-3762ba0e1ee8)

 
Un exemplu de cod in micropython pentru afisarea temperaturii si a umiditatii urmarind ora exacta, folosind controlerul Raspberry pico W.
- Raspberry pico W
- afisaj OLED: SSD1315 0.96 inch, GROVE v1.0
- interpretor: rp2-pico-w-20230426-v1.20.0.uf2
- modul AM2302

Conectarea la reteaua wifi se face prin libraria "network", furnizand ssid si password-ul ruter-ului.
Dupa conectare se acceseaza serverul ntp printr-o conexiune tip socket.
Afisarea se face pe un display SSD1315 conectat la microcontroler printr-o conexiune I2C, folosind libraria micropython "ssd1306".
Se afiseaza sirurile preformatate, data si ora, temperatura si umiditatea, cu cadenta de o secunda, intr-o bucla infinita.
Senzorul de temperatura si umiditate comunica cu controlerul printr-o conexiune pe 1 fir (in exemplu, de cod, pinul 20) prin intermediul librariei micropython "dht".
