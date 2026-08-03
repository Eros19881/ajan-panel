# 🌟 Gizli Ajan (Eros Star) — Discord İzleme Paneli

Bu proje, Discord sunucunuzdaki anlık mesaj akışını, aktif üyeleri ve istatistikleri doğrudan web tarayıcınızdan, **muhteşem bir arayüzle** izlemenizi sağlayan Node.js tabanlı bir "Gizli Ajan" (İzleme Paneli) sistemidir.

---

## 🎨 Panel Özellikleri

- **🌌 Göz Alıcı Tasarım**: Kayar yıldızlar (starfield), aurora gradient arka planı ve siber grid tasarımı.
- **📋 Canlı Log Akışı**: Sunucuda atılan her mesaj (DM hariç) anlık olarak, silinse dahi panele düşer. 
- **👥 Üye Entegrasyonu**: Sunucudaki üyeler otomatik alınır, katılış tarihleri, Discord ID'leri, rolleri ve hesap açılış tarihleri listelenir.
- **🖼️ Gerçek Avatarlar**: Mesaj atanların ve üyelerin anlık Discord profil fotoğrafları yansıtılır.
- **📊 Canlı İstatistikler**:
  - En çok mesaj atanlar sıralaması (Altın, Gümüş, Bronz)
  - En aktif kanallar bar grafiği
  - Saniye bazlı mesaj/dakika hızı
- **📥 Dışa Aktarma**: Toplanan logları tek tıkla `.txt` formatında bilgisayarınıza indirebilirsiniz.

---

## 🚀 Kurulum & Çalıştırma (Kendi Bilgisayarın İçin)

### 1. Gereksinimleri Yükle
Terminali açın ve projenin olduğu klasörde şu komutu çalıştırarak gerekli paketleri indirin:
```bash
npm install express socket.io discord.js dotenv
```

### 2. .env Dosyası Ayarları
Proje klasöründe `.env` isimli bir dosya oluşturun ve içine bot tokeninizi ekleyin:
```env
DISCORD_TOKEN=senin_bot_tokenin_buraya_gelecek
```

### 3. Sistemi Başlat
Aşağıdaki komutu girerek hem botu hem de paneli aynı anda ayağa kaldırın:
```bash
node server.js
```

### 4. Panele Giriş
Bot başarıyla başladıktan sonra tarayıcında şu adresi aç:
👉 **[http://localhost:3000](http://localhost:3000)**

---

## ☁️ WispByte / Pterodactyl Panelde Çalıştırma (Hosting)

Bu projeyi uzak bir hosting sunucusunda (WispByte, Pterodactyl vb.) 7/24 çalıştırıyorsanız:

1. WispByte panelinizden **Ağ (Network) / Portlar** kısmına gidin.
2. Sistemin size verdiği portu **Birincil (Primary)** port olarak atadığınızdan emin olun.
3. Botu `node server.js` komutuyla başlattığınızda, bot hostinginizin verdiği IP ve Port üzerinden otomatik olarak paneli aktif edecektir.
4. Örneğin: `http://192.168.1.1:8080` adresinden panelinize ulaşabilirsiniz!

---

## ⚠️ Önemli Discord Bot İzinleri (Developer Portal)

Botunuzun mesaj içeriklerini ve üye listelerini okuyabilmesi için **[Discord Developer Portal](https://discord.com/developers/applications)** üzerinden şu iki ayrıcalıklı yetkiyi (Intents) açmalısınız:
- ✅ **Server Members Intent** (Tüm üyeleri görebilmek için)
- ✅ **Message Content Intent** (Mesajların ne olduğunu okuyabilmek için)

Aksi halde bot mesaj içeriklerini göremez ve paneli boş bırakır!

---
*Gölge operasyonları için tasarlandı. 🕵️‍♂️*
