# Regras de Componentes

Não criar componentes gigantes.

Preferir:

Componentes pequenos
+
Composição
+
Reutilização


---

# components/common/

Componentes genéricos.

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


Não possuem regras de negócio.


---

# components/forms/

Componentes de formulário.

Exemplos:

- LoginForm
- ContactForm
- NewsletterForm
- ProductForm


Responsabilidades:

- Interface.
- Validação visual.


Não podem:

- Fazer chamadas API.
- Controlar regras de negócio.


---

# components/layout/

Componentes estruturais.

Exemplos:

- Navbar
- Header
- Footer
- Sidebar
- DashboardLayout
- PageContainer


---

# components/sections/

Grandes blocos de páginas.

Exemplo:

Home:

Hero
Services
Gallery
FAQ
Testimonials
CTA


Criar pastas quando a seção possuir muito código.


---

# components/ui/

Biblioteca visual.

Utilizar:

- Shadcn/ui


Não recriar componentes existentes.