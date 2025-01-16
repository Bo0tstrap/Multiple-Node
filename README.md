# Multiple-Node
# Multiple Network Linux Kurulum Rehberi

## 1. İstemciyi İndirme

Linux mimariniz için uyumlu istemciyi indirin:

```bash
wget https://cdn.app.multiple.cc/client/linux/x64/multipleforlinux.tar
```

## 2. Arşivi Çıkarma

Kurulum paketini çıkarın:

```bash
tar -xvf multipleforlinux.tar
```

## 3. Gerekli İzinlerin Verilmesi

Çalıştırılabilir dosyalara gerekli izinleri verin:

```bash
chmod +x ./multiple-cli
chmod +x ./multiple-node
```

## 4. Yol Değişkenini Ayarlama

Gerekli dizinleri PATH değişkenine ekleyin:

```bash
export PATH=$PATH:/root/multipleforlinux/
source /etc/profile
```

## 5. Dizin İzinlerinin Ayarlanması

Dizin ve dosyalara tam erişim izni verin:

```bash
chmod -R 777 multipleforlinux
```

## 6. Programı Başlatma

Programı arka planda çalıştırın:

```bash
nohup ./multiple-node > output.log 2>&1 &
```

## 7. Hesap Bağlama

Resmi web sitesinden kayıt olduktan sonra oluşturulan identifieri kullanarak bağlayın:

```bash
multiple-cli bind --bandwidth-download 100 --identifier <BENZERSIZ_KIMLIK> --pin <PIN_KODU> --storage 200 --bandwidth-upload 100
```

## 8. Yardım Komutları

Diğer komutları görmek için:

```bash
multiple-cli --help
```

