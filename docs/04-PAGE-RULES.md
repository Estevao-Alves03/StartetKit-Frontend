# Regras de Pages

Cada página representa uma rota.

Exemplo:

pages/Home/index.tsx


---

A página deve:

- Organizar componentes.
- Montar a estrutura visual.
- Controlar composição.


---

A página NÃO deve:

- Possuir muita lógica.
- Fazer chamadas API.
- Ter regras de negócio.


---

A lógica deve ficar em:

- hooks
- services
- utils


---

Exemplo:

pages/Products

index.tsx
components/
types.ts
data.ts