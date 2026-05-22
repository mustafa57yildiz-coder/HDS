# Haftalık Ders Programı (HDS)

Haftalık Ders Programı (HDS), okullar ve eğitim kurumları için tasarlanmış, yapay zeka destekli gelişmiş bir ders programı hazırlama Windows uygulamasıdır.

## Temel Özellikler

- **Yapay Zeka Destekli Dağıtım**: Tabu Arama, Yapay Arı Kolonisi (ABC), Karınca Kolonisi (ACO) ve Parçacık Sürü Optimizasyonu (PSO) gibi sezgisel algoritmalar kullanılarak ders programındaki karmaşık kısıtlar otomatik çözülür ve ideal dağılım sağlanır.
- **Kapsamlı Okul Yönetimi**: 
  - Öğretmen, Sınıf ve Ders tanımlamaları.
  - Öğretmenlerin ders atamalarının detaylı yapılandırılması.
  - Sosyal Kulüp ve eğitici kolların yönetimi.
- **Excel Entegrasyonu**: Tüm tanımlı verileri ve sonuç programını `ClosedXML` altyapısı sayesinde kolayca Excel'e aktarabilir, aynı zamanda dışarıdan Excel verisi içeri aktarabilirsiniz.
- **Veritabanı Altyapısı**: Entity Framework Core 10 ve SQLite ile hızlı, taşınabilir ve güvenilir veri yönetimi.
- **Otomatik Güncelleme Sistemi**: GitHub entegrasyonu sayesinde yeni bir güncelleme (Release) yayınlandığında program içinden tek tıkla otomatik tespit edilir ve kurulur.

## Kullanılan Teknolojiler

- **Dil / Platform:** C# / .NET 10.0 (net10.0-windows)
- **Arayüz:** Windows Forms (WinForms)
- **Veritabanı:** Microsoft Entity Framework Core (SQLite)
- **Kurulum/Dağıtım:** Inno Setup 6 (Otomatik kurulum paketi hazırlama desteğiyle)

## Kurulum ve Dağıtım

Projeyi kaynak koddan derleyip doğrudan Windows için Setup (Kurulum) paketi haline getirmek isterseniz:

1. Sisteminizde **Inno Setup 6**'nın kurulu olduğundan emin olun.
2. Proje dizinindeki `build_setup.ps1` script dosyasına sağ tıklayıp **"PowerShell ile Çalıştır"** diyerek çalıştırın.
3. Script otomatik olarak projeyi `Release` modunda derleyecek (`dotnet publish`) ve Inno Setup aracılığıyla tek bir `HaftalikDersProgrami_Setup.exe` kurulum dosyası oluşturacaktır.

## Güncellemeler ve GitHub Entegrasyonu

Bu proje, güncellemelerini otomatik olarak aşağıdaki GitHub adresi üzerinden kontrol etmektedir:
[https://github.com/mustafa57yildiz-coder/HDS](https://github.com/mustafa57yildiz-coder/HDS)

GitHub'da projeye yeni bir `Release` (Sürüm) eklendiğinde ve derlenmiş Setup dosyası varlıklar (Assets) bölümüne eklendiğinde; uygulama içerisindeki "Sürümü Güncelle" bölümünden en yeni sürüm kullanıcılara sunulur ve indirme işlemi program tarafından gerçekleştirilir.

## Lisans

Bu proje, eğitim kurumlarının kullanımı için tasarlanmıştır. Tüm hakları saklıdır.
