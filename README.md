# Construindo-seu-Portfólio-Front-end-do-Zero-com-HTML-CSS-e-JavaScript

Construir um portfólio front-end do zero utilizando HTML, CSS e JavaScript é uma excelente maneira de consolidar habilidades essenciais para desenvolvimento web enquanto cria uma vitrine profissional para seus projetos. Vamos detalhar como poderemos estruturar e desenvolver seu portfólio de forma organizada e eficiente.

### Passos Iniciais

1. **Configuração do Ambiente de Desenvolvimento**
   - Instale um editor de código como VS Code, Sublime Text ou qualquer outro de sua preferência.
   - Tenha um navegador web instalado (Chrome, Firefox, etc.) para testar seu projeto.
   - Crie uma conta no GitHub para hospedar seu código e utilizar o GitHub Pages.

2. **Estrutura do Projeto**

   Organizar seu projeto de forma modular e clara ajuda na manutenção e extensão futura. Vamos estruturar nosso portfólio básico:

   ```
   meu-portfolio/
   ├── index.html
   ├── css/
   │   ├── styles.css
   │   └── (outros estilos, se necessário)
   ├── js/
   │   ├── main.js
   │   └── (outros scripts, se necessário)
   ├── img/
   │   └── (imagens utilizadas no portfólio)
   └── README.md
   ```

   - **index.html**: Página principal do seu portfólio.
   - **css/**: Diretório para os arquivos CSS.
   - **js/**: Diretório para os arquivos JavaScript.
   - **img/**: Diretório para armazenar imagens utilizadas no portfólio.
   - **README.md**: Documentação básica do seu projeto.

### Desenvolvimento do Portfólio

1. **HTML (index.html)**

   O HTML será o esqueleto do seu portfólio, definindo a estrutura e o conteúdo da página. Aqui está um exemplo básico:

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Meu Portfólio</title>
       <link rel="stylesheet" href="css/styles.css">
   </head>
   <body>
       <header>
           <div class="container">
               <h1>Meu Portfólio</h1>
               <nav>
                   <ul>
                       <li><a href="#sobre">Sobre</a></li>
                       <li><a href="#projetos">Projetos</a></li>
                       <li><a href="#contato">Contato</a></li>
                   </ul>
               </nav>
           </div>
       </header>
       <section id="sobre" class="section">
           <div class="container">
               <h2>Sobre Mim</h2>
               <p>Olá! Eu sou [seu nome].</p>
           </div>
       </section>
       <section id="projetos" class="section">
           <div class="container">
               <h2>Meus Projetos</h2>
               <div class="grid">
                   <!-- Exemplo de projeto -->
                   <div class="project">
                       <img src="img/projeto1.png" alt="Projeto 1">
                       <h3>Projeto 1</h3>
                       <p>Descrição breve do projeto.</p>
                       <a href="#" class="btn">Ver mais</a>
                   </div>
                   <!-- Outros projetos -->
               </div>
           </div>
       </section>
       <section id="contato" class="section">
           <div class="container">
               <h2>Contato</h2>
               <form id="contact-form">
                   <input type="text" name="name" placeholder="Seu nome" required>
                   <input type="email" name="email" placeholder="Seu e-mail" required>
                   <textarea name="message" placeholder="Sua mensagem" required></textarea>
                   <button type="submit">Enviar</button>
               </form>
           </div>
       </section>
       <footer>
           <div class="container">
               <p>&copy; 2024 Meu Portfólio. Todos os direitos reservados.</p>
           </div>
       </footer>
       <script src="js/main.js"></script>
   </body>
   </html>
   ```

2. **CSS (styles.css)**

   O CSS será responsável pelo estilo e layout do seu portfólio. Aqui está um exemplo básico para estilizar o cabeçalho e a seção de projetos:

   ```css
   /* styles.css */

   /* Reset básico */
   * {
       margin: 0;
       padding: 0;
       box-sizing: border-box;
   }

   body {
       font-family: Arial, sans-serif;
       line-height: 1.6;
       background-color: #f4f4f4;
   }

   .container {
       max-width: 1200px;
       margin: 0 auto;
       padding: 0 20px;
   }

   header {
       background-color: #333;
       color: #fff;
       padding: 10px 0;
   }

   header h1 {
       font-size: 2em;
   }

   nav ul {
       list-style-type: none;
   }

   nav ul li {
       display: inline;
       margin-right: 20px;
   }

   nav ul li a {
       color: #fff;
       text-decoration: none;
       font-size: 1.2em;
   }

   .section {
       padding: 50px 0;
   }

   .section h2 {
       font-size: 1.8em;
       margin-bottom: 20px;
   }

   .grid {
       display: grid;
       grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
       gap: 20px;
   }

   .project {
       background-color: #fff;
       padding: 20px;
       box-shadow: 0 0 10px rgba(0,0,0,0.1);
   }

   .project img {
       width: 100%;
       height: auto;
       border-radius: 5px;
       margin-bottom: 10px;
   }

   .project h3 {
       font-size: 1.4em;
       margin-bottom: 10px;
   }

   .project p {
       color: #666;
   }

   .btn {
       display: inline-block;
       background-color: #333;
       color: #fff;
       padding: 10px 20px;
       text-decoration: none;
       border-radius: 5px;
       transition: background-color 0.3s ease;
   }

   .btn:hover {
       background-color: #555;
   }

   /* Estilos adicionais conforme necessário */

   ```

3. **JavaScript (main.js)**

   Utilize JavaScript para adicionar interatividade ao seu portfólio, como animações, validação de formulários, etc. Aqui está um exemplo básico:

   ```javascript
   // main.js

   // Exemplo de funcionalidade para scroll suave
   document.querySelectorAll('a[href^="#"]').forEach(anchor => {
       anchor.addEventListener('click', function(e) {
           e.preventDefault();

           document.querySelector(this.getAttribute('href')).scrollIntoView({
               behavior: 'smooth'
           });
       });
   });

   // Exemplo de validação de formulário simples
   const form = document.getElementById('contact-form');

   form.addEventListener('submit', function(e) {
       e.preventDefault();

       // Validar os campos (exemplo simples)
       let name = this.elements['name'].value;
       let email = this.elements['email'].value;
       let message = this.elements['message'].value;

       if (name && email && message) {
           // Enviar o formulário (exemplo: enviar para um backend ou email)
           alert('Formulário enviado com sucesso!');
           this.reset();
       } else {
           alert('Por favor, preencha todos os campos.');
       }
   });
   ```

### Implantação com GitHub Pages

Para hospedar seu portfólio online, utilize o GitHub Pages:

1. Faça o commit e o push do seu projeto para um repositório GitHub público.
2. Vá para as configurações do seu repositório no GitHub.
3. Na seção GitHub Pages, selecione o branch `main` (ou o branch que você está utilizando) como source.
4. Seu portfólio estará acessível publicamente através do link fornecido (geralmente `https://seu-usuario.github.io/seu-repositorio`).

### Considerações Finais

Construir um portfólio front-end utilizando HTML, CSS e JavaScript não apenas demonstra suas habilidades como desenvolvedor web, mas também oferece uma plataforma para apresentar seus projetos de forma profissional. Personalize seu portfólio conforme necessário, adicione mais projetos e funcionalidades conforme você avança no aprendizado e na carreira de desenvolvimento web.
