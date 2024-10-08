# Authentication API

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)

This project is an API built using **Java, Java Spring, H2 as the database.**

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database](#database)
- [Contributing](#contributing)

## Installation

1. Clone the repository:

```bash
git clone https://github.com/jorgeguedess/study_Spring_challengePicpay.git
```

2. Install dependencies with Maven

## Usage

1. Start the application with Maven
2. The API will be accessible at http://localhost:8080

## API Endpoints

The API provides the following endpoints:

**GET USERS**

```markdown
GET /users - Retrieve a list of all users.
```

```json
[
  {
    "id": 1,
    "firstName": "Luana",
    "lastName": "Silva",
    "document": "12345677",
    "email": "luana@example.com",
    "password": "senha",
    "balance": 20.0,
    "userType": "MERCHANT"
  },
  {
    "id": 2,
    "firstName": "Pedro",
    "lastName": "Rangel",
    "document": "123456783",
    "email": "luckas@example.com",
    "password": "senha",
    "balance": 0.0,
    "userType": "COMMON"
  }
]
```

**POST USERS**

```markdown
POST /users - Register a new user into the App
```

```json
{
  "firstName": "Luana",
  "lastName": "Silva",
  "password": "senha",
  "document": "12345677",
  "email": "lucas@example.com",
  "userType": "COMMON",
  "balance": 10
}
```

**POST TRANSACTIONS**

```markdown
POST /transactions - Register a new Transaction between users (COMMON to COMMON or COMMON to MERCHANT)
```

```json
{
  "senderId": 2,
  "receiverId": 1,
  "value": 10
}
```

## Database

The project utilizes [H2 Database](https://www.h2database.com/html/tutorial.html) as the database.
