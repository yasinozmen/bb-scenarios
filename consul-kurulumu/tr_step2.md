### 2- Consul Service Agent Nedir? Neden Kullanılır?
Consul Service Agent, HashiCorp tarafından geliştirilen bir hizmet keşfi ve yönetim aracıdır. Consul Service Agent, aşağıdaki görevleri yerine getirir:
**1) Service Discovery:** Consul'un clientları API ya da MySQL gibi servisleri register edebilir ve diğer clientlar da Consul'u verilen servisin sağlayıcılarını keşfetmek için kullanılabilir. DNS veya HTTP kullanarak, uygulamalar bağlı oldukları servisleri kolayca bulabilirler.
**2) Health Checking:** Operator tarafından clusterın sağlığını monitoring etmek için kullanılmaktadaır. Ayrıca servis discovery componentleri tarafından sağlıksız hostlara trafiğin yönlendirilmemesi için de kullanılmaktadır.
**3) KV Store:** Uygulamalar, Consul'un Key/Value Store'undan dynamic configuration, feature flagging, coordination ve leader election gibi pek çok amaç için faydanılabilmektedir.
**4) Secure Service Communication:** Consul servislerin Mutual TLS Connection'ı kurabilmeleri için TLS sertifikaları oluşturup servislere dağıtılabilir. 'Intensions' hangi servislerin iletişim kurmasına izin verildiğini tanımlamak için kullanılmaktadır. Complex Network Topology'leri ve static firewall ruleları yerine gerçek zamanlı değişeilen 'Intensions' sayesinde 'Service Segmentation' kolayca yönetilebilir.
**5) Multi Datacenter:** Consul, Multiple Datacenterları desteklemektedir. Diğer bir değişle, Consul kullanıcılarının birden fazla bölgede büyümek için ek soyutlama katmanları oluşturma konusunda endişelenmemeleri gerektiği anlamına gelmektedir.

Kısaca özetlemek gerekirse, Consul Service Agent dağıtık sistemlerde hizmetlerin keşfedilmesi, izlenmesi ve yönetilmesi için kullanılan bir yazılımdır.

-> Consul Service Agent'in nasıl kullanıldığını öğreneceğimiz sonraki adıma geçebilirsiniz.