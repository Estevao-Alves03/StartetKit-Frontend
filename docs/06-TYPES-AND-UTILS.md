# Typescript

Todo dado utilizado deve possuir tipagem.

Evitar:

any


---

Exemplo:

types/Product.ts


interface Product {

id:number;

name:string;

price:number;

}


---

# Utils

Funções auxiliares independentes do React.


Podem conter:

- Formatação.
- Conversões.
- Helpers.


Exemplos:

formatPhone()

formatCurrency()

capitalize()

generateSlug()


---

Não podem possuir:

- Hooks.
- Estados.
- Componentes.