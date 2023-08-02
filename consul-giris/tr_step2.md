# HashiCorp - Consul
Bir Önceki adımda Consul'un daha iyi anlaşılabilmesi için bilmemiz gereken kavramlardan söz ettik. Şimdi ise Consul Nedir, Ne İçin Kullanılır?, Consul Özellikleri Nelerdir?, Consul'un Mimarisi ve Bileşenleri gibi konu başlıklarını açıklayacağız. 
## 1- Consul Nedir, Ne İçin Kullanılır?
Consul diğer adıyla Consul Service Discovery, HashiCorp şirketi tarafından geliştirilmiş konfigürasyon yönetimi ve network segmentation işlevleri ile tam özellikli bir kontrol paneli sağlayan service mesh çözümüdür. 
## 2- Consul Özellikleri Nelerdir?
**a) Service Discovery:** Consul'un clientları API ya da MySQL gibi servisleri register edebilir ve diğer clientlar da Consul'u verilen servisin sağlayıcılarını keşfetmek için kullanılabilir. DNS veya HTTP kullanarak, uygulamalar bağlı oldukları servisleri kolayca bulabilirler.
**b) Health Checking:** Operator tarafından clusterın sağlığını monitoring etmek için kullanılmaktadaır. Ayrıca servis discovery componentleri tarafından sağlıksız hostlara trafiğin yönlendirilmemesi için de kullanılmaktadır.
**c) KV Store:** Uygulamalar, Consul'un Key/Value Store'undan dynamic configuration, feature flagging, coordination ve leader election gibi pek çok amaç için faydanılabilmektedir.
**d) Secure Service Communication:** Consul servislerin Mutual TLS Connection'ı kurabilmeleri için TLS sertifikaları oluşturup servislere dağıtılabilir. 'Intensions' hangi servislerin iletişim kurmasına izin verildiğini tanımlamak için kullanılmaktadır. Complex Network Topology'leri ve static firewall ruleları yerine gerçek zamanlı değişeilen 'Intensions' sayesinde 'Service Segmentation' kolayca yönetilebilir.
**e) Multi Datacenter:** Consul, Multiple Datacenterları desteklemektedir. Diğer bir değişle, Consul kullanıcılarının birden fazla bölgede büyümek için ek soyutlama katmanları oluşturma konusunda endişelenmemeleri gerektiği anlamına gelmektedir.
## 3- Consul'un Mimarisi ve Bileşenleri
Consul; agentlar, serverlar ve clientlar olmak üzere üç ana bileşenden oluşan dağıtılmış bir sistemdir.

**Agentler:** Consul'un temel yapı taşıdır. Consul clusterındaki her node'un çalışan bir agenti olmalıdır.Agent şunlardan sorumludur:
○ Consul ile kayıt hizmetleri
○ Keşif hizmetleri
○ Healtcheck hizmetleri
○ Verilerin KV deposunda saklanması

**Sunucular:** Temel Consul işlevselliği için gereklidir. Sunucu şunlardan sorumludur:
○ Consul statusünü saklama ve çoğaltma
○ Cluster için bir lider seçmek
○ Uygulamalarınız için bir DNS hizmeti sağlamak

**İstemciler:** İstemci, Consul hizmetiyle etkileşim kurmak için kullanılır. İstemciler, şunları yapabilir;
○ Hizmetleri keşfedin
○ Hizmetlerin sağlığını kontrol edin
○ Verileri KV deposunda saklayın


-> *HashiCorp - Consul eğitimimizin 1. adımını tamamladık. Consul kurulumunu gerçekleştirebileceğimiz 2. adıma geçebilirsiniz.*