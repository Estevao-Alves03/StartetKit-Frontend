# Estrutura do Projeto

Este documento define as regras de organização e arquitetura do frontend.

A estrutura existente deve ser respeitada obrigatoriamente.

Não criar novas pastas sem necessidade.

Não alterar a arquitetura do projeto.

O frontend será responsável apenas pela interface e comunicação com APIs.

Regras de negócio, autenticação, banco de dados e permissões serão tratados futuramente pelo backend Laravel.

---

# assets/

Responsável por armazenar arquivos estáticos da aplicação.

Utilizar para:

- imagens
- ícones
- fontes
- arquivos visuais

Exemplos:

```
assets/
├── images/
├── icons/
├── fonts/
└── logos/
```

Exemplos de arquivos:

- logo.svg
- hero.png
- favicon.png
- background.jpg
- Poppins.ttf

---

# components/

Local destinado a componentes reutilizáveis.

Regra:

Se um componente for utilizado em duas ou mais partes da aplicação, ele deve ser criado aqui.

Evitar criar componentes duplicados.

---

## components/common/

Componentes genéricos que podem ser utilizados em qualquer projeto.

Exemplos:

- Button
- Input
- Modal
- Card
- Badge
- Loading
- Skeleton
- Container
- SectionTitle
- EmptyState

Não devem possuir regras específicas de negócio.

---

## components/forms/

Componentes relacionados a formulários.

Responsáveis apenas pela interface e validação visual.

Exemplos:

- LoginForm
- ContactForm
- NewsletterForm
- ScheduleForm
- ProductForm

Não devem realizar chamadas diretas para API.

A comunicação deve ser feita através da camada services.

---

## components/layout/

Componentes estruturais da aplicação.

Exemplos:

- Navbar
- Header
- Footer
- Sidebar
- PageContainer
- DashboardLayout

Responsáveis pela estrutura visual das páginas.

---

## components/sections/

Grandes blocos de uma página.

Utilizados principalmente em páginas institucionais e landing pages.

Exemplo:

Home:

```
Home
├── Hero
├── Services
├── Gallery
├── FAQ
├── Testimonials
└── CTA
```

Cada seção deve possuir sua própria pasta quando possuir grande quantidade de código.

---

## components/ui/

Componentes da biblioteca visual.

Utilizar principalmente componentes do:

- Shadcn/ui

Não recriar componentes que já existem na biblioteca.

---

# pages/

Cada pasta representa uma rota da aplicação.

Exemplos:

```
pages/
├── Home
├── About
├── Contact
├── Blog
├── Dashboard
└── Products
```

Cada página deve ser responsável por organizar seus componentes.

Exemplo:

```
pages/Home/index.tsx
```

Pode montar:

- Navbar
- Hero
- Services
- Testimonials
- Footer

A página não deve conter muita lógica.

A lógica deve ficar separada em:

- hooks
- services
- utils

---

# routes/

Responsável exclusivamente pelo React Router.

Nunca colocar componentes visuais dentro desta pasta.

Exemplos:

- AppRoutes.tsx
- PublicRoutes.tsx
- PrivateRoutes.tsx

As rotas devem apenas definir:

- caminhos
- páginas
- proteção futura de acesso

---

# services/

Responsável por toda comunicação externa.

Principalmente:

- APIs
- requisições HTTP
- integrações externas

Exemplos:

```
services/
├── api.ts
├── auth.ts
├── users.ts
├── products.ts
└── pages.ts
```

Exemplos de responsabilidades:

```
GET /products

POST /login

DELETE /gallery
```

Nunca realizar chamadas diretamente dentro dos componentes.

---

# Autenticação

O frontend NÃO deve criar sistemas próprios de autenticação.

Não utilizar:

- Supabase Auth
- Firebase Auth
- OAuth externo
- Banco local de usuários

A autenticação será realizada pelo backend Laravel.

O frontend deve apenas possuir:

- telas de login;
- componentes de formulário;
- estados visuais;
- rotas preparadas para proteção futura.

---

# types/

Responsável pelas interfaces e tipos TypeScript.

Exemplos:

```
types/
├── User.ts
├── Product.ts
├── Service.ts
├── Gallery.ts
└── Page.ts
```

Todo dado utilizado pela aplicação deve possuir tipagem.

Evitar utilizar:

```ts
any
```

---

# utils/

Funções auxiliares independentes do React.

Não podem possuir:

- hooks;
- estados;
- componentes.

Exemplos:

- formatPhone()
- formatCurrency()
- generateSlug()
- capitalize()
- scrollTop()

---

# app.tsx

Arquivo principal da aplicação.

Responsável por centralizar:

- providers
- layouts
- rotas
- configurações globais

---

# main.tsx

Ponto de entrada do React.

Responsável por renderizar a aplicação.

Exemplo:

```tsx
<StrictMode>
  <App />
</StrictMode>
```

---

# index.css

Arquivo de estilos globais.

Responsável por:

- importação do Tailwind;
- variáveis globais;
- estilos base.

Evitar colocar estilos específicos de componentes aqui.

---

# Regras Gerais

## Componentização

Não criar componentes gigantes.

Dividir responsabilidades.

Preferir:

```
Componentes pequenos
+
Composição
+
Reutilização
```

---

## Responsividade

Todo componente deve funcionar em:

- Desktop
- Tablet
- Mobile

---

## Código

Sempre utilizar:

- TypeScript
- Componentes funcionais React
- Hooks
- Código limpo
- Componentes reutilizáveis

---

## Importante

Antes de criar qualquer arquivo novo:

1. Verifique se já existe algo parecido.
2. Reutilize componentes existentes.
3. Respeite a arquitetura atual.
4. Não adicione bibliotecas sem necessidade.