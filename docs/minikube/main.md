# MiniKube

O MiniKube foi escolhido como orquestrador Kubernets para a arquitetura de microsserviços desenvolvida. 

## Estrutura do Projeto

Todos os microsserviços tiveram o deploy realizado no mesmo cluster, para isso, foi criado uma pasta k8s com os arquivos necessários em cada uma das API's desenvolvidas. 

A estrutura básica de diretórios para o projeto é a seguinte:

``` { .bash }
.
├── account-service
│   ├── k8s/
│   │   ├── k8s.yaml 
│   └── ...
```

## Código Fonte

Os arquivos de configuração do MiniKube são apenas criados nos repositórios de implementação da API, ou seja, aqueles que possuem ´Service´ no nome.

### Postgres

=== "Postgres"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/account-service/main/k8s/postgres.yaml"
    ```

### Account Service

=== "Deployment"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/account-service/main/k8s/deployment.yaml"
    ```

=== "Service"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/account-service/main/k8s/service.yaml"
    ```

### Auth Service

=== "Deployment"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/auth-service/main/k8s/deployment.yaml"
    ```

=== "Service"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/auth-service/main/k8s/service.yaml"
    ```

=== "Secret"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/auth-service/main/k8s/secret.yaml"
    ```

### Gateway Service

=== "Deployment"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/gateway-service/main/k8s/deployment.yaml"
    ```

=== "Service"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/gateway-service/main/k8s/service.yaml"
    ```

### Product Service

=== "Deployment"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/product-service/main/k8s/deployment.yaml"
    ```

=== "Service"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/product-service/main/k8s/service.yaml"
    ```

### Order Service

=== "Deployment"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/order-service/main/k8s/deployment.yaml"
    ```

=== "Service"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/order-service/main/k8s/service.yaml"
    ```


