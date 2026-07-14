# Services e Comunicação

Toda comunicação externa deve passar por services.

---

Exemplo:

services/products.ts


Responsável:

GET /products

POST /products

DELETE /products


---

Nunca fazer:

fetch()
axios()
requisições HTTP


diretamente dentro de componentes.


---

Fluxo correto:

Component

↓

Hook

↓

Service

↓

API Laravel


---

O frontend apenas consome dados.