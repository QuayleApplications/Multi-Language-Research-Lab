## How to Run Experiments (Docker)

Replace `{question}` with the folder name for this question and `{n}` with the experiment number.

```bash
# PHP 8.3
docker compose run --rm php83 php PHP/{question}/lab/concept_experiments/experiment_{n}.php

# PHP 8.1
docker compose run --rm php81 php PHP/{question}/lab/concept_experiments/experiment_{n}.php

# PHP 7.4
docker compose run --rm php74 php PHP/{question}/lab/concept_experiments/experiment_{n}.php

# Bash
docker compose run --rm bash bash Bash/{question}/lab/concept_experiments/experiment_{n}.sh

# C++
docker compose run --rm cpp bash -c "cd Cplusplus/{question}/lab/concept_experiments && g++ experiment_{n}.cpp -o main && ./main"

# C#
docker compose run --rm csharp dotnet run --project Csharp/{question}/lab/concept_experiments/experiment_{n}.csproj

# Go
docker compose run --rm go go run Go/{question}/lab/concept_experiments/experiment_{n}.go

# Java  (assuming class name = Experiment_{n})
docker compose run --rm java bash -c "cd Java/{question}/lab/concept_experiments && javac Experiment_{n}.java && java Experiment_{n}"

# JavaScript
docker compose run --rm javascript node JavaScript/{question}/lab/concept_experiments/experiment_{n}.js

# NodeJS
docker compose run --rm nodejs node NodeJS/{question}/lab/concept_experiments/experiment_{n}.js

# Python
docker compose run --rm python python Python/{question}/lab/concept_experiments/experiment_{n}.py

# Rust (Cargo project in concept_experiments/)
docker compose run --rm rust bash -c "cd Rust/{question}/lab/concept_experiments && cargo run"

# MySQL (start server once, then connect)
docker compose up -d mysql
docker compose run --rm mysql mysql -h mysql -urigor -prigor rigor

# SQL (SQLite)
docker compose run --rm sql sqlite3 SQL/{question}/lab/concept_experiments/experiment_{n}.db \
  < SQL/{question}/lab/concept_experiments/experiment_{n}.sql
