# AltyapiServer

### Hakkında ###
Metin2 Sıfırdan Altyapı Server Files Hazırlama Rehberini hazırlarken kullandığım dosyalar.                                                                                       
Rehbere bakmak isterseniz: https://www.mmotutkunlari.com/konu/metin2-sifirdan-altyapi-server-files-hazirlama-rehberi.7141

### Nasıl Kurulur? ####
Şuan için bu dosyalar Freebsd 12.1 veya 11.x ile build edilmektedir.
#### Kurulması Gereken Paketler ####
* mysql80-client
* mysql80-server
* openssl
* python
* git
* gcc9
* gmake
* makedepend
* subversion

Paketleri kurduktan sonra kaynak kodlarını build etmeye başlayabilirsiniz.                                                                                                       
Sırayla şu komutları uygulayın.                                                                                                                                                   
Ana dizine gidin.
> cd /

Eğer home klasörü yoksa şu komut ile oluşturun.
> mkdir /home

Kaynak kodlarını git ile çekin.
> git clone https://github.com/MMOTutkunlari/AltyapiServer.git

Extern dosyalarını çıkartın.
> cd /home/AltyapiServer/Srcs/                                                                                                                                                   
> tar -zxf Extern-server-freebsd-12.tgz

Cryptopp'u build edin. (-j aynı anda ne kadar dosya build edecegini belirtir.)
> cd /home/AltyapServer/Srcs/Extern/cryptopp                                                                                                                                     
> gmake -j6                                                                                                                                                                       
> mv libcryptopp.a ../lib                                                                                                                                                         

Server source build edin. (-j aynı anda ne kadar dosya build edecegini belirtir.)
> cd /home/AltyapiServer/Srcs/Server                                                                                                                                             
> gmake all -j6

### Sonra neler yapacağım? ###
Daha sonra server files ve clienti oluşturmanız gerekiyor. 
> Client: https://github.com/MMOTutkunlari/AltyapiClient                                                                                                                         
> ServerFiles: https://github.com/MMOTutkunlari/AltyapiSF

Aklınıza takılan sorular olursa sitemize gelip sormaktan çekinmeyiniz. :)                                                                                                         
www.mmotutkunlari.com | Whistle