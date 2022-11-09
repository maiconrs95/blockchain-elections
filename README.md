# blockchain-elections

A simple elections webapp with blockchain

# Starting

> You must have docker, docker compose, Java 8 and node installed in your setup. I personaly use [asdf](https://asdf-vm.com/guide/introduction.html) to manage my tools version.

- Run docker compose to initialize MySQL `docker compose up -d`
- Run java server `java -Dspring.datasource.username={{user}} -Dspring.datasource.password={{password}} -jar webapp-runner.jar --port 8080 --expand-war eleicoesonline.war`
- Access `http://localhost:8080/magic/generate/roles` to generate roles
- Access `http://localhost:8080/magic/generate/owner` to generate owners
- Run docker compose to initialize sawtooth `docker-compose -f sawtooth-default.yaml up`
- Install node deps and run blockchain server in `./app/blockchain-api` - `npm i && node index.js`
