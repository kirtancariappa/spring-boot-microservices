# Spring Boot Microservices Sample Project

This project demonstrates two Spring Boot microservices:
- Currency Exchange Service
- Currency Conversion Service

## Services

### 1. currency-exchange-sample-service
Runs on port 8000. Provides exchange rates.

### 2. currency-conversion-sample-service
Runs on port 8100. Calls exchange service to calculate converted currency.

## How to Run

```bash
cd currency-exchange-sample-service
mvn spring-boot:run

cd currency-conversion-sample-service
mvn spring-boot:run
```
