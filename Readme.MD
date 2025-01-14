# Projeto Final DIO 2024

- #### Esta API demonstra o funcionamento de uma Web API de um cliente de banco e sua interação com Swagger

## Principais Tecnologias
![Blog](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![Blog](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white
)
- **Java 17**
- **Spring Boot 3**
- **Spring Data JPA**
- **OpenAPI (Swagger)**
- **Railway**

## [Link do Figma](https://www.figma.com/file/0ZsjwjsYlYd3timxqMWlbj/SANTANDER---Projeto-Web%2FMobile?type=design&node-id=1421%3A432&mode=design&t=6dPQuerScEQH0zAn-1)

O Figma foi utilizado para a abstração do domínio desta API, sendo útil na análise e projeto da solução.

## Diagrama de Classes (Domínio da API)

```mermaid
classDiagram
    class User {
        -String name
        -Account account
        -List~Feature~ features
        -Card card
        -List~News~ news
    }

    class Account {
        -String number
        -String agency
        -Double balance
        -Double limit
    }

    class Feature {
        -String icon
        -String description
    }

    class Card {
        -String number
        -Double limit
    }

    class News {
        -String icon
        -String description
    }

    User --> Account
    User --> "1..*" Feature
    User --> Card
    User --> "1..*" News
```
### Documentação da API: Swagger

![img.png](img.png)

### Banco de Dados em memória H2 Database

![img_1.png](img_1.png)
