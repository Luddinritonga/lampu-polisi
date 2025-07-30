# 💡 Arduino Project: LED Blink, Running LED, & Efek Lampu Polisi

Proyek sederhana menggunakan Arduino untuk: [Tonton tutorial di YouTube](https://youtu.be/abcdefghijk) atau 
[Jalankan langsung di Wokwi](https://wokwi.com/projects/437877847458967553)
<br>
✅ LED Blink (kedip biasa)<br>
✅ Running LED (lampu berjalan)<br>
✅ Efek Lampu Polisi (bergantian kanan-kiri)<br>

---

## 📦 Komponen
| Komponen | Jumlah |
|--------:|:------:|
| Arduino Uno | 1 |
| LED merah | 2 |
| LED kuning | 4 |
| Resistor 220Ω | 6 |
| Kabel jumper | secukupnya |
| Breadboard | 1 |

---

## ⚡ Wiring
- Pin D2 → LED merah kiri (lampu polisi)
- Pin D3 → LED merah kanan (lampu polisi)
- Pin D4–D7 → LED kuning (running LED)
- Pin 13 → LED built-in (blink)
- Semua LED dipasang resistor seri 220Ω

---

## 💻 Kode Lengkap
```cpp
int ledBlink = 13;
int ledPolisi1 = 2;
int ledPolisi2 = 3;
int ledRunning[] = {4, 5, 6, 7};

void setup() {
  pinMode(ledBlink, OUTPUT);
  pinMode(ledPolisi1, OUTPUT);
  pinMode(ledPolisi2, OUTPUT);
  for (int i = 0; i < 4; i++) {
    pinMode(ledRunning[i], OUTPUT);
  }
}

void loop() {
  // LED Blink
  digitalWrite(ledBlink, HIGH);
  delay(500);
  digitalWrite(ledBlink, LOW);
  delay(500);

  // Running LED
  for (int i = 0; i < 4; i++) {
    digitalWrite(ledRunning[i], HIGH);
    delay(200);
    digitalWrite(ledRunning[i], LOW);
  }

  // Efek Lampu Polisi
  for (int i = 0; i < 5; i++) {
    digitalWrite(ledPolisi1, HIGH);
    digitalWrite(ledPolisi2, LOW);
    delay(100);
    digitalWrite(ledPolisi1, LOW);
    digitalWrite(ledPolisi2, HIGH);
    delay(100);
  }
  digitalWrite(ledPolisi1, LOW);
  digitalWrite(ledPolisi2, LOW);
}
```

## 📷 **skema / rangkaian**

![Lampu RGB Arduino](https://github.com/Luddinritonga/lampu-polisi/blob/main/skema.png)

## 🔧 **Cara Upload**
1. Sambungkan Arduino ke PC via kabel USB
2. Buka file `.ino` di Arduino IDE
3. Pilih board dan port yang sesuai
4. Upload kode ke Arduino




## 📫 Contact Me
[![Website](https://img.shields.io/badge/Website-000000?style=for-the-badge&logo=about-dot-me&logoColor=white)](https://luddinritonga.github.io/fortopolio/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/luddinritonga)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:luddinritonga03@gmail.com)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@sekedarcandu)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/luddin-ritonga-727920307?)


