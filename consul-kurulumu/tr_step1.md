# HashiCorp - Consul
Consul eğitimimizin 2. senaryosunda Consul yazılımının makinamıza nasıl kurulduğunu ve servis ajanının nasıl başlatıldığını öğreneceğiz.
### 1-Consul Server Kurulumu
Consul yazılımımızın kurulumuna başlamadan önce Ubuntu paket yöneticisini güncellememiz gerekiyor. Bunun için aşağıdaki komutları sırası ile çalıştırın:

`apt-get update -y`

Consul kurulumunda ihtiyacımız olan paketleri aşağıdaki komudu kullanarak kurun:

`apt-get install unzip gnupg2 curl wget -y`

Bir sonraki adıma geçmeden önce, yukarıdaki komudun bileşenlerini inceleyelim:
- **apt-get:** Ubuntu tabanlı Linux dağıtımlarında paket yöneticisi olan APT aracını kullanır.
- **unzip:** ZIP dosyalarını çıkarmak için kullanılır.
- **gnupg2:** GNU Privcy Guard adlı açık kaynaklı bir şifreleme yazılımıdır.
- **curl:** Komut satırından URL'leri kullanarak veri alışverişi yapmaya yarayan bir araçtır.
- **wget:** İnternet üzerinden dosya indirmek için kullanılır.
- **-y:** İşlem sırasında herhangi bir onay istenmeden paketleri otomatik olarak kurmayı sağlayan bir seçenektir.

Gerekli paketlerin kurulumları tamamlandıktan sonra Consul yazılımının son versiyonunu alalım:

`wget https://releases.hashicorp.com/consul/1.8.4/consul_1.8.4_linux_amd64.zip`

Kurulum tamamlandıktan sonra dosyayı açalım:

`unzip consul_1.8.4_linux_amd64.zip`

Sonrasında consul dosyasını */usr/local/bin/* adresine taşıyalım:

`mv consul /usr/local/bin/`

Dosya taşıma işlemini tammaladıktan sonra artık consul yazılımını kullanmaya hazıırız. (Consul yazılımının kurulduğundan emin olmak istiyorsanız `consul --version`komutunu kullanabilirsiniz.)

-> Consul ile kullanılan Service Agent'in ne olduğunu ve neden kullanıldığını öğreneceğimiz sonraki adıma geçebilirsiniz.
