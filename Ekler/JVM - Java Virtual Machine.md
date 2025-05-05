# Java Sanal Makinesi (JVM)

## JVM Nedir?
Java Virtual Machine (JVM), derlenmiş Java programlarını çalıştırmak için tanımlanmış soyut bir makinedir. Basitçe, Java bayt kodunu alıp (derlenmiş Java), uyumlu bir JVM yüklü herhangi bir cihaz veya işletim sisteminde çalıştıran bir çevirmendir ve aynı zamanda çalışma ortamı sağlar.

## JVM Nasıl Çalışır?
JVM şu adımlarla çalışır:

1. **Yükleme (Loading)**  
   Sınıf Yükleyici (Class Loader) sistemi `.class` dosyalarını (bayt kodu) belleğe yükler.
2. **Bağlama (Linking)**  
   - **Doğrulama (Verification)**: Bayt kodunun doğruluğunu ve güvenliğini kontrol eder.  
   - **Hazırlama (Preparation)**: Statik değişkenler için bellek ayırır.  
   - **Çözümleme (Resolution)**: Kod içindeki sembolik referansları doğrudan referanslarla değiştirir.
3. **Başlatma (Initialization)**  
   Statik başlatıcılar ve statik değişkenler ayarlanır.
4. **Çalıştırma (Execution)**  
   - **Yorumlayıcı (Interpreter)**: Bayt kodu talimatlarını tek tek okuyup çalıştırır.  
   - **Anında Derleme (JIT - Just-In-Time) Derleyici**: Çalışma zamanında sık kullanılan bayt kodu yollarını yerel makine koduna çevirerek performansı artırır.
5. **Bellek Yönetimi (Memory Management)**  
   Çöp Toplayıcı (Garbage Collector), artık kullanılmayan belleği otomatik olarak boşaltarak bellek sızıntılarını önler.

## JVM'in Temel Bileşenleri
- **Sınıf Yükleyici (Class Loader)**: Sınıfları ve arayüzleri yükler ve düzenler.  
- **Bayt Kod Doğrulayıcı (Bytecode Verifier)**: Kodun güvenliğini ve bütünlüğünü çalıştırmadan önce doğrular.  
- **Çalışma Motoru (Execution Engine)**: Bayt kodunu yorumlayıcı veya JIT derleyici aracılığıyla çalıştırır.  
- **Çalışma Zamanı Veri Alanları (Runtime Data Areas)**:  
  - *Yığın (Heap)*: Nesneleri ve dizileri depolar.  
  - *Yığın (Stack)*: Her iş parçacığının kendine ait yığını vardır, yerel değişkenleri ve ara sonuçları depolar.  
  - *Komut Sayacı (Program Counter - PC)*: Geçerli talimatın adresini izler.  
- **Yerel Arabirim (Native Interface)**: C veya C++ gibi yerel kütüphanelerle entegrasyon sağlar.  
- **Çöp Toplayıcı (Garbage Collector)**: Otomatik bellek yönetimini gerçekleştirir.

## JVM Neden Önemlidir?
- **Platform Bağımsızlık**: "Bir kez yaz, her yerde çalıştır." Java bayt kodu, uyumlu bir JVM yüklü herhangi bir işletim sisteminde çalışır.  
- **Güvenlik**: Bayt kodu doğrulama ve kontrollü yerel çağrılar sayesinde güvenli bir çalıştırma ortamı sunar.  
- **Performans**: JIT ve uyarlamalı derlemelerle dinamik optimizasyon sağlar.  
- **Bellek Güvenliği**: Otomatik çöp toplama, bellek hatalarını azaltır ve geliştirmeyi basitleştirir.

## Gerçek Hayattan Bir Benzetme
Java kaynak kodunu İngilizce yazdığınızı düşünün. JVM, bu talimatları gittiğiniz her ülkenin (donanım/OS) yerel diline (makine kodu) çeviren çok dilli bir asistan gibidir; böylece her seferinde doğru ve verimli bir şekilde çalışır.
