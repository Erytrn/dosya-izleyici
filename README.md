# File Watcher & Executor (Dosya İzleyici ve Çalıştırıcı)

Bu proje, belirlenen bir dizindeki dosya değişikliklerini (oluşturma, silme, değiştirme) gerçek zamanlı izleyen ve buna bağlı olarak otomatik komut çalıştıran bir otomasyon aracıdır. VirtualBox gerektirmez, Go ve fsnotify kullanılarak performanslı bir şekilde tasarlanmıştır.

## Özellikler

- **Event Loop:** Dosya sistemi olaylarını asenkron olarak dinler.
- **Filtreleme:** Sadece `.js` ve `.py` uzantılı dosyalardaki değişimleri algılar.
- **Debounce (Geciktirme):** Üst üste gelen kayıt işlemlerini gruplayarak gereksiz komut tekrarını önler (500ms).
- **Otomasyon:** Değişiklik algılandığında belirlenen terminal komutunu çalıştırır.

## Kurulum ve Çalıştırma

1. Projeyi indirin.
2. `src` klasörüne gidin.
3. Aşağıdaki komutla çalıştırın:
   ```bash
   go run main.go