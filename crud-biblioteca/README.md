# CrudBiblioteca

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 21.2.10.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Vitest](https://vitest.dev/) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.

# Perguntas e Respostas

**1. Qual é a responsabilidade do componente?**
A responsabilidade do componente é gerenciar a interface do usuário (view). Ele conecta a lógica da aplicação (no TypeScript) com o template (HTML) e os estilos (CSS), tratando as interações do usuário (como cliques e formulários) e atualizando os dados exibidos na tela.

**2. Qual é a responsabilidade do service?**
O service (serviço) é responsável por encapsular regras de negócio, acesso a dados (como chamadas a APIs e banco de dados via HTTP) e o compartilhamento de informações entre diferentes componentes. Isso mantém os componentes "limpos" e focados apenas na visualização, promovendo a reutilização de código.

**3. Para que serve o model?**
O model (modelo/interface em TypeScript) serve para tipar os dados da aplicação. Ele define a estrutura, o formato e os tipos das propriedades de um objeto, garantindo segurança na tipagem (type safety), ajudando a evitar erros durante o desenvolvimento e facilitando o autocompletar na IDE.

**4. Por que o campo id é opcional?**
Em um modelo de dados, o campo `id` costuma ser opcional (ex: `id?: string` ou `id?: number`) porque quando estamos criando um novo registro (antes de enviá-lo ao backend), ele ainda não possui um identificador. O `id` só é gerado e atribuído pelo banco de dados após o cadastro ser efetivado.

**5. Qual método HTTP lista dados?**
O método **GET**.

**6. Qual método HTTP cadastra dados?**
O método **POST**.

**7. Qual método HTTP atualiza dados?**
O método **PUT** (para substituição completa do registro) ou **PATCH** (para atualização parcial).

**8. Qual método HTTP exclui dados?**
O método **DELETE**.

**9. Para que serve o router-outlet?**
O `<router-outlet>` é uma diretiva do Angular que atua como um marcador/espaço reservado no template HTML da aplicação. É nesse local exato que o roteador do Angular irá carregar e exibir dinamicamente os componentes correspondentes às rotas que o usuário acessar.

**10. Por que precisamos usar .subscribe()?**
O Angular utiliza a biblioteca RxJS e *Observables* para lidar com operações assíncronas, como requisições HTTP. Um Observable é "preguiçoso" (lazy) e não executa a requisição até que alguém o chame. O método `.subscribe()` é usado para se inscrever nesse fluxo: ele dispara a execução da requisição e permite acessar os dados retornados (ou os erros) dentro da sua função de callback para atualizar a aplicação.
