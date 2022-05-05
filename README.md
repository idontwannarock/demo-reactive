Demo project of Reactive service comparing Servlet service with K6 load test plus visualization with Grafana.

## Pre-requisite

- docker compose
- JDK 11+

## TL;DR

### Start Docker containers

```bash
docker compose up -d postgres influxdb grafana
```

And open `https://localhost:3000` in a browser.

### Run project

Windows

```batch
.\mvnw.cmd spring-boot:run
```

Linux or MacOS

```bash
./mvnw spring-boot:run
```

### Run tests

Run reactive service test

```bash
docker compose run k6 run /scripts/test-reactive.js
```

Run servlet service test

```bash
docker compose run k6 run /scripts/test-block.js
```

