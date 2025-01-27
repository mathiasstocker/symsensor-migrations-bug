# SymSensor/ActuatorDoctrineBundle

## Migrations bug reproduction steps

1. Clone this repository
2. `symfony composer install`
3. `docker compose up -d`
4. `symfony console doctrine:migrations:migrate`
5. `symfony server:start -d`
6. `Open [https://localhost:8000/_actuator/health](https://localhost:8000/_actuator/health)`
7. doctrine-migrations status is "DOWN" - but we ran the migrations in step 4
