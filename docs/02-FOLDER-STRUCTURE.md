# Estrutura de Pastas

A estrutura existente deve ser respeitada.

Não criar novas pastas sem necessidade.

---

## assets/

Arquivos estáticos.

Utilizar para:

- imagens
- ícones
- fontes
- logos

Exemplo:

assets/

images/
icons/
fonts/
logos/


Arquivos:

- logo.svg
- hero.png
- favicon.png
- background.jpg
- Poppins.ttf


---

# components/

Componentes reutilizáveis.

Um componente deve ser criado aqui quando utilizado em duas ou mais partes.

---

# pages/

Cada pasta representa uma rota.

Exemplo:

pages/

Home/
About/
Contact/
Dashboard/


---

# routes/

Somente React Router.

Nunca colocar componentes visuais aqui.

Exemplo:

- AppRoutes.tsx
- PublicRoutes.tsx
- PrivateRoutes.tsx


---

# services/

Comunicação externa.

Exemplo:

services/

api.ts
auth.ts
users.ts
products.ts


---

# types/

Interfaces TypeScript.

Exemplo:

User.ts
Product.ts
Service.ts


---

# utils/

Funções auxiliares.

Exemplo:

formatCurrency()
formatPhone()
generateSlug()