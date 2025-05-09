---
title:  "Testando com Rest Assured uma API Fake criada com Json Server dentro de um container Docker"
date:   2024-04-29 19:04:23
categories: [Api]
tags: [Automação API]
image: /images/json-server.jpg
---

Tech Stack: [Rest Assured] [JUnit] [Docker] [Fake JSON Server]


Endpoints
- POST /hotel-reservations para incluir uma nova reserva.
- GET /hotel-reservations para listar todas as reservas.
- GET /hotel-reservations?clientId={id_cliente} para listar todas as reservas de um cliente específico.
- PUT /hotel-reservations/{id_reserva} para atualizar uma reserva.
- DELETE /hotel-reservations/{id_reserva} para deletar uma reserva.


No wiremock :

```plaintext
project-root/
│
├── mappings/
│ ├── create-reservation.json
│ ├── list-reservations.json
│ ├── list-reservations-by-client.json
│ ├── update-reservation.json
│ └── delete-reservation.json
│
└── __files/
└── (any static files you need, if necessary)
```

