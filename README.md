# Multiple-Node
# Multiple Network Linux Kurulum Rehberi

![image](https://github.com/user-attachments/assets/c725edf7-947f-4c51-9949-c07f73a53d24)


## 1. İstemciyi İndirme

Linux için istemciyi indirelim:

```bash
wget https://cdn.app.multiple.cc/client/linux/x64/multipleforlinux.tar
```

## 2. Arşivi Çıkarma

Kurulum paketini çıkaralım ve bağlayalım:

```bash
tar -xvf multipleforlinux.tar
cd multipleforlinux
```

## 3. Gerekli İzinlerin Verilmesi

Dosyalara gerekli izinleri verelim:

```bash
chmod +x ./multiple-cli
chmod +x ./multiple-node
```

## 4. Yol Değişkenini Ayarlama

Gerekli dizinleri PATH değişkenine ekleyelim:

```bash
export PATH=$PATH:/root/multipleforlinux/
source /etc/profile
```

## 5. Dizin İzinlerinin Ayarlanması

Dizin ve dosyalara tam erişim izni verelim:

```bash
chmod -R 777 multipleforlinux
```

## 6. Programı Başlatma

Programı arka planda çalıştıralım:

```bash
nohup ./multiple-node > output.log 2>&1 &
```

## 7. Hesap Bağlama

[Web sitesinden](https://www.app.multiple.cc/#/signup?inviteCode=v1jzk7hL) kayıt olduktan sonra oluşturulan identifier kullanarak bağlayalım:
(ŞİFRE kendinize göre koyun, depolama bant genişliği ayarlarını kendi sunucunuza göre ayarlayabilirsiniz.)

```bash
./multiple-cli bind --bandwidth-download 100 --identifier <İDENTİFİER> --pin <ŞİFRE> --storage 200 --bandwidth-upload 100
```

## 8. Yardım Komutları

Diğer komutları görmek için:

```bash
multiple-cli --help
```

