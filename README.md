# Django-Project-3--TheNewBoston--

Django

    • Django ,  Python ile kullanılan bir web framework’tür.
    • Windows’ta PowerShell’i yönetici olarak çalıştırıyoruz. Linux ve Max’te ise terminalde sudo komutunu kullanıyoruz .
    • Proje geliştirmek için Python bilgisine ihtiyaç vardır.
    • Python versiyon sorgulamak için terminale;
        ◦ Python –version
    • Kurulumları gerçekleştirmek için pip kurmak gerekiyor
        ◦ Sudo apt-get install python-pip
    • Windows pip için easy_install versiyon sorgulama;
        ◦ Easy_install –version (12.04 üstü)
        ◦ Kurulum yeri C/Python34/scripts
    • Pip’in Windows’ta tanımlanması için easy_install’a sağ tıklayarak yolunu kopyalıyoruz ,Bilgisayarıma sağ ytılayarak Özellikler -> Gelişmiş Sistem Ayarları -> Ortam Değişkenleri -> Path alanına kopyaladığımız adresi ekliyoruz. Sonra da Shell’i yeniden başlatıyoruz.
    • https://boostrap.pypa.io/ez_setup.py sitesine giderek, terminalde 
        ◦ Cd  C://Users/…/Desktop masaüstüne kopyalıyoruz
    • Projelerde ortak paketler ve paket sürümleri kullanılmayacak ise virtualenv kurulmalıdır ;
        ◦ Pip install virtualenv
    • Sanal ortamı oluşturmak için ;
        ◦ Python3 –m venv myenv
    • Sanal oratamı aktifleştirmek için;
        ◦ Source myenv/bin/activate
    • Sanal ortamı  aktifleştirdek sonra kurulumları yapmamız gerekiyor.
    • Sanal ortamı kapatmak için ;
        ◦ Deactivate yazılmalı terminale
    • Django kurulumu;
        ◦ Windows için;
            ▪ Easy_install django(==sürüm) (parantez içi kulanılmazsa en son sürüm kurulur)
        ◦ Linux için;
            ▪ Pip install django(==sürüm)
    • Django sürüm sorgulama;
        ◦ Django-admin –version
    • Django ile proje oluşturma;
        ◦ Django-admin startproject (proje adı)
    • Manage.py;
        ◦ Bu dosyayı asla silmeyin, İstisnai durumlar haricinde düzenlemeyin kısaca bu dosyayı yok sayın. Bu dosya bir UI(Kullanıcı Arayüzü) dosyasıdır.Veri Tabanına erişim sağlamak, web site için kullanıcı oluşturmak gibi işlevleri yapmamızı sağlar
    • __init__.py;
        ◦ Python’ın dosyanın bulunduğu dizinin bir python paketi olduğunu belirtir . İçerisi genelde boş bırakılır.
    • Settings.py;
        ◦ Web sitesi ile ilgili ayarlamaların yapıldığı dosyamızdır. Dosyanın içeriğini kullanıkça açılayacağız.
    • Urls.py;
        ◦ Bir web sitesine girgiğimizde fomainden sonra gidilecek olan sayfanın adını belirlenmesinde, başka bir deyişle sayfanın adresinin belirlenmesini sağlar
    • wsgi.py;
        ◦ Bir web sunucusunun Ağ geçidi arayüzünü sağlıyor. Özel bir web sunucusu türü.
    •  Bu dosyalar projeyi oluşturduktan sonra pek bir değşiklik yapmadan kullanıyoruz.
    • Server’ı çalıştırmak için ;
        ◦ Python 2 için;
            ▪ Python manage.py runserver (isteğe bağlı port numarası)
        ◦ Python 3 için
            ▪ ./manage.py  runserver (isteğe bağlı port numarası)
    • Bizi direkt Django’nun test yapısından geçirerek  eğer projede sıkıntı yoksa proje çalışcak ve web sayfasına 127.0.0.0:8000 adresinde sitemiz çalışacak
    • Django’da app(uygulama) oluşturma;
        ◦ ./manage.py startapp (app adı)
    • Apps içeriği;
        ◦ Migrations  dizini;
            ▪ Web sitemizin tüm kaynak kodunu bağlayar bu dizin 
        ◦ __init.py__;
            ▪ Bu dizinin bir Python dizini olduğunu veya paketi olduğunu belirtir 
        ◦ Admin.py;
            ▪ Bu dosaya ile her web sitesinde olduğu gibi yönetici sayfası vardır ve bu ayarlamaların yapıldığı yerler vardır(Silmek, eklemek, aramak, bilgi almak ) bu ayarlamaların yapıldığı sayfadır.
        ◦ App.py;
            ▪ Yapılandırma ayarlarının olduğu sayfadır ve bu ayarlamaları Django App’i oluşturduğumuzda otomatik oluşturur.
        ◦ Models.py;
            ▪ Veri Tabanımızın nasıl şekil alacağını , verileri nasıl saklayacağımızı hangi tabloları depolamak istediğimize karar verdiğimiz dosya 
        ◦ Tests.py;
            ▪ Kodumuzda hata olup olmadığından emin olmak için bir dizi ufak kod parçaları buraya yazarak test ediyoruz.
        ◦ Views.py;
            ▪ Web sayfasından talepler gelir ve bu taleplerin bir html dosyasına gönderilir. Python fonksiyonları; cevap için, oturum açmak için , bir şey indirmek için ya da yanıt almak için yazılarak bu isteklere cevap verilen dosya.
    • Server çalıştırıldığında (it Works sayfası)
        ◦ Bu sayfa çalıştığında  şuana kadar herşeyin düzgün yapıldığının belirtisidir
    • /admin  sayfasına girdiğimizde hata alacağız çünkü biz henüz veritabanı oluşturmadık
    • Urls.py’da IP adresini ya da alan adını belirteceğiz. Burada reguler expression(düzenli ifade) kullancağız . Eğer bilmiyorsanız internetten bakmanızı öneririm. Url’e bir şey yazarken bunun anlık durumu karşılaması değil ileriye dönük büyük bir proje olacağını düşünerek  yazmalıyız
    • url’e ^  işareti ile başlıyoruz ve bitirmek isteğimizde $ (dolar)  işareti ile bitiriyoruz.
    • url’deki name alanı zorunlu değil bunu genelde html yazarken bu url’e ad vererek çağırmak için kullanıyoruz.
    • HttpResponse içerisine herhangi bir metin ya da html kodu yazılabilir.
    • Django kurulumu ile birlikte bize veritabanı olarak varsayılan sqlite3  sunuyor . Bütün ayarlamaları yapılı bir şekilde bize sunulmuş ama biz bunu değiştirebiliriz. Yaklaşık 77 tane veritabanı ile çalışabiliyoruz bunlardan en çok kullanıla  MySql PostreSql  ‘dir

    • INSTALLED_APPS;
        ◦ Burası bize Django kurulumu ile birlikte bir çok uygulama sunuyor; Yönetici , Kimlik doğrulama, Oturum mesajları, İçerik türleri ve bizde kendi oluşturduğumuz uygulamaları buraya ekleyerek projeye dahil edeceğiz
    • Migrate;
        ◦ Yaptığımız değişiklikleri ya da yazdığımız kodun senkronize bir şekilde veritabanına  uygulatmak için kullanıyoruz.
    • Models.py;
        ◦ Verilerimizi nasıl saklamak istediğimizin bir  planıdır. Bir model’den diğerine miras alabiliriz
    • Django ID numarasını otomatik olarak atar bunun için bizim Class’larımızda id atamamıza gerek yoktur.
    • Tabloları oluşturup veri tabanına yansıtmak 
        ◦ ./manage.py makemigrations (isteğe bağlı app adı)
            ▪ App adı yazılırsa şayet saedce o app tablolarını oluşturur geri  kalanlar oluşturulmaz
    • Oluşturulan tabloların  Sql ifade  olarak görmek için ;
        ◦ ./manage.py sqlmigrate (app adı) (makemigreations dosya adı (0001))
    • Veri tabanında (models’te) yeni tablolar oluşturulduktan sonra veya herhangi bir değişik yapıldıktan sonra makemigrations  ve  migrate komutları çalıştırılır. 
    • Shell bir etkileşim modudur. 
        ◦ Etkileşim mod; Etkin bellekte önceden beslenen ifadeleri çalıştırırken her ifade için anında geri bildirim veren bir komuttur.
        ◦ Normal mod; Komut dosyasını ve bitmiş .py dosyalarının Python yorumlayıcısında çalıştırıldığı halidir.
    • Shell’e yazdığımız komutların geçici olmaması için save() ile mutlaka kaydetmemiz gerekiyor
    • Django  ID  atamasını kendi yapar ve benzersiz bir ID tutar. ID aynı zamanda PK(Primary Key)  olarak kullanılabilir.
    • Shell ‘de nesneleri tanımlarken bütün özelliklerini tanımlayabildiğimiz gibi boş bir nesne oluşturup özelliklerini sonradan doldurarak da kaydedebiliriz.
    • Veri tabanımızda verilerimiz nesne olarak bir dizi içerisinde tutuluyor ve içeriğini (istediğimiz özelliklerini) görebilmek için  modelde tablomuza __str__ fonksiyonu yazmalıyız.
    • Shell’de verilerimiz bellekte tutulduğu için models’ta yapılan her değişiklikten sonra mutlaka shell’den çıkış yaparak yeniden girdikten sonra veri sorgulamalarını yapmalıyız.
    • Nesnelerin içerisnde verileri sınıflandırarak ya da herhangi veriyi aramak için filter()  fonksiyonu kullanılır.
    • Django admin panelini hazır bir şekilde bizlere sunuyor tek yapmamız gereken bu panele giriş yapabilmek için kullanıcı oluşturmamız gerekiyor
        ◦ ./manage.py createsuperuser
    • Bir views görünüm için fonksiyonların bulunduğu bu fonksiyonların işlevlerinin ne olduğu belirlendiği alandı.Views’ta fonksiyonları html dosyaları ile bağlamalıyız ki oradaki görünümü elde edebilelim bunun içinde yazılan views’la html arasındaki bağlantıyı url ile sağlıyoruz.
    • Daha güzel bir görünüm ve anlaşılırlığı arttırmak için template ile kaynak kodları farklı yerlerde tutmalıyız.
    •  
