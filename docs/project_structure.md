# Estrutura do Projeto

## assets/
Responsável por armazenar arquivos estáticos como imagens, ícones e fontes.

Exemplos:
- logo.svg
- hero.png
- favicon.png
- background.jpg
- Poppins.ttf

## components/
Componentes reutilizáveis da aplicação. Se você usar em duas páginas diferentes, provavelmente é um componente.

### common/
Componentes genéricos reutilizáveis.

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

### forms/
Componentes relacionados a formulários.

Exemplos: 
- LoginForm
- ContactForm
- NewsletterForm
- ScheduleForm

### layout/
Componentes estruturais.

Exemplos: 
- Navbar
- Footer
- Sidebar
- Header
- PageContainer

### sections/
Grandes seções das páginas.

Exemplo da home: 
<Home>
- Hero
- Services
- Gallery
- FAQ
- CTA
- Testimonials
- Footer

### ui/
Componentes visuais da biblioteca de UI, para o frontend eu estou utilizando bastante Shadcn/ui

## pages/
Cada pasta representa uma rota da aplicação.

- Home
- About
- Contact
- Blog
- Category
- Project

Exemplo:
pages/Home/index.tsx

Essa pagina monta: 
- Navbar
- Hero
- Services
- Testimonials
- Footer
Ela não faz muita lógica. 

## routes/
Responsável pelo React Router. Nunca coloque componentes aqui.

Exemplo: 
- AppRoutes.tsx
- AboutRoutes.tsx
- PrivateRoutes.tsx
- PublicRoutes.tsx

## services/
Toda comunicação externa. Principalmente API.

Exemplo: 
- api.ts
- auth.ts
- blog.ts
- pages.ts
- services.ts

imagine: 
- GET /posts
- POST /login
- DELETE /gallery

## types/
Interfaces do Typescript.

Exemplo:
- User
- Post
- Service
- Gallery
- Page

## utils/
Funções auxiliares.

Exemplo: 
- formatPhone()
- formatCurrency()
- generateSlug()
- capitalize()
- scrollTop()
Nunca devem depender do React.

## app.tsx
É a aplicação. Normalmente é onde centralizamos todos os arquivos do site desenvolvido

## main.tsx
Entrada do React. Responsável por renderizar a aplicação.
Normalmente:

<StrictMode>
  <App />
</StrictMode>

## index.css
CSS global. Importa Tailwind basicamente.