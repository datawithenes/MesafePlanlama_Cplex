
# Mesafe Planlama ve Sağlık Ocağı Yerleştirme (CPLEX)

Bu proje, Aydın ilinin Söke ilçesindeki **13 sağlık ocağının** yerleşim planını optimize etmek amacıyla geliştirilmiştir. Sağlık ocaklarının mevcut yerleşiminin, mesafe ve nüfus yoğunluğu gibi faktörler göz önüne alındığında yeterli seviyede olmadığı düşünülmüş ve **CPLEX** programı kullanılarak daha verimli bir yerleşim planı önerilmiştir. Bu projede, mahallelerin mesafeleri ve nüfusları baz alınarak sağlık ocaklarının yeniden yerleştirilmesi yapılmıştır.

Sonuçlar, beklediğimden farklı çıkmış ve mevcut sistemle karşılaştırıldığında daha verimli bir yerleşim planı ortaya konmuştur.

## Proje Özeti

Bu proje, aşağıdaki temel hedeflere odaklanmaktadır:

- **Sağlık Ocağı Yerleştirme Optimizasyonu**: 13 sağlık ocağının en uygun yerlere yerleştirilmesi, mevcut yerleşim ile karşılaştırılarak yapılmıştır.
- **Mesafe ve Nüfus Faktörleri**: Yerleşim planı, mahalleler arasındaki mesafeler ve her mahalledeki nüfus yoğunluğu gibi veriler dikkate alınarak optimize edilmiştir.
- **CPLEX Optimizasyon Algoritmaları**: IBM ILOG CPLEX Optimization Studio kullanılarak yerleştirme ve optimizasyon hesaplamaları gerçekleştirilmiştir.
- **Sonuç Karşılaştırması**: Mevcut sağlık ocağı yerleşimi ile optimize edilmiş yeni yerleşim planının karşılaştırılması yapılmıştır.

## Kullanılan Araçlar ve Teknolojiler

- **IBM ILOG CPLEX Optimization Studio**: Optimizasyon algoritmalarının uygulanması ve çözüm sürecinin gerçekleştirilmesi için kullanılmıştır.
- **Python**: Veri işleme ve analiz sürecinde kullanılmıştır. Python, CPLEX ile entegrasyonu sağlamak için de kullanılmıştır.
- **Veri Seti**: Mahalleler arasındaki mesafeler ve nüfus yoğunlukları gibi veriler, Aydın ilinin Söke ilçesindeki mahallelerden alınmıştır.

## Veri Seti

Veri seti, Söke ilçesindeki 13 sağlık ocağının mevcut yerleşim yerlerini, mahalleler arasındaki mesafeleri ve her mahalledeki nüfus yoğunluğunu içermektedir. Veriler aşağıdaki gibi organize edilmiştir:

- **Mahalle Adı**: Her mahalle ismi.
- **Nüfus Yoğunluğu**: Her mahalledeki nüfus sayısı.
- **Mesafeler**: Mahalleler arasındaki mesafeler, coğrafi olarak hesaplanmış ve kilometre cinsinden verilmiştir.
- **Mevcut Sağlık Ocağı Yerleşimi**: 13 sağlık ocağının mevcut yerleri.
- **Önerilen Sağlık Ocağı Yerleşimi**: CPLEX ile hesaplanan ve önerilen sağlık ocağı yerleşim planı.

## Optimizasyon Modeli

### Adımlar

1. **Veri Hazırlığı**: Mahalleler arasındaki mesafeler ve nüfus yoğunlukları gibi veriler toplanarak optimize edilmesi gereken parametreler belirlendi.
   
2. **Optimizasyon Problemi Tanımlaması**:
   - **Amaç Fonksiyonu**: Sağlık ocaklarının mahallelere olan mesafelerinin ve nüfus yoğunluğunun minimize edilmesi hedeflenmiştir. Bu, toplam ulaşım mesafesi ve sağlık hizmetine erişim kolaylığı üzerinde olumlu etkiler yaratacaktır.
   - **Kısıtlar**: Sağlık ocakları sadece belirli mahallelere yerleştirilebilir ve her sağlık ocağı yalnızca bir mahallede yer alabilir. Ayrıca, her sağlık ocağının nüfus yoğunluğuna göre kapasite gereksinimlerini karşılaması gerekmektedir.

3. **CPLEX Kullanımı**: IBM ILOG CPLEX kullanılarak, **lineer programlama** (LP) ve **karışık tam sayılı programlama** (MIP) algoritmaları ile optimizasyon yapılmıştır. CPLEX'in sunduğu güçlü algoritmalar sayesinde, farklı parametreler ve kısıtlarla en uygun sağlık ocağı yerleşim planı bulunmuştur.

4. **Sonuçların Karşılaştırılması**:
   - Mevcut sağlık ocağı yerleşim planı ile önerilen yerleşim planı karşılaştırılmıştır.
   - Grafiksel olarak mesafeler, nüfus yoğunluğu ve sağlık ocaklarının erişilebilirliği analiz edilmiştir.

## Proje Sonuçları

CPLEX kullanarak yapılan optimizasyon sonucunda:

- **Mevcut Yerleşim**: Sağlık ocaklarının mevcut yerleşimi, bazı mahalleler için yeterli erişim sağlamamakta ve mesafeler oldukça uzun kalmaktadır.
- **Optimizasyon Sonuçları**: Yeni yerleşim planı, mahallelere daha yakın sağlık ocakları yerleştirilerek, ulaşım mesafelerinin ve sağlık hizmetlerine erişim zamanlarının azaltılmasını sağlamıştır. Ayrıca, nüfus yoğunluğuna göre optimize edilen yerleşim, her mahalle için daha adil bir sağlık hizmeti dağılımı sunmaktadır.

## Sunum ve Raporlar

Projenin detaylı analizi ve karşılaştırma sonuçları hakkında daha fazla bilgi almak için sunum dosyasını ve raporları PDF olarak dosyalar kısmından indirip inceleyebilirsiniz.



## Kurulum ve Çalıştırma

Proje dosyalarını çalıştırmak ve analizleri yapabilmek için aşağıdaki adımları takip edebilirsiniz:

### 1. IBM ILOG CPLEX Kurulumu

CPLEX'in çalışabilmesi için **IBM ILOG CPLEX Optimization Studio** yüklü olmalıdır. IBM'in resmi web sitesinden CPLEX'i indirip kurabilirsiniz.

- [IBM ILOG CPLEX İndir](https://www.ibm.com/products/ilog-cplex-optimization-studio)

### 2. Python Entegrasyonu

Python ve CPLEX entegrasyonu için aşağıdaki adımları takip edebilirsiniz:

1. Python'ı kurun (Python 3.x).
2. `cplex` Python modülünü yükleyin:
   ```bash
   pip install cplex
   ```

3. Optimizasyon modeli ve verileri hazırlayın ve Python betiğini çalıştırarak sonuçları elde edin.

### 3. Çalıştırma

Projenin tamamı CPLEX ve Python arasında entegrasyon sağlanarak çalıştırılabilir. Verilerinizi hazırladıktan sonra optimizasyon modelini çalıştırabilir ve sonuçları analiz edebilirsiniz.

## Katkı Sağlama

Bu projeye katkı sağlamak isterseniz, lütfen şu adımları takip edin:

1. Bu projeyi forkladığınızda kendi dalınızı oluşturun.
2. Yeni özellikler veya hata düzeltmeleri ekleyin.
3. Pull request oluşturun.

## Lisans

Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.

