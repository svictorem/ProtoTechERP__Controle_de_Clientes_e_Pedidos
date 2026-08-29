# ProtoTech - Controle de Clientes e Pedidos

O projeto **ProtoTech - Controle de Clientes e Pedidos** é uma aplicação web desenvolvida em Java com o framework Spring Boot. O sistema tem como objetivo principal gerenciar o fluxo de clientes, produtos, controle de estoque e o processamento de pedidos, oferecendo também a funcionalidade de geração de relatórios em formato PDF.

## 🚀 Funcionalidades

- **Gestão de Clientes:** Cadastro, atualização, visualização e remoção de clientes.
- **Catálogo de Produtos:** Gerenciamento de produtos e suas respectivas categorias.
- **Controle de Estoque:** Monitoramento das quantidades em estoque com sistema de alertas para produtos próximos ao fim.
- **Gestão de Pedidos:** Registro e acompanhamento de pedidos e de seus itens.
- **Geração de Relatórios:** Emissão de relatórios gerenciais e de pedidos em formato PDF.
- **Painel Administrativo:** Gestão da plataforma via usuários administradores.

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Java 17
- **Framework Principal:** Spring Boot (Web MVC, Data JPA, Validation)
- **Template Engine:** Thymeleaf (renderização de páginas HTML no servidor)
- **Banco de Dados:** MySQL
- **Geração de PDFs:** OpenHTMLtoPDF
- **Build Tool:** Maven

## 📁 Estrutura do Projeto

A aplicação segue a arquitetura em camadas padrão do Spring MVC:
- `model`: Entidades JPA que representam as tabelas do banco de dados (`Cliente`, `Produto`, `Pedido`, etc.).
- `repository`: Interfaces do Spring Data JPA para comunicação com o banco.
- `service`: Camada onde ficam concentradas as regras e lógicas de negócio.
- `controller`: Controladores REST/MVC que lidam com as requisições HTTP e devolvem as views.
- `templates`: Páginas HTML dinâmicas renderizadas pelo Thymeleaf (localizadas na pasta `src/main/resources/templates`).

## ⚙️ Como Executar o Projeto

### Pré-requisitos
Certifique-se de ter instalado em sua máquina:
- Java Development Kit (JDK) 17
- MySQL Server
- Maven (opcional, pois o projeto possui o Maven Wrapper `mvnw`)

### Passo a Passo

1. **Configuração do Banco de Dados:**
   - O sistema está configurado para tentar se conectar ao banco `grupo02_db` localmente e, caso ele não exista, criá-lo (devido à flag `createDatabaseIfNotExist=true`).
   - As credenciais padrão definidas no `application.properties` são:
     - Usuário: `root`
     - Senha: `12345678`
   - *Atenção:* Se você usar outra senha no seu MySQL, modifique-a no arquivo `src/main/resources/application.properties`.

2. **Compilando e Rodando:**
   - Abra o terminal na raiz do projeto e execute:
     - No Windows: `mvnw.cmd spring-boot:run`
     - No Linux/Mac: `./mvnw spring-boot:run`
   - *Alternativa:* Você também pode importar o projeto na sua IDE favorita (IntelliJ IDEA, Eclipse, VS Code) e rodar a classe principal `Projeto02Grupo02Application.java`.

3. **Acessando a Aplicação:**
   - Com o servidor iniciado, abra seu navegador e acesse:
     ```
     http://localhost:8080
     ```

---
*Projeto desenvolvido pelo Grupo 02 (Cetam).*
