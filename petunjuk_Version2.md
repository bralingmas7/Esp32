# Cara Memasukkan Token Telegram ke Kode ESP32

Agar ESP32 dapat mengirim data ke Telegram, Anda **harus memasukkan token bot Telegram** ke dalam kode program. Berikut langkah-langkah dan contohnya:

---

## 1. Dapatkan Token Bot Telegram

1. **Buka Telegram**, cari dan chat dengan **BotFather**.
2. Ketik `/newbot` dan ikuti instruksinya untuk membuat bot baru.
3. Setelah selesai, Anda akan mendapatkan **token bot** seperti:
   ```
   123456789:AAAbbbCccDddEeeFffGggHhhIiiJjjKkk
   ```

---

## 2. Masukkan Token ke Kode ESP32

Pada contoh kode, cari baris berikut:

```cpp
const char* telegramBotToken = "123456789:AA...";
```

Ganti `123456789:AA...` dengan **token bot Telegram** yang Anda dapatkan dari BotFather.

**Contoh:**
```cpp
const char* telegramBotToken = "123456789:AAAbbbCccDddEeeFffGggHhhIiiJjjKkk";
```

---

## 3. Masukkan Chat ID Telegram

- **Chat ID** adalah ID pengguna atau grup tujuan pesan.
- Untuk mengetahui chat ID Anda, bisa gunakan bot seperti [@userinfobot](https://t.me/userinfobot) di Telegram, lalu ketik `/start`, akan muncul chat ID Anda.

Kemudian, masukkan ke kode:

```cpp
const char* chat_id = "123456789"; // Ganti dengan chat ID Anda
```

---

## 4. Simpan dan Upload ke ESP32

Setelah Anda mengganti token dan chat ID:
- Simpan kode.
- Upload ke board ESP32.

---

## Contoh Lengkap Bagian Token

```cpp
const char* ssid = "NAMA_WIFI";
const char* password = "PASSWORD_WIFI";
const char* telegramBotToken = "123456789:AAAbbbCccDddEeeFffGggHhhIiiJjjKkk"; // Token bot Telegram
const char* chat_id = "123456789"; // Chat ID Telegram tujuan
```

---

**Penting:**  
- **Jangan pernah membagikan token bot Telegram Anda ke orang lain.**
- Jika token tersebar, segera buat token baru melalui BotFather.
