
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

*   [Fiber](https://github.com/gofiber/fiber) - Express.js'ten esinlenilmiş, Fasthttp üzerine kurulmuş yüksek performanslı bir web çatısı.
*   [Gin](https://github.com/gin-gonic/gin) - Martini benzeri bir API'ye sahip, yüksek performanslı bir web çatısı.
*   [Echo](https://github.com/labstack/echo) - Yüksek performanslı, minimalist ve genişletilebilir bir Go web çatısı.
*   *...diğerlerini buraya ekleyin...*

## Veritabanı (Database)

_ORM ve Veritabanı Araçları_

*   [GORM](https://github.com/go-gorm/gorm) - Go için geliştirici dostu, tam özellikli bir ORM kütüphanesi.
*   [SQLx](https://github.com/jmoiron/sqlx) - Standart `database/sql` paketini genişleten, Go için genel amaçlı bir SQL uzantısı.
*   [ent](https://github.com/facebook/ent) - Go için basit ama güçlü bir varlık (entity) çatısı ve ORM.
*   [SQLBoiler](https://github.com/volatiletech/sqlboiler) - Veritabanı şemanızdan sizin için özel olarak hazırlanmış, oldukça hızlı bir ORM üreteci.
*   *...diğerlerini buraya ekleyin...*

_Veritabanı Sürücüleri_

*   [pgx](https://github.com/jackc/pgx) - PostgreSQL için yüksek performanslı ve tam özellikli bir sürücü ve araç takımı.
*   [go-sql-driver/mysql](https://github.com/go-sql-driver/mysql) - Go için bir MySQL sürücüsü.
*   [mongo-go-driver](https://github.com/mongodb/mongo-go-driver) - Go dili için resmi MongoDB sürücüsü.
*   [go-redis](https://github.com/redis/go-redis) - Golang için Redis istemcisi.
*   *...diğerlerini buraya ekleyin...*

## Komut Satırı Arayüzü (CLI)

*   [Cobra](https://github.com/spf13/cobra) - Modern Go CLI uygulamaları oluşturmak için güçlü bir kütüphane.
*   [urfave/cli](https://github.com/urfave/cli) - Go'da komut satırı uygulamaları oluşturmak için basit, hızlı ve eğlenceli bir paket.
*   [Bubble Tea](https://github.com/charmbracelet/bubbletea) - The Elm Architecture tabanlı, terminal uygulamaları oluşturmak için bir Go çatısı.
*   *...diğerlerini buraya ekleyin...*

## Yapılandırma (Configuration)

*   [Viper](https://github.com/spf13/viper) - Dişli bir Go yapılandırma yöneticisi. Dosyalardan, ortam değişkenlerinden ve daha fazlasından okuma yapar.
*   [godotenv](https://github.com/joho/godotenv) - `.env` dosyalarından ortam değişkenlerini yüklemek için kullanılır.
*   [koanf](https://github.com/knadh/koanf) - Hafif ve genişletilebilir yapılandırma okuma kütüphanesi.
*   *...diğerlerini buraya ekleyin...*

## Loglama (Logging)

*   [Zap](https://github.com/uber-go/zap) - Hızlı, yapısal ve seviyeli loglama için bir kütüphane.
*   [Logrus](https://github.com/sirupsen/logrus) - Go için yapısal ve tak-çıkar (pluggable) loglama.
*   [zerolog](https://github.com/rs/zerolog) - Sıfır bellek tahsisatı (zero-allocation) yapan bir JSON logger.
*   *...diğerlerini buraya ekleyin...*

## Test (Testing)

*   [Testify](https://github.com/stretchr/testify) - Go standart kütüphanesini tamamlayan, test için yardımcı araçlar ve assertion'lar sunar.
*   [GoMock](https://github.com/uber-go/mock) - Go programlama dili için bir mock oluşturma çatısı.
*   [go-cmp](https://github.com/google/go-cmp) - Testlerde Go değerlerini karşılaştırmak için kullanılan bir paket.
*   [testcontainers-go](https://github.com/testcontainers/testcontainers-go) - Otomatik entegrasyon testleri için konteyner tabanlı bağımlılıkları oluşturmayı basitleştirir.
*   *...diğerlerini buraya ekleyin...*

## Güvenlik (Security)

*   [golang-jwt/jwt](https://github.com/golang-jwt/jwt) - JSON Web Token'ları (JWT) oluşturmak ve doğrulamak için tam özellikli bir implementasyon.
*   [bcrypt](https://golang.org/x/crypto/bcrypt) - Şifreleri güvenli bir şekilde hash'lemek için kullanılır.
*   [lego](https://github.com/go-acme/lego) - Let's Encrypt için saf Go ile yazılmış bir ACME istemci kütüphanesi.
*   *...diğerlerini buraya ekleyin...*

## API ve RPC

*   [gRPC-go](https://github.com/grpc/grpc-go) - Go için gRPC'nin resmi implementasyonu. HTTP/2 tabanlı RPC.
*   [chi](https://github.com/go-chi/chi) - `net/context` üzerine kurulu küçük, hızlı ve etkileyici bir HTTP router'ı.
*   [gorilla/mux](https://github.com/gorilla/mux) - Golang için güçlü bir URL router ve dağıtıcı.
*   [rpcx](https://github.com/smallnest/rpcx) - Alibaba Dubbo gibi dağıtık ve takılabilir bir RPC servis çatısı.
*   *...diğerlerini buraya ekleyin...*

## Araçlar (Tooling)

*   [golangci-lint](https://github.com/golangci/golangci-lint) - Hızlı, paralel çalışan, birden çok linter'ı birleştiren bir araç.
*   [air](https://github.com/cosmtrek/air) - Go için canlı yeniden yükleme (live reload) aracı.
*   [goreleaser](https://github.com/goreleaser/goreleaser) - Go ile yazılmış programları hızlı ve kolay bir şekilde dağıtmak için kullanılır.
*   [delve](https://github.com/derekparker/delve) - Go için bir hata ayıklayıcı (debugger).
*   *...diğerlerini buraya ekleyin...*

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
