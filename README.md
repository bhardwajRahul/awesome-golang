
# Awesome Go 

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Go programlama dili için harika kütüphanelerin, araçların ve kaynakların seçilmiş bir listesi.

## İçindekiler

- [Web Çatıları (Web Frameworks)](#web-çatıları-web-frameworks)
- [Veritabanı (Database)](#veritabanı-database)
- [Komut Satırı Arayüzü (CLI)](#komut-satırı-arayüzü-cli)
- [Yapılandırma (Configuration)](#yapılandırma-configuration)
- [Loglama (Logging)](#loglama-logging)
- [Test (Testing)](#test-testing)
- [Güvenlik (Security)](#güvenlik-security)
- [API ve RPC](#api-ve-rpc)
- [Araçlar (Tooling)](#araçlar-tooling)
- [Kaynaklar (Resources)](#kaynaklar-resources)
  - [Öğreticiler (Tutorials)](#öğreticiler-tutorials)
  - [Kitaplar (Books)](#kitaplar-books)
  - [Topluluklar (Communities)](#topluluklar-communities)

---


## Web Çatıları (Web Frameworks)

*   [**Gin**](https://github.com/gin-gonic/gin) - Muhtemelen en popüler ve yaygın olarak kullanılan Go web çatısıdır. Martini benzeri bir API'ye sahip olmasına rağmen, Radix ağacı tabanlı yönlendirme (Radix tree routing) sayesinde son derece hızlıdır. Geniş bir topluluğa ve zengin bir ara katman (middleware) ekosistemine sahiptir. Yeni projeler için en güvenli başlangıç noktalarından biridir.
*   [**Fiber**](https://github.com/gofiber/fiber) - Node.js dünyasındaki Express.js'ten güçlü bir şekilde esinlenmiş, kullanımı son derece kolay ve keyifli bir çatı. Go'nun standart `net/http` paketi yerine, **`fasthttp`** üzerine kurulmuştur, bu da onu en hızlı web çatılarından biri yapar. Express tecrübesi olan geliştiriciler için adaptasyonu çok kolaydır.
*   [**Echo**](https://github.com/labstack/echo) - Yüksek performanslı, minimalist ve genişletilebilir bir diğer popüler çatı. Güçlü bir yönlendiriciye, zengin bir ara katman setine ve yerleşik şablon oluşturma (template rendering) desteğine sahiptir. Genellikle Gin ve Fiber ile birlikte en iyi minimalist çatılardan biri olarak anılır.
*   [**Chi**](https://github.com/go-chi/chi) - Hafif, deyimsel (idiomatic) ve birleştirilebilir (composable) olmasıyla öne çıkar. `chi`'nin en büyük avantajı, Go'nun standart `net/http` paketiyle tam uyumlu olmasıdır. Bu, ekosistemdeki mevcut `net/http` uyumlu ara katmanları hiçbir değişiklik yapmadan kullanabileceğiniz anlamına gelir. Go'nun felsefesine en sadık çatılardan biridir.
*   [**Gorilla/Mux**](https://github.com/gorilla/mux) - Go'daki en eski ve en köklü yönlendiricilerden (router) biridir. Tam bir çatıdan çok, güçlü bir yönlendirici ve dağıtıcıdır. Çok büyük ve eski projelerin temelini oluşturur. Esnek yönlendirme kuralları ve sağlamlığı ile bilinir. Artık topluluk tarafından yönetilse de hala çok yaygındır.
*   [**Revel**](https://github.com/revel/revel) - Minimalist çatılardan farklı olarak, "her şey dahil" (batteries-included) bir yaklaşım sunan tam yığın (full-stack) bir web çatısıdır. Kendi şablon motoru, yönlendiricisi ve test çatısıyla gelir. Kod üretimi ve "hot-reload" gibi özellikleriyle, Ruby on Rails veya Django gibi çatılara daha çok benzer.

## Veritabanı (Database)

_ORM ve Veritabanı Araçları_

*   [GORM](https://github.com/go-gorm/gorm) - Go için geliştirici dostu, tam özellikli bir ORM kütüphanesi.
*   [SQLx](https://github.com/jmoiron/sqlx) - Standart `database/sql` paketini genişleten, Go için genel amaçlı bir SQL uzantısı.
*   [ent](https://github.com/facebook/ent) - Go için basit ama güçlü bir varlık (entity) çatısı ve ORM.
*   [SQLBoiler](https://github.com/volatiletech/sqlboiler) - Veritabanı şemanızdan sizin için özel olarak hazırlanmış, oldukça hızlı bir ORM üreteci.

_Veritabanı Sürücüleri_

*   [**pgx**](https://github.com/jackc/pgx) (PostgreSQL) - PostgreSQL için yüksek performanslı ve tam özellikli bir sürücü ve araç takımı. Standart `database/sql` arayüzünün ötesinde gelişmiş PostgreSQL özelliklerine (örneğin, JSONB desteği) doğrudan erişim sunar. Modern projeler için en çok tavsiye edilen sürücüdür.
*   [**go-sql-driver/mysql**](https://github.com/go-sql-driver/mysql) (MySQL) - Go'nun `database/sql` paketi için en popüler, kararlı ve tam özellikli MySQL sürücüsü. Neredeyse tüm MySQL tabanlı projelerin temelini oluşturur.
*   [**modernc.org/sqlite**](https://gitlab.com/cznic/sqlite) (SQLite) - CGO gerektirmeyen, **saf Go (pure Go)** ile yazılmış modern bir SQLite sürücüsü. Bu özelliği sayesinde çapraz derlemeyi (cross-compilation) son derece kolaylaştırır ve harici bağımlılıkları ortadan kaldırır.
*   [**mattn/go-sqlite3**](https://github.com/mattn/go-sqlite3) (SQLite) - SQLite3 için `database/sql` uyumlu, en eski ve yaygın sürücülerden biridir. SQLite C kütüphanesini `cgo` kullanarak sarmalar.
*   [**microsoft/go-mssql**](https://github.com/microsoft/go-mssql) (Microsoft SQL Server) - Microsoft SQL Server için `database/sql` ile uyumlu resmi sürücü.
*   [**lib/pq**](https://github.com/lib/pq) (PostgreSQL) - Saf Go (pure Go) ile yazılmış, uzun süredir standart olarak kabul edilen bir PostgreSQL sürücüsü. Bakım modunda olmasına rağmen hala çok sayıda projede kullanılmaktadır.
*   [**mongo-go-driver**](https://github.com/mongodb/mongo-go-driver) (MongoDB) - Go dili için resmi MongoDB sürücüsü. `database/sql` arayüzünü kullanmaz; kendine özgü, zengin ve deyimsel (idiomatic) bir API'si vardır.
*   [**redis/go-redis**](https://github.com/redis/go-redis) (Redis) - Golang için en popüler, tam özellikli ve yüksek performanslı Redis istemcisi. Veritabanı olarak da kullanılan bu bellek-içi (in-memory) veri deposuyla etkileşim için standarttır.
*   [**gocql/gocql**](https://github.com/gocql/gocql) (Cassandra) - Apache Cassandra için en yaygın kullanılan Go sürücüsü. Yüksek düzeyde yapılandırılabilir ve performans odaklıdır.
*   [**sijms/go-ora**](https://github.com/sijms/go-ora) (Oracle) - Oracle Database için **saf Go** ile yazılmış bir sürücü. Oracle Instant Client kurulumu gibi can sıkıcı harici bağımlılıklara ihtiyaç duymaması en büyük avantajıdır.

## Komut Satırı Arayüzü (CLI)

*   [Cobra](https://github.com/spf13/cobra) - Modern Go CLI uygulamaları oluşturmak için güçlü bir kütüphane.
*   [urfave/cli](https://github.com/urfave/cli) - Go'da komut satırı uygulamaları oluşturmak için basit, hızlı ve eğlenceli bir paket.
*   [Bubble Tea](https://github.com/charmbracelet/bubbletea) - The Elm Architecture tabanlı, terminal uygulamaları oluşturmak için bir Go çatısı.
*   *...diğerlerini buraya ekleyin...*

## Yapılandırma (Configuration)
*   [**Viper**](https://github.com/spf13/viper) - Go ekosistemindeki en güçlü ve tam özellikli yapılandırma kütüphanesi.
    *   JSON, YAML, TOML, .env ve Java properties gibi birçok dosya formatını okuyabilir.
    *   Ortam değişkenlerini otomatik olarak okur ve bağlar.
    *   Komut satırı bayraklarını entegre edebilir.
    *   Yapılandırmayı canlı olarak izleyebilir (live watching) ve değişiklikleri yeniden yükleyebilir.
    *   Neredeyse tüm yapılandırma ihtiyaçları için "her şeyi yapan" bir çözümdür.
*   [**koanf**](https://github.com/knadh/koanf) - Viper'a modern, hafif ve son derece modüler bir alternatif.
    *   Yapılandırılabilir "sağlayıcılar" (providers) aracılığıyla dosyalardan, ortam değişkenlerinden veya `etcd` gibi uzak kaynaklardan okuma yapar.
    *   Esnek yapısı ve temiz API'si ile öne çıkar. Viper'ın getirdiği karmaşıklık olmadan güçlü özellikler sunar.
*   [**godotenv**](https://github.com/joho/godotenv) - Çok basit ve tek bir işi çok iyi yapan bir kütüphane: `.env` dosyalarından ortam değişkenlerini yüklemek. Genellikle geliştirme ortamlarında 12-factor app prensiplerine uymayı kolaylaştırmak için kullanılır.
*   [**envconfig**](https://github.com/kelseyhightower/envconfig) - Özellikle konteynerize edilmiş ve bulut tabanlı (cloud-native) uygulamalar için popülerdir. Tek bir amacı vardır: Ortam değişkenlerini doğrudan bir Go struct'ına doldurmak. Kullanımı çok basit ve etkilidir.
*   [**cleanenv**](https://github.com/ilyakaznacheev/cleanenv) - "Temiz mimari" (clean architecture) prensiplerini benimseyen bir yapılandırma kütüphanesi. Dosyalardan ve ortam değişkenlerinden gelen yapılandırmayı, struct etiketleri (tags) kullanarak temiz ve az kodla bir Go struct'ına yüklemeye odaklanır.
*   
## Loglama (Logging)

*   [Zap](https://github.com/uber-go/zap) - Hızlı, yapısal ve seviyeli loglama için bir kütüphane.
*   [Logrus](https://github.com/sirupsen/logrus) - Go için yapısal ve tak-çıkar (pluggable) loglama.
*   [zerolog](https://github.com/rs/zerolog) - Sıfır bellek tahsisatı (zero-allocation) yapan bir JSON logger.

## Test (Testing)

*   [**Testify**](https://github.com/stretchr/testify) - Go test ekosisteminin İsviçre çakısı. Standart `testing` paketini zenginleştiren en popüler araç takımıdır.
    *   `assert`: Testin başarısız olsa bile devam etmesini sağlayan zengin bir assertion seti (`assert.Equal(t, 1, 1)`).
    *   `require`: Bir assertion başarısız olduğunda testi anında durduran (`t.Fatal`) assertion seti.
    *   `suite`: Testleri yapılar (structs) içinde gruplayarak kurulum (setup) ve söküm (teardown) mantığını kolaylaştırır.
*   [**go-cmp**](https://github.com/google/go-cmp) - Karmaşık veri yapılarının (struct, slice vb.) testlerde güvenli bir şekilde karşılaştırılmasını sağlayan bir kütüphane. `reflect.DeepEqual`'a göre çok daha güvenli ve yapılandırılabilir olmasıyla öne çıkar.
*   **[testing](https://pkg.go.dev/testing)** - Her şeyin temeli. Standart kütüphaneyle gelen, `t.Run` ile alt testler oluşturmayı, `t.Helper` ile yardımcı fonksiyonları işaretlemeyi ve temel test yapılarını (`*testing.T`) sunan çekirdek paket.
*   [**GoMock**](https://github.com/uber-go/mock) - Go ekibi tarafından geliştirilen, arayüzlerden (interface) sahte (mock) implementasyonlar üreten, birim testlerinde bağımlılıkları izole etmek için standart haline gelmiş bir çatı. `mockgen` aracı ile mock'ları otomatik olarak oluşturur.
*   [**gofakeit**](https://github.com/brianvoe/gofakeit) - Testler için programatik olarak tonlarca sahte ama gerçekçi veri (isimler, adresler, UUID'ler, kredi kartı numaraları, rastgele metinler vb.) oluşturmayı sağlayan harika bir kütüphane.
*   [**sqlmock**](https://github.com/DATA-DOG/go-sqlmock) - `database/sql` kullanan kodları test ederken, gerçek bir veritabanı bağlantısına ihtiyaç duymadan sahte SQL sürücüsü oluşturmayı sağlar. Veritabanı etkileşimlerini taklit etmek için kullanılır.
*   [**testcontainers-go**](https://github.com/testcontainers/testcontainers-go) - Entegrasyon testlerinin vazgeçilmezi. Testler sırasında programatik olarak Docker konteynerleri (PostgreSQL, Redis, Kafka vb.) oluşturup, test bittiğinde otomatik olarak yok etmeyi sağlar.
*   **[net/http/httptest](https://pkg.go.dev/net/http/httptest)** - Standart kütüphanenin HTTP işleyicilerini (handler) test etmek için sunduğu, sahte HTTP istekleri oluşturmayı ve bellek-içi sunucular (in-memory server) çalıştırmayı sağlayan temel paket.
*   [**httpexpect**](https://github.com/gavv/httpexpect) - `httptest` üzerine kurulmuş, API'lerin uçtan uca testini akıcı (fluent) ve BDD (Davranış Odaklı Geliştirme) tarzı bir söz dizimiyle yapmayı sağlayan bir kütüphane (`Expect().Status(http.StatusOK).JSON().Object()...`).

### İleri Seviye ve Uzmanlık Araçları

*   **Yerleşik Fuzzing (`testing.F`)** - Go 1.18 ile standart kütüphaneye eklenen, bir fonksiyona rastgele girdiler göndererek beklenmedik hataları ve kenar durumları (edge cases) otomatik olarak bulan güçlü bir test tekniğidir.
*   [**Godog**](https://github.com/cucumber/godog) - Cucumber'dan esinlenilmiş, Go için en popüler Davranış Odaklı Geliştirme (BDD) çatısıdır. `Given-When-Then` formatında yazılan test senaryolarını Go fonksiyonlarına bağlar.
*   [**goleak**](https://github.com/uber-go/goleak) - Özellikle eşzamanlı (concurrent) programlarda, testlerin bittiğinde arkada sızdırılmış (leaked) goroutine'ler bırakıp bırakmadığını kontrol eden, testlerin temizliğini garanti altına alan bir araç.
## Güvenlik (Security)
*   [**golang.org/x/crypto**](https://pkg.go.dev/golang.org/x/crypto) - Go'nun yarı-standart kriptografi kütüphanesi. Özellikle **[bcrypt](https://pkg.go.dev/golang.org/x/crypto/bcrypt)** paketi, şifreleri güvenli bir şekilde hash'lemek için endüstri standardı olarak kabul edilir.
*   [**golang-jwt/jwt**](https://github.com/golang-jwt/jwt) - JSON Web Token'ları (JWT) oluşturmak, ayrıştırmak ve doğrulamak için en popüler, tam özellikli kütüphane. API'ler için durum bilgisi tutmayan (stateless) kimlik doğrulamanın temelini oluşturur.
*   [**casbin**](https://github.com/casbin/casbin) - Son derece güçlü ve esnek bir yetkilendirme (authorization) kütüphanesi. ACL, RBAC, ABAC gibi birçok erişim kontrol modelini destekler ve "kimin, hangi kaynağa, ne yapabileceğini" yönetmeyi kolaylaştırır.
*   [**oauth2**](https://pkg.go.dev/golang.org/x/oauth2) - Go ekibi tarafından geliştirilen, "Google/GitHub/Facebook ile giriş yap" gibi özellikleri uygulamak için kullanılan, OAuth 2.0 standardının istemci (client) tarafını yöneten temel kütüphane.
*   **[crypto/*](https://pkg.go.dev/crypto)** - Go'nun standart kütüphanesinde yer alan ve temel kriptografik işlemler (AES, RSA, SHA256 vb.) için gereken tüm temel yapı taşlarını sunan paketler bütünü.
*   [**lego**](https://github.com/go-acme/lego) - Let's Encrypt ve diğer ACME tabanlı sertifika otoritelerinden otomatik olarak SSL/TLS sertifikaları almak ve yenilemek için kullanılan, saf Go ile yazılmış bir kütüphane. HTTPS'i otomatikleştirmek için harikadır.
*   [**bluemonday**](https://github.com/microcosm-cc/bluemonday) - Kullanıcılardan gelen HTML girdilerini zararlı kodlardan (XSS atakları gibi) arındırmak için kullanılan, güçlü ve politika tabanlı bir HTML temizleyici (sanitizer).
*   **[crypto/tls](https://pkg.go.dev/crypto/tls)** - Standart kütüphanenin HTTPS ve diğer güvenli ağ iletişimlerini sağlayan temel paketi.
*   [**govulncheck**](https://pkg.go.dev/golang.org/x/vuln/cmd/govulncheck) - Go ekibinin resmi güvenlik aracı. Projenizin bağımlılıklarını tarayarak bilinen güvenlik açıkları (vulnerability) içeren paketleri tespit eder. Sadece kodunuzun gerçekten çağırdığı zafiyetleri raporlamasıyla öne çıkar.
*   [**gosec**](https://github.com/securego/gosec) - Go kaynak kodunu statik olarak analiz ederek SQL enjeksiyonu, sabit kodlanmış kimlik bilgileri (hardcoded credentials), güvensiz bloklar gibi yaygın güvenlik açıklarını tespit eden bir linting aracı.
*   [**mkcert**](https://github.com/FiloSottile/mkcert) - Yerel geliştirme ortamı için (`localhost` gibi) geçerli ve güvenilir TLS sertifikaları oluşturmayı sağlayan basit bir araç. HTTPS ile geliştirme yaparken tarayıcı uyarılarından kurtulmanızı sağlar.

## API ve RPC

*   [gRPC-go](https://github.com/grpc/grpc-go) - Go için gRPC'nin resmi implementasyonu. Google tarafından geliştirilen, HTTP/2 tabanlı yüksek performanslı bir RPC çatısı.
*   [Gin](https://github.com/gin-gonic/gin) - Radix ağacı tabanlı yönlendirme kullanan, oldukça hızlı ve popüler bir HTTP web çatısı.
*   [Fiber](https://github.com/gofiber/fiber) - Express.js'ten esinlenilmiş, `fasthttp` üzerine kurulmuş, kullanımı kolay ve son derece hızlı bir web çatısı.
*   [Echo](https://github.com/labstack/echo) - Yüksek performanslı, minimalist ve genişletilebilir, güçlü bir şablonlama ve ara katman (middleware) desteği sunan bir web çatısı.
*   [chi](https://github.com/go-chi/chi) - `net/http` ile tam uyumlu, hafif, deyimsel (idiomatic) ve birleştirilebilir bir HTTP router'ı.
*   [gorilla/mux](https://github.com/gorilla/mux) - Gelen istekleri hedeflenen işleyicilere yönlendirmek için güçlü bir URL router ve dağıtıcı. Uzun süredir Go ekosisteminin temel taşlarından biridir.
*   [gqlgen](https://github.com/99designs/gqlgen) - Bir GraphQL şemasından yola çıkarak tür-güvenli (type-safe) Go kodu üreten, GraphQL sunucuları oluşturmak için standart haline gelmiş bir kütüphane.
*   [Twirp](https://github.com/twitchtv/twirp) - Twitch tarafından geliştirilen, Protobuf tabanlı, gRPC'ye göre daha basit, hem JSON hem de Protobuf destekli bir RPC çatısı.
*   [gRPC-Gateway](https://github.com/grpc-ecosystem/grpc-gateway) - gRPC servisleriniz için otomatik olarak bir RESTful JSON proxy'si oluşturan bir eklenti. Tek bir gRPC tanımıyla hem RPC hem de REST API sunmanızı sağlar.
*   [Go-kit](https://github.com/go-kit/kit) - Dağıtık ve sağlam mikroservisler oluşturmak için modüler, birleştirilebilir bir programlama araç takımı. Sadece bir çatı değil, bir mimari yaklaşımı sunar.
*   [go-zero](https://github.com/zeromicro/go-zero) - Kod üretimi özellikleriyle dolu, web ve RPC için tam özellikli bir çatı. Yüksek eşzamanlılık (concurrency) senaryoları için tasarlanmıştır.
*   [fasthttp](https://github.com/valyala/fasthttp) - Standart `net/http`'ye yüksek performanslı bir alternatif. Fiber gibi birçok çatının temelini oluşturur ve hızın kritik olduğu API'ler için kullanılır.
*   [Hertz](https://github.com/cloudwego/hertz) - Bytedance tarafından geliştirilen, yüksek performans, genişletilebilirlik ve kullanımı kolaylaştırmaya odaklanan bir HTTP çatısı.
*   [Goa](https://github.com/goadesign/goa) - Tasarım öncelikli (design-first) bir yaklaşımla API'ler oluşturmanızı sağlayan bir çatı. Tasarımınızdan kod ve dokümantasyon üretir.
*   [emicklei/go-restful](https://github.com/emicklei/go-restful) - JAX-RS ve Spring Framework gibi Java çatılarından esinlenen, RESTful web servisleri oluşturmak için tasarlanmış bir kütüphane.
*   [Kratos](https://github.com/go-kratos/kratos) - Bilibili tarafından geliştirilen, mikroservis odaklı, Go-kit'ten ilham alan, `gRPC` ve `HTTP`'yi standart olarak sunan bir çatı.
*   [gorilla/websocket](https://github.com/gorilla/websocket) - Go için tam özellikli ve geniş çapta kullanılan bir WebSocket implementasyonu. Gerçek zamanlı API'ler için vazgeçilmezdir.
*   [rpcx](https://github.com/smallnest/rpcx) - Yüksek performanslı, dağıtık ve tak-çıkar (pluggable) özelliklere sahip, Alibaba Dubbo gibi bir RPC servis çatısı.
*   [kitex](https://github.com/cloudwego/kitex) - Bytedance tarafından geliştirilen, Thrift ve Protobuf'u destekleyen yüksek performanslı ve genişletilebilir bir RPC çatısı.
*   **net/http** - Go'nun standart kütüphanesi. Hiçbir harici bağımlılık olmadan güçlü, üretime hazır API'ler oluşturmak için temel yapı taşlarını sunar. Diğer tüm kütüphaneler ya onu sarmalar ya da ona bir alternatif sunar.
*   

## Araçlar (Tooling)
*   [golangci-lint](https://github.com/golangci/golangci-lint) - Onlarca farklı linter'ı tek bir çatı altında toplayan, son derece hızlı ve yapılandırılabilir bir "meta" linter. Go projelerinde kod standartlarını zorunlu kılmak için endüstri standardı haline gelmiştir.
*   [gopls](https://github.com/golang/tools/tree/master/gopls) - Go ekibi tarafından geliştirilen resmi Dil Sunucusu Protokolü (Language Server Protocol) implementasyonu. VS Code, GoLand, Vim gibi editörlerde otomatik tamamlama, tanıma gitme (go-to-definition) ve anlık hata analizi gibi özellikleri sağlar.
*   [gofmt](https://pkg.go.dev/cmd/gofmt) - Go'nun standart kütüphanesiyle gelen, Go kodunu standart formata göre otomatik olarak biçimlendiren araç. `goimports` ise `gofmt`'nin `import` bloklarını da organize eden bir üst sürümüdür.
*   [gosec](https://github.com/securego/gosec) - Go kaynak kodunu tarayarak bilinen güvenlik açıklarını ve yaygın yapılan hataları tespit eden bir statik analiz aracı.
*   [revive](https://github.com/mgechev/revive) - `golint`'e göre daha hızlı, yapılandırılabilir ve genişletilebilir bir linter. Özellikle CI/CD süreçlerinde yüksek performans sunar.
*   [delve](https://github.com/go-delve/delve) - Go programlama dili için tam özellikli, en popüler ve güçlü hata ayıklayıcı (debugger).
*   [air](https://github.com/cosmtrek/air) - Kod dosyalarında bir değişiklik algıladığında uygulamayı otomatik olarak yeniden başlatan, canlı yeniden yükleme (live reload) aracı. Web geliştirme sürecini inanılmaz hızlandırır.
*   [gops](https://github.com/google/gops) - O an çalışan Go süreçlerini listelemek ve onlar hakkında bellek, goroutine gibi tanılama bilgileri almak için kullanılan bir araç.
*   [testcontainers-go](https://github.com/testcontainers/testcontainers-go) - Entegrasyon testleri için programatik olarak Docker konteynerleri (PostgreSQL, Redis, Kafka vb.) oluşturup yönetmeyi sağlayan, test ortamlarını otomatikleştiren bir kütüphane.
*   [GoMock](https://github.com/uber-go/mock) - Arayüzlerden (interface) sahte (mock) implementasyonlar üreten, birim testlerinde bağımlılıkları izole etmek için kullanılan standart bir çatı.
*   [gofakeit](https://github.com/brianvoe/gofakeit) - Testler için rastgele ve sahte veriler (isim, adres, kredi kartı vb.) oluşturmayı kolaylaştıran bir kütüphane.
*   [goreleaser](https://github.com/goreleaser/goreleaser) - Go projelerinizi farklı işletim sistemleri ve mimariler için derleyen, arşivleyen, sürüm notları oluşturan ve GitHub gibi platformlara yayınlayan harika bir otomasyon aracı.
*   [gox](https://github.com/mitchellh/gox) - Go için basit, paralel çalışan bir çapraz derleme (cross-compilation) aracı.
*   [swaggo/swag](https://github.com/swaggo/swag) - Go kod yorumlarından yola çıkarak otomatik olarak Swagger 2.0 / OpenAPI dokümantasyonu üreten bir araç.
*   [oapi-codegen](https://github.com/deepmap/oapi-codegen) - OpenAPI 3 spesifikasyonundan yola çıkarak Go için sunucu iskeleti (server boilerplate) ve istemci (client) kodu üreten bir araç. Tasarım öncelikli (design-first) API'ler için idealdir.
*   [wire](https://github.com/google/wire) - Derleme zamanında çalışan, otomatik ve hataya daha az açık bir bağımlılık enjeksiyonu (dependency injection) aracı.
*   [go-callvis](https://github.com/ofabry/go-callvis) - Go programınızdaki çağrı grafiğini (call graph) interaktif bir şekilde görselleştiren bir araç. Büyük projeleri anlamak için kullanışlıdır.
*   [pprof](https://pkg.go.dev/net/http/pprof) - Go'nun standart kütüphanesinde bulunan, çalışan bir uygulamanın CPU ve bellek profillerini analiz etmek için kullanılan bir profil oluşturma aracıdır. Genellikle `go tool pprof` ile görselleştirilir.
*   
---


### Öğreticiler (Tutorials)

📚 Başlangıç ve Genel Eğitimler

* [Go Turu](https://tour.golang.org/) – Etkileşimli bir Go dili turu.
* [Go Örneklerle](https://gobyexample.com/) – Açıklamalı örneklerle Go diline giriş.
* [Go Hile Kartı](https://github.com/a8m/go-lang-cheat-sheet) – Go dili için referans kartı.
* [Go Eğitimleri – JavaTpoint](https://www.javatpoint.com/go-tutorial) – Temel Go dil eğitimi.
* [Go Eğitimleri – Tutorialspoint](https://www.tutorialspoint.com/go/index.htm)
* [Go’yu 7 Günde Öğren](https://github.com/harrytran103/7_days_of_go) – Node.js geliştiricileri için Go.
* [Go için 1000+ Alıştırma](https://github.com/inancgumus/learngo) – Alıştırmalarla Go öğrenin.
* [Go ile Test Güdümlü Geliştirme (TDD)](https://github.com/quii/learn-go-with-tests) – TDD yaklaşımıyla Go öğrenin.

🔧 Web Geliştirme

* [Go ile Web Uygulaması Geliştirme](https://github.com/astaxie/build-web-application-with-golang)
* [Gorilla Mux & PostgreSQL ile REST API](https://semaphoreci.com/community/tutorials/building-and-testing-a-rest-api-in-go-with-gorilla-mux-and-postgresql)
* [Gin ile Web Uygulaması & Mikroservis](https://semaphoreci.com/community/tutorials/building-go-web-applications-and-microservices-using-gin)
* [Go ile Docker Kullanımı](https://semaphoreci.com/community/tutorials/how-to-deploy-a-go-web-application-with-docker)
* [Go WebAssembly ile Basit Hesap Makinesi](https://tutorialedge.net/golang/go-webassembly-tutorial/)
* [Go Örnek 101](https://github.com/Hasan-Kilici/go-examples)
* [Golang E-Ticaret Rehberi (Ponzu CMS)](https://snipcart.com/blog/golang-ecommerce-ponzu-cms-demo)

🗃️ Veri Tabanı & Cache

* [Go Database/SQL Eğitimi](http://go-database-sql.org/)
* [Yavaş Sorgular için Cache](https://medium.com/@rocketlaunchr.cloud/caching-slow-database-queries-1085d308a0c9)
* [MySQL Sorgularını İptal Etme](https://medium.com/@rocketlaunchr.cloud/canceling-mysql-in-go-827ed8f83b30)
* [dbq vs sqlx vs GORM Karşılaştırması](https://medium.com/@rocketlaunchr.cloud/how-to-benchmark-dbq-vs-sqlx-vs-gorm-e814caacecb5)

🛠️ İleri Seviye, Performans, Güvenlik

* [Go’da Yapısal Loglama Rehberi](https://betterstack.com/community/guides/logging/logging-in-go/)
* [Go Uygulamalarını Ölçeklendirme](https://betterstack.com/community/guides/scaling-go/)
* [Rol Tabanlı Yetkilendirme (RBAC)](https://www.permit.io/blog/role-based-access-control-rbac-authorization-in-golang)
* [Davranış Odaklı Geliştirme (BDD) – Godog ile](https://semaphoreci.com/community/tutorials/how-to-use-godog-for-behavior-driven-development-in-go)
* [Go ile Redis, Docker, Git, SQLite yaz!](https://app.codecrafters.io/tracks/go) – CodeCrafters uygulamalı eğitim.

🎮 Oyun ve Görsellik

* [Go ile Oyun Geliştirme](https://www.youtube.com/watch?v=9D4yH7e_ea8&list=PLDZujg-VgQlZUy1iCqBbe5faZLMkA3g2x) – Video serisi.
* [WebAssembly ile Go Giriş](https://medium.com/@martinolsansky/webassembly-with-golang-is-fun-b243c0e34f02)
* [Go’yu Görsel Anlamak](https://dev.to/aurelievache/series/26234) – Görsellerle Go öğretisi.

📦 Mimariler & Tasarım Desenleri

* [Go Tasarım Desenleri](https://github.com/shubhamzanwar/design-patterns)
* [Go-Clean-Template](https://github.com/evrone/go-clean-template) – Temiz mimari şablonu.
* [Hex Monscape](https://github.com/Haraj-backend/hex-monscape) – Hexagonal mimariye giriş.
* [Go Patterns](https://github.com/tmrts/go-patterns) – Sık kullanılan yapı ve desenler.


 👨‍💻 Öğrenme Platformları

* [YourBasic Go](https://yourbasic.org/golang) – Kapsamlı öğreticiler.
* [Go için Hackr.io Eğitimi](https://hackr.io/tutorials/learn-golang) – Oylarla seçilmiş en iyi eğitimler.
* [Golang için FreeCodeCamp Eğitimi](https://www.freecodecamp.org/news/golang-tutorial-list-free-courses-learn-go-programming-language/)
* [Coursera: Google Go ile Programlama](https://www.coursera.org/specializations/google-golang)


 🧩 Kod Parçacıkları & Örnekler

* [golang-examples](https://github.com/SimonWaldherr/golang-examples)
* [GopherSnippets](https://gophersnippets.com/)
* [GopherCoding](https://gophercoding.com/)
* [GoSamples](https://gosamples.dev/)
* [Go ile Öğrenmek](https://dev.to/aurelievache/learning-go-by-examples-introduction-448n)

---

### 🎥 YouTube & Video İçerikler


* [Awesome Go @LibHunt](https://go.libhunt.com) - Go araçları için başvurabileceğiniz temel kaynak.
* [Harika Golang Atölyeleri](https://github.com/amit-davidson/awesome-golang-workshops) - Özenle seçilmiş harika Go atölyeleri listesi.
* [Harika Uzaktan İşler](https://github.com/lukasz-madon/awesome-remote-job) - Harika uzaktan çalışma fırsatları listesi. Birçoğu Go geliştiricisi arıyor.
* [awesome-awesomeness](https://github.com/bayandin/awesome-awesomeness) - Diğer harika listelerin listesi.
* [awesome-go-extra](https://github.com/xwjdsh/awesome-go-extra) - awesome-go README dosyasını ayrıştırır ve havuz bilgileriyle yeni bir README oluşturur.
* [Code with Mukesh](https://codewithmukesh.com/categories/golang) - Yazılım mühendisi Mukesh’in blog yazıları.
* [Coding Mystery](https://codingmystery.com) - Go kullanarak kaçış odası tarzı programlama bulmacaları çözün.
* [CodinGame](https://www.codingame.com/) - Küçük oyunlar üzerinden etkileşimli görevlerle Go öğrenin.
* [Go Blog](https://blog.golang.org) - Resmi Go blogu.
* [Go Code Club](https://www.youtube.com/watch?v=nvoIPQYdx9g&list=PLEcwzBXTPUE_YQR7R0BRtHBYJ0LN3Y0i3) - Her hafta farklı bir Go projesini tartışan geliştirici topluluğu.
* [Go Topluluğu (Hashnode)](https://hashnode.com/n/go) - Hashnode üzerindeki Gopher topluluğu.
* [Go Forum](https://forum.golangbridge.org) - Go dili üzerine tartışma forumu.
* [Go Projeleri](https://github.com/golang/go/wiki/Projects) - Go topluluk vikisindeki projeler listesi.
* [Go Özdeyişleri](https://go-proverbs.github.io/) - Rob Pike tarafından derlenen Go dili özdeyişleri.
* [Go Karnesi](https://goreportcard.com) - Go paketiniz için otomatik kalite değerlendirme aracı.
* [go.dev](https://go.dev/) - Go geliştiricileri için resmi merkez.
* [gocryforhelp](https://github.com/ninedraft/gocryforhelp) - Yardıma ihtiyaç duyan Go projeleri koleksiyonu. Açık kaynak dünyasına katkı için iyi bir başlangıç noktası.
* [Golang Geliştirici İşleri](https://golangjob.xyz) - Yalnızca Go ile ilgili iş ilanlarını listeleyen platform.
* [Golang Haberleri](https://golangnews.com) - Go dili ile ilgili bağlantılar ve haberler.
* [Golang Nugget](https://golangnugget.com) - Her pazartesi gelen kutunuza gelen haftalık Go içerik özeti.
* [Golang Weekly](https://discu.eu/weekly/golang/) - Her pazartesi Go hakkında projeler, eğitimler ve makaleler.
* [golang-nuts](https://groups.google.com/forum/#!forum/golang-nuts) - Go geliştirici e-posta grubu.
* [Google Plus Topluluğu](https://plus.google.com/communities/114112804251407510571) - #golang hayranları için Google+ topluluğu (artık aktif olmayabilir).
* [Gopher Topluluğu Slack Sohbeti](https://invite.slack.golangbridge.org) - Gophers için Slack topluluğu ([nasıl ortaya çıktığını öğrenin](https://blog.gopheracademy.com/gophers-slack-community/)).
* [Gophercises](https://gophercises.com/) - Yeni başlayanlar için ücretsiz Go kodlama egzersizleri.
* [json2go](https://m-zajac.github.io/json2go) - Gelişmiş JSON → Go struct dönüşüm aracı.
* [justforfunc](https://www.youtube.com/c/justforfunc) - Francesc Campoy tarafından sunulan Go dili üzerine YouTube kanalı ([@francesc](https://twitter.com/francesc)).
* [Go Programlama Öğren](https://blog.learngoprogramming.com) - Görselli anlatımlarla Go kavramları öğrenin.
* [Made with Golang](https://madewithgolang.com/?ref=awesome-go) - Go ile yapılmış projeleri keşfedin.
* [pkg.go.dev](https://pkg.go.dev/) - Açık kaynak Go paketlerinin dokümantasyon merkezi.
* [studygolang](https://studygolang.com) - Çin merkezli aktif bir Go topluluğu.
* [Bugün GitHub’da trend olan Go depoları](https://github.com/trending?l=go) - Yeni Go kütüphaneleri keşfetmek için güzel bir kaynak.
* [TutorialEdge - Golang](https://tutorialedge.net/course/golang/) - Golang üzerine eğitim içeriği.

---

👥 Diğer Dil Geliştiricileri için Go

* [Node.js Geliştiricileri için Go](https://github.com/miguelmota/golang-for-nodejs-developers)


### Topluluklar (Communities)

*   [Go Forum](https://forum.golangbridge.org/) - Go topluluğu için resmi forum.
*   [Gophers Slack](https://gophers.slack.com/) - Go geliştiricileri için en büyük Slack kanalı.
---

## Katkıda Bulunma (Contributing)

Katkılarınız ve önerileriniz her zaman kabul edilir! Lütfen şu adımları izleyin:

1.  Bu projeyi **Fork**'layın.
2.  `feature/yeni-harika-sey` gibi bir isimle yeni bir branch oluşturun.
3.  Değişikliklerinizi yapın ve **Commit**'leyin (`git commit -m 'feat: Yeni bir harika kütüphane ekle'`).
4.  Branch'inizi **Push**'layın (`git push origin feature/yeni-harika-sey`).
5.  Bir **Pull Request** açın.
