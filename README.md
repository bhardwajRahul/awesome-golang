# Awesome Go

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome libraries, tools, and resources for the Go programming language.

## Contents

- [Web Frameworks](#web-frameworks)
- [Database](#database)
- [Command Line Interface (CLI)](#command-line-interface-cli)
- [Configuration](#configuration)
- [Logging](#logging)
- [Testing](#testing)
- [Security](#security)
- [API and RPC](#api-and-rpc)
- [Tooling](#tooling)
- [Resources](#resources)
  - [Tutorials](#tutorials)
  - [Books](#books)
  - [Communities](#communities)

---

## Web Frameworks

*   [**Gin**](https://github.com/gin-gonic/gin) - Arguably the most popular and widely used Go web framework. Although it has a Martini-like API, it is extremely fast thanks to its Radix tree-based routing. It has a large community and a rich ecosystem of middleware. It is one of the safest starting points for new projects.
*   [**Fiber**](https://github.com/gofiber/fiber) - A framework that is extremely easy and enjoyable to use, strongly inspired by Express.js from the Node.js world. It is built on top of **`fasthttp`** instead of Go's standard `net/http` package, making it one of the fastest web frameworks available. It is very easy to adapt for developers with Express experience.
*   [**Echo**](https://github.com/labstack/echo) - Another popular high-performance, minimalist, and extensible framework. It features a powerful router, a rich set of middleware, and built-in support for template rendering. It is often mentioned alongside Gin and Fiber as one of the best minimalist frameworks.
*   [**Chi**](https://github.com/go-chi/chi) - Stands out for being lightweight, idiomatic, and composable. The biggest advantage of `chi` is its full compatibility with Go's standard `net/http` package. This means you can use existing `net/http`-compatible middleware without any changes. It is one of the frameworks most faithful to Go's philosophy.
*   [**Gorilla/Mux**](https://github.com/gorilla/mux) - One of the oldest and most established routers in Go. It is more of a powerful router and dispatcher than a full-fledged framework. It forms the basis of many large and legacy projects. It is known for its flexible routing rules and robustness. Although it is now community-managed, it is still very common.
*   
## Database

_ORM and Database Tools_

*   [GORM](https://github.com/go-gorm/gorm) - A developer-friendly, full-featured ORM library for Go.
*   [SQLx](https://github.com/jmoiron/sqlx) - A general-purpose SQL extension for Go that extends the standard `database/sql` package.
*   [ent](https://github.com/facebook/ent) - A simple yet powerful entity framework and ORM for Go.
*   [SQLBoiler](https://github.com/volatiletech/sqlboiler) - A lightning-fast ORM generator, tailor-made for you from your database schema.
*   [sqlc](https://sqlc.dev/)   - Compile SQL to type-safe code
*   [FluentSQL](https://github.com/JiveGroup/FluentSQL) -  flexible and powerful SQL string builder
  
_Database Drivers_

*   [**pgx**](https://github.com/jackc/pgx) (PostgreSQL) - A high-performance and full-featured driver and toolkit for PostgreSQL. It offers direct access to advanced PostgreSQL features (e.g., JSONB support) beyond the standard `database/sql` interface. It is the most recommended driver for modern projects.
*   [**go-sql-driver/mysql**](https://github.com/go-sql-driver/mysql) (MySQL) - The most popular, stable, and full-featured MySQL driver for Go's `database/sql` package. It forms the basis of almost all MySQL-based projects.
*   [**modernc.org/sqlite**](https://gitlab.com/cznic/sqlite) (SQLite) - A modern SQLite driver written in **pure Go** that does not require CGO. This feature makes cross-compilation extremely easy and eliminates external dependencies.
*   [**mattn/go-sqlite3**](https://github.com/mattn/go-sqlite3) (SQLite) - One of the oldest and most common `database/sql`-compatible drivers for SQLite3. It wraps the SQLite C library using `cgo`.
*   [**microsoft/go-mssql**](https://github.com/microsoft/go-mssql) (Microsoft SQL Server) - The official `database/sql`-compatible driver for Microsoft SQL Server.
*   [**lib/pq**](https://github.com/lib/pq) (PostgreSQL) - A long-established PostgreSQL driver written in pure Go. Although it is in maintenance mode, it is still used in many projects.
*   [**mongo-go-driver**](https://github.com/mongodb/mongo-go-driver) (MongoDB) - The official MongoDB driver for the Go language. It does not use the `database/sql` interface; it has its own rich and idiomatic API.
*   [**redis/go-redis**](https://github.com/redis/go-redis) (Redis) - The most popular, full-featured, and high-performance Redis client for Golang. It is the standard for interacting with this in-memory data store, which is also used as a database.
*   [**gocql/gocql**](https://github.com/gocql/gocql) (Cassandra) - The most widely used Go driver for Apache Cassandra. It is highly configurable and performance-oriented.
*   [**sijms/go-ora**](https://github.com/sijms/go-ora) (Oracle) - A driver for Oracle Database written in **pure Go**. Its biggest advantage is that it does not require annoying external dependencies like an Oracle Instant Client installation.

## Command Line Interface (CLI)

*   [Cobra](https://github.com/spf13/cobra) - A powerful library for creating modern Go CLI applications.
*   [urfave/cli](https://github.com/urfave/cli) - A simple, fast, and fun package for building command-line apps in Go.
*   [Bubble Tea](https://github.com/charmbracelet/bubbletea) - A Go framework for building terminal applications based on The Elm Architecture.
*   *...add others here...*

## Configuration
*   [**Viper**](https://github.com/spf13/viper) - The most powerful and full-featured configuration library in the Go ecosystem.
    *   Can read many file formats like JSON, YAML, TOML, .env, and Java properties.
    *   Automatically reads and binds environment variables.
    *   Can integrate command-line flags.
    *   Can perform live watching of configuration and reload changes.
    *   It is a "do-it-all" solution for almost all configuration needs.
*   [**koanf**](https://github.com/knadh/koanf) - A modern, lightweight, and highly modular alternative to Viper.
    *   Reads from files, environment variables, or remote sources like `etcd` through configurable "providers."
    *   Stands out with its flexible structure and clean API. It offers powerful features without the complexity of Viper.
*   [**godotenv**](https://github.com/joho/godotenv) - A very simple library that does one job very well: loading environment variables from `.env` files. It is often used to facilitate adherence to 12-factor app principles in development environments.
*   [**envconfig**](https://github.com/kelseyhightower/envconfig) - Popular especially for containerized and cloud-native applications. It has a single purpose: to populate a Go struct directly from environment variables. It is very simple and effective to use.
*   [**cleanenv**](https://github.com/ilyakaznacheev/cleanenv) - A configuration library that adopts "clean architecture" principles. It focuses on loading configuration from files and environment variables into a Go struct with clean and minimal code, using struct tags.

## Logging

*   [Zap](https://github.com/uber-go/zap) - A library for fast, structured, and leveled logging.
*   [Logrus](https://github.com/sirupsen/logrus) - Structured and pluggable logging for Go.
*   [zerolog](https://github.com/rs/zerolog) - A JSON logger that performs zero-allocation.

## Testing

*   [**Testify**](https://github.com/stretchr/testify) - The Swiss Army knife of the Go testing ecosystem. It is the most popular toolkit that enriches the standard `testing` package.
    *   `assert`: A rich set of assertions that allow the test to continue even if it fails (`assert.Equal(t, 1, 1)`).
    *   `require`: An assertion set that stops the test immediately (`t.Fatal`) when an assertion fails.
    *   `suite`: Facilitates setup and teardown logic by grouping tests within structs.
*   [**go-cmp**](https://github.com/google/go-cmp) - A library for safely comparing complex data structures (structs, slices, etc.) in tests. It stands out for being much safer and more configurable than `reflect.DeepEqual`.
*   **[testing](https://pkg.go.dev/testing)** - The foundation of everything. The core package that comes with the standard library, providing the ability to create sub-tests with `t.Run`, mark helper functions with `t.Helper`, and offering basic test structures (`*testing.T`).
*   [**GoMock**](https://github.com/uber-go/mock) - Developed by the Go team, this framework has become the standard for isolating dependencies in unit tests by generating mock implementations from interfaces. It automatically creates mocks with the `mockgen` tool.
*   [**gofakeit**](https://github.com/brianvoe/gofakeit) - An excellent library for programmatically generating tons of fake but realistic data for tests (names, addresses, UUIDs, credit card numbers, random texts, etc.).
*   [**sqlmock**](https://github.com/DATA-DOG/go-sqlmock) - Allows creating a fake SQL driver when testing code that uses `database/sql`, without needing a real database connection. It is used to mock database interactions.
*   [**testcontainers-go**](https://github.com/testcontainers/testcontainers-go) - Indispensable for integration tests. It allows for programmatically creating Docker containers (PostgreSQL, Redis, Kafka, etc.) during tests and automatically destroying them when the test is finished.
*   **[net/http/httptest](https://pkg.go.dev/net/http/httptest)** - The standard library's basic package for testing HTTP handlers, which allows for creating fake HTTP requests and running in-memory servers.
*   [**httpexpect**](https://github.com/gavv/httpexpect) - Built on top of `httptest`, this library allows for end-to-end testing of APIs with a fluent and BDD (Behavior-Driven Development) style syntax (`Expect().Status(http.StatusOK).JSON().Object()...`).

### Advanced and Specialized Tools

*   **Built-in Fuzzing (`testing.F`)** - Added to the standard library with Go 1.18, this is a powerful testing technique that automatically finds unexpected errors and edge cases by sending random inputs to a function.
*   [**Godog**](https://github.com/cucumber/godog) - Inspired by Cucumber, this is the most popular Behavior-Driven Development (BDD) framework for Go. It links test scenarios written in the `Given-When-Then` format to Go functions.
*   [**goleak**](https://github.com/uber-go/goleak) - A tool that ensures the cleanliness of tests by checking if any goroutines have been leaked after the tests have finished, especially in concurrent programs.

## Security
*   [**golang.org/x/crypto**](https://pkg.go.dev/golang.org/x/crypto) - Go's semi-standard cryptography library. The **[bcrypt](https://pkg.go.dev/golang.org/x/crypto/bcrypt)** package, in particular, is considered the industry standard for securely hashing passwords.
*   [**golang-jwt/jwt**](https://github.com/golang-jwt/jwt) - The most popular, full-featured library for creating, parsing, and validating JSON Web Tokens (JWT). It forms the basis of stateless authentication for APIs.
*   [**casbin**](https://github.com/casbin/casbin) - An extremely powerful and flexible authorization library. It supports many access control models like ACL, RBAC, and ABAC, and makes it easy to manage "who can do what to which resource."
*   [**oauth2**](https://pkg.go.dev/golang.org/x/oauth2) - Developed by the Go team, this is the core library for managing the client side of the OAuth 2.0 standard, used to implement features like "Sign in with Google/GitHub/Facebook."
*   **[crypto/*](https://pkg.go.dev/crypto)** - The set of packages in Go's standard library that provides all the basic building blocks for fundamental cryptographic operations (AES, RSA, SHA256, etc.).
*   [**lego**](https://github.com/go-acme/lego) - A library written in pure Go, used to automatically obtain and renew SSL/TLS certificates from Let's Encrypt and other ACME-based certificate authorities. It's great for automating HTTPS.
*   [**bluemonday**](https://github.com/microcosm-cc/bluemonday) - A powerful, policy-based HTML sanitizer used to clean user-submitted HTML input from malicious code (like XSS attacks).
*   **[crypto/tls](https://pkg.go.dev/crypto/tls)** - The standard library's core package that enables HTTPS and other secure network communications.
*   [**govulncheck**](https://pkg.go.dev/golang.org/x/vuln/cmd/govulncheck) - The Go team's official security tool. It scans your project's dependencies to detect packages with known vulnerabilities. It stands out by only reporting vulnerabilities that your code actually calls.
*   [**gosec**](https://github.com/securego/gosec) - A linting tool that statically analyzes Go source code to detect common security vulnerabilities like SQL injection, hardcoded credentials, and insecure blocks.
*   [**mkcert**](https://github.com/FiloSottile/mkcert) - A simple tool for creating valid and trusted TLS certificates for local development environments (like `localhost`). It helps you get rid of browser warnings when developing with HTTPS.

## API and RPC

*   [gRPC-go](https://github.com/grpc/grpc-go) - The official implementation of gRPC for Go. A high-performance RPC framework based on HTTP/2, developed by Google.
*   [Gin](https://github.com/gin-gonic/gin) - A very fast and popular HTTP web framework that uses Radix tree-based routing.
*   [Fiber](https://github.com/gofiber/fiber) - An easy-to-use and extremely fast web framework inspired by Express.js, built on `fasthttp`.
*   [Echo](https://github.com/labstack/echo) - A high-performance, minimalist, and extensible web framework that offers powerful templating and middleware support.
*   [chi](https://github.com/go-chi/chi) - A lightweight, idiomatic, and composable HTTP router that is fully compatible with `net/http`.
*   [gorilla/mux](https://github.com/gorilla/mux) - A powerful URL router and dispatcher for routing incoming requests to their target handlers. It has long been a cornerstone of the Go ecosystem.
*   [gqlgen](https://github.com/99designs/gqlgen) - A library that has become the standard for building GraphQL servers by generating type-safe Go code from a GraphQL schema.
*   [Twirp](https://github.com/twitchtv/twirp) - A Protobuf-based RPC framework developed by Twitch, which is simpler than gRPC and supports both JSON and Protobuf.
*   [gRPC-Gateway](https://github.com/grpc-ecosystem/grpc-gateway) - A plugin that automatically generates a RESTful JSON proxy for your gRPC services. It allows you to serve both RPC and REST APIs from a single gRPC definition.
*   [Go-kit](https://github.com/go-kit/kit) - A modular, composable programming toolkit for building distributed and robust microservices. It offers an architectural approach, not just a framework.
*   [go-zero](https://github.com/zeromicro/go-zero) - A full-featured framework for web and RPC, packed with code generation features. It is designed for high-concurrency scenarios.
*   [fasthttp](https://github.com/valyala/fasthttp) - A high-performance alternative to the standard `net/http`. It forms the basis of many frameworks like Fiber and is used for APIs where speed is critical.
*   [Hertz](https://github.com/cloudwego/hertz) - An HTTP framework developed by Bytedance, focusing on high performance, extensibility, and ease of use.
*   [Goa](https://github.com/goadesign/goa) - A framework that allows you to create APIs with a design-first approach. It generates code and documentation from your design.
*   [emicklei/go-restful](https://github.com/emicklei/go-restful) - A library designed for creating RESTful web services, inspired by Java frameworks like JAX-RS and Spring Framework.
*   [Kratos](https://github.com/go-kratos/kratos) - Developed by Bilibili, a microservice-oriented framework inspired by Go-kit, offering `gRPC` and `HTTP` as standards.
*   [gorilla/websocket](https://github.com/gorilla/websocket) - A full-featured and widely used WebSocket implementation for Go. It is indispensable for real-time APIs.
*   [rpcx](https://github.com/smallnest/rpcx) - A high-performance, distributed, and pluggable RPC service framework, similar to Alibaba's Dubbo.
*   [kitex](https://github.com/cloudwego/kitex) - A high-performance and extensible RPC framework developed by Bytedance, supporting Thrift and Protobuf.
*   **net/http** - Go's standard library. It provides the fundamental building blocks for creating powerful, production-ready APIs without any external dependencies. All other libraries either wrap it or offer an alternative to it.

## Tooling
*   [golangci-lint](https://github.com/golangci/golangci-lint) - An extremely fast and configurable "meta" linter that brings dozens of different linters under one roof. It has become the industry standard for enforcing code standards in Go projects.
*   [gopls](https://github.com/golang/tools/tree/master/gopls) - The official Language Server Protocol implementation developed by the Go team. It provides features like auto-completion, go-to-definition, and real-time error analysis in editors like VS Code, GoLand, and Vim.
*   [gofmt](https://pkg.go.dev/cmd/gofmt) - The tool that comes with Go's standard library, which automatically formats Go code according to the standard format. `goimports` is a superset of `gofmt` that also organizes `import` blocks.
*   [gosec](https://github.com/securego/gosec) - A static analysis tool that scans Go source code to detect known security vulnerabilities and common mistakes.
*   [revive](https://github.com/mgechev/revive) - A linter that is faster, more configurable, and more extensible than `golint`. It offers high performance, especially in CI/CD pipelines.
*   [delve](https://github.com/go-delve/delve) - The most popular and powerful full-featured debugger for the Go programming language.
*   [air](https://github.com/cosmtrek/air) - A live reload tool that automatically restarts the application when it detects a change in the code files. It incredibly speeds up the web development process.
*   [gops](https://github.com/google/gops) - A tool used to list currently running Go processes and get diagnostic information about them, such as memory and goroutines.
*   [testcontainers-go](https://github.com/testcontainers/testcontainers-go) - A library that automates test environments by programmatically creating and managing Docker containers (PostgreSQL, Redis, Kafka, etc.) for integration tests.
*   [GoMock](https://github.com/uber-go/mock) - A standard framework used to isolate dependencies in unit tests by generating mock implementations from interfaces.
*   [gofakeit](https://github.com/brianvoe/gofakeit) - A library that makes it easy to generate random and fake data (name, address, credit card, etc.) for tests.
*   [goreleaser](https://github.com/goreleaser/goreleaser) - A fantastic automation tool that compiles your Go projects for different operating systems and architectures, archives them, creates release notes, and publishes them to platforms like GitHub.
*   [gox](https://github.com/mitchellh/gox) - A simple, parallel-running cross-compilation tool for Go.
*   [swaggo/swag](https://github.com/swaggo/swag) - A tool that automatically generates Swagger 2.0 / OpenAPI documentation from Go code comments.
*   [oapi-codegen](https://github.com/deepmap/oapi-codegen) - A tool that generates Go server boilerplate and client code from an OpenAPI 3 specification. Ideal for design-first APIs.
*   [wire](https://github.com/google/wire) - A compile-time dependency injection tool that is automatic and less prone to errors.
*   [go-callvis](https://github.com/ofabry/go-callvis) - A tool that interactively visualizes the call graph of your Go program. Useful for understanding large projects.
*   [pprof](https://pkg.go.dev/net/http/pprof) - A profiling tool included in Go's standard library, used to analyze the CPU and memory profiles of a running application. It is usually visualized with `go tool pprof`.

---

### Tutorials

📚 Beginner and General Tutorials

*   [A Tour of Go](https://tour.golang.org/) – An interactive tour of the Go language.
*   [Go by Example](https://gobyexample.com/) – An introduction to the Go language with annotated examples.
*   [Go Cheat Sheet](https://github.com/a8m/go-lang-cheat-sheet) – A reference card for the Go language.
*   [Go Tutorials – JavaTpoint](https://www.javatpoint.com/go-tutorial) – Basic Go language tutorial.
*   [Go Tutorials – Tutorialspoint](https://www.tutorialspoint.com/go/index.htm)
*   [Learn Go in 7 Days](https://github.com/harrytran103/7_days_of_go) – Go for Node.js developers.
*   [1000+ Exercises for Go](https://github.com/inancgumus/learngo) – Learn Go with exercises.
*   [Learn Go with Tests](https://github.com/quii/learn-go-with-tests) – Learn Go with a TDD approach.

🔧 Web Development

*   [Build Web Application with Golang](https://github.com/astaxie/build-web-application-with-golang)
*   [Building and Testing a REST API in Go with Gorilla Mux & PostgreSQL](https://semaphoreci.com/community/tutorials/building-and-testing-a-rest-api-in-go-with-gorilla-mux-and-postgresql)
*   [Building Go Web Applications and Microservices Using Gin](https://semaphoreci.com/community/tutorials/building-go-web-applications-and-microservices-using-gin)
*   [How to Deploy a Go Web Application with Docker](https://semaphoreci.com/community/tutorials/how-to-deploy-a-go-web-application-with-docker)
*   [Simple Calculator with Go WebAssembly](https://tutorialedge.net/golang/go-webassembly-tutorial/)
*   [Go Examples 101](https://github.com/Hasan-Kilici/go-examples)
*   [Golang E-commerce Guide (Ponzu CMS)](https://snipcart.com/blog/golang-ecommerce-ponzu-cms-demo)

🗃️ Database & Cache

*   [Go Database/SQL Tutorial](http://go-database-sql.org/)
*   [Caching Slow Database Queries](https://medium.com/@rocketlaunchr.cloud/caching-slow-database-queries-1085d308a0c9)
*   [Canceling MySQL in Go](https://medium.com/@rocketlaunchr.cloud/canceling-mysql-in-go-827ed8f83b30)
*   [dbq vs sqlx vs GORM Benchmark](https://medium.com/@rocketlaunchr.cloud/how-to-benchmark-dbq-vs-sqlx-vs-gorm-e814caacecb5)

🛠️ Advanced, Performance, Security

*   [Guide to Structured Logging in Go](https://betterstack.com/community/guides/logging/logging-in-go/)
*   [Scaling Go Applications](https://betterstack.com/community/guides/scaling-go/)
*   [Role-Based Access Control (RBAC) Authorization in Golang](https://www.permit.io/blog/role-based-access-control-rbac-authorization-in-golang)
*   [Behavior-Driven Development (BDD) with Godog](https://semaphoreci.com/community/tutorials/how-to-use-godog-for-behavior-driven-development-in-go)
*   [Build your own Redis, Docker, Git, SQLite in Go!](https://app.codecrafters.io/tracks/go) – CodeCrafters hands-on tutorial.

🎮 Games and Graphics

*   [Game Development with Go](https://www.youtube.com/watch?v=9D4yH7e_ea8&list=PLDZujg-VgQlZUy1iCqBbe5faZLMkA3g2x) – Video series.
*   [Introduction to Go with WebAssembly](https://medium.com/@martinolsansky/webassembly-with-golang-is-fun-b243c0e34f02)
*   [Understanding Go Visually](https://dev.to/aurelievache/series/26234) – A visual tutorial for Go.

📦 Architectures & Design Patterns

*   [Go Design Patterns](https://github.com/shubhamzanwar/design-patterns)
*   [Go-Clean-Template](https://github.com/evrone/go-clean-template) – A clean architecture template.
*   [Hex Monscape](https://github.com/Haraj-backend/hex-monscape) – An introduction to Hexagonal architecture.
*   [Go Patterns](https://github.com/tmrts/go-patterns) – Commonly used structures and patterns.


👨‍💻 Learning Platforms

*   [YourBasic Go](https://yourbasic.org/golang) – Comprehensive tutorials.
*   [Hackr.io Tutorial for Go](https://hackr.io/tutorials/learn-golang) – The best tutorials selected by votes.
*   [FreeCodeCamp Tutorial for Golang](https://www.freecodecamp.org/news/golang-tutorial-list-free-courses-learn-go-programming-language/)
*   [Coursera: Programming with Google Go](https://www.coursera.org/specializations/google-golang)


🧩 Code Snippets & Examples

*   [golang-examples](https://github.com/SimonWaldherr/golang-examples)
*   [GopherSnippets](https://gophersnippets.com/)
*   [GopherCoding](https://gophercoding.com/)
*   [GoSamples](https://gosamples.dev/)
*   [Learning with Go](https://dev.to/aurelievache/learning-go-by-examples-introduction-448n)

---

### 🎥 YouTube & Video Content


*   [Awesome Go @LibHunt](https://go.libhunt.com) - A primary resource for Go tools.
*   [Awesome Golang Workshops](https://github.com/amit-davidson/awesome-golang-workshops) - A list of curated awesome Go workshops.
*   [Awesome Remote Jobs](https://github.com/lukasz-madon/awesome-remote-job) - A list of awesome remote work opportunities. Many are looking for Go developers.
*   [awesome-awesomeness](https://github.com/bayandin/awesome-awesomeness) - A list of other awesome lists.
*   [awesome-go-extra](https://github.com/xwjdsh/awesome-go-extra) - Parses the awesome-go README file and generates a new README with repository information.
*   [Code with Mukesh](https://codewithmukesh.com/categories/golang) - Blog posts from software engineer Mukesh.
*   [Coding Mystery](https://codingmystery.com) - Solve escape room style programming puzzles using Go.
*   [CodinGame](https://www.codingame.com/) - Learn Go through interactive tasks by playing small games.
*   [Go Blog](https://blog.golang.org) - The official Go blog.
*   [Go Code Club](https://www.youtube.com/watch?v=nvoIPQYdx9g&list=PLEcwzBXTPUE_YQR7R0BRtHBYJ0LN3Y0i3) - A developer community that discusses a different Go project each week.
*   [Go Community (Hashnode)](https://hashnode.com/n/go) - The Gopher community on Hashnode.
*   [Go Forum](https://forum.golangbridge.org) - A discussion forum on the Go language.
*   [Go Projects](https://github.com/golang/go/wiki/Projects) - A list of projects in the Go community wiki.
*   [Go Proverbs](https://go-proverbs.github.io/) - Go language proverbs compiled by Rob Pike.
*   [Go Report Card](https://goreportcard.com) - An automatic quality assessment tool for your Go package.
*   [go.dev](https://go.dev/) - The official hub for Go developers.
*   [gocryforhelp](https://github.com/ninedraft/gocryforhelp) - A collection of Go projects that need help. A good starting point for contributing to the open-source world.
*   [Golang Developer Jobs](https://golangjob.xyz) - A platform that lists only Go-related job postings.
*   [Golang News](https://golangnews.com) - Links and news related to the Go language.
*   [Golang Nugget](https://golangnugget.com) - A weekly summary of Go content delivered to your inbox every Monday.
*   [Golang Weekly](https://discu.eu/weekly/golang/) - Projects, tutorials, and articles about Go every Monday.
*   [golang-nuts](https://groups.google.com/forum/#!forum/golang-nuts) - The Go developer mailing list.
*   [Google Plus Community](https://plus.google.com/communities/114112804251407510571) - The Google+ community for #golang fans (may no longer be active).
*   [Gopher Community Slack Chat](https://invite.slack.golangbridge.org) - The Slack community for Gophers ([learn how it came to be](https://blog.gopheracademy.com/gophers-slack-community/)).
*   [Gophercises](https://gophercises.com/) - Free Go coding exercises for beginners.
*   [json2go](https://m-zajac.github.io/json2go) - An advanced JSON → Go struct conversion tool.
*   [justforfunc](https://www.youtube.com/c/justforfunc) - A YouTube channel on the Go language presented by Francesc Campoy ([@francesc](https://twitter.com/francesc)).
*   [Learn Go Programming](https://blog.learngoprogramming.com) - Learn Go concepts with visual explanations.
*   [Made with Golang](https://madewithgolang.com/?ref=awesome-go) - Discover projects made with Go.
*   [pkg.go.dev](https://pkg.go.dev/) - The documentation center for open-source Go packages.
*   [studygolang](https://studygolang.com) - An active Go community based in China.
*   [Trending Go repositories on GitHub today](https://github.com/trending?l=go) - A great resource for discovering new Go libraries.
*   [TutorialEdge - Golang](https://tutorialedge.net/course/golang/) - Tutorial content on Golang.

---

👥 Go for Developers of Other Languages

*   [Go for Node.js Developers](https://github.com/miguelmota/golang-for-nodejs-developers)


### Communities

*   [Go Forum](https://forum.golangbridge.org/) - The official forum for the Go community.
*   [Gophers Slack](https://gophers.slack.com/) - The largest Slack channel for Go developers.
---

## Contributing

Your contributions and suggestions are always welcome! Please follow these steps:

1.  **Fork** this project.
2.  Create a new branch with a name like `feature/new-awesome-thing`.
3.  Make your changes and **Commit** them (`git commit -m 'feat: Add a new awesome library'`).
4.  **Push** your branch (`git push origin feature/new-awesome-thing`).
5.  Open a **Pull Request**.
6. **Up A** [Reddit](https://www.reddit.com/r/golang/comments/1m7yj31/new_to_go_this_github_repo_is_the_ultimate/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button).
