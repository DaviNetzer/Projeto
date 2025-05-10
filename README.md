# Comentário de teste
// Alteração simulada para atividade

💻 Sobre o projeto
Gerenciador de tarefas - Aplicação desenvolvida com base num desafio proposto onde, o principal objetivo é criar um projeto totalmente do 0 capaz de realizar um CRUD para gerenciamento das suas tarefas.


🚀 Como está dividido o projeto
Este projeto é divido em duas partes:

Back-end (pasta backend)
Front-end (pasta frontend)
💡O Front-end precisa que o Back-end esteja sendo executado para funcionar.

Pré-requisitos
Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:

Git;
Node.js + NPM;
Docker;
Se desejar, ao invés do NPM, pode utilizar o Yarn

Caso seu sistema operacional não seja Linux, você precisará ter configurado o WSL 2 que permite que os desenvolvedores instalem uma distribuição do Linux para utilizar aplicativos, utilitários e ferramentas de linha de comando bash do Linux diretamente no Windows, além disso, sugiro também ter o app Windows Terminal para facilitar.

Como editor de código, recomendo o VSCode.

Você também pode utilizar uma ferramenta para poder consumir a API back-end, para esse projeto, utilizamos o Insomnia.

🎲 Rodando o Back-end (backend)
# Clone este repositório
$ git clone git@github.com:DaviNetzer/Projeto.git

# Acesse a pasta do projeto no terminal/cmd
$ cd gerenciador-tarefas

# Vá para a pasta backend
$ cd backend

# Rode o comando para iniciar o back-end
$ docker-compose up --build -d
Insomnia

Se deu tudo certo, no seu Docker desktop deverá aparecer o container backend que foi criado, conforme imagem abaixo: Passo 01

Antes de rodar a aplicação front-end, é preciso ter o banco de dados configurado com as devidas tabelas e colunas, para isso, utilizei como gerenciador de banco de dados o Beekeeper Studio, mas fica ao seu critério qual gerenciador irá querer utilizar, no caso, abaixo, mostrarei o passo a passo para importar o SQL pelo Beekeeper.

Baixe o arquivo database_postgres.sql na sua máquina;

Abra o Beekeeper Studio e na combo-box selecione o Postgres; Passo 01

Preencha os campos "User", "Password" e "Default Database" conforme as informações da imagem abaixo. É importante ser igual, pois é o que está configurado no .env da aplicação e que o docker irá ler para se conectar ao banco corretamente. Passo 01

Teste a conexão no botão "Test"; Passo 01

Se a conexão for bem sucedida, conecte-se ao banco de dados no botão "Connect";

Após estar conectado, vá no menu File >> Import SQL Files; Passo 01

Após importar, ele irá aparecer nesse menu, basta selecionar ele (com dois cliques) e rodar o SQL no botão "Run"; Passo 01

Ao voltar para o primeiro menu, verá que irá aparecer um schema chamado public e dentro desse schema estará a tabela tasks e suas devidas colunas. Passo 01

🧭 Rodando a aplicação Front-end (frontend) com NPM
# Vá para a pasta frontend
$ cd frontend

# Instale as dependências
$ npm i

# Execute a aplicação
$ npm run serve

# No terminal será exibido o link em que poderá visualizar a aplicação front-end rodando, geralmente na http://localhost:8080, mas pode variar se já estiver com essa porta ocupada.
🧭 Rodando a aplicação Front-end (frontend) com Yarn
# Vá para a pasta frontend
$ cd frontend

# Instale as dependências
$ yarn i

# Execute a aplicação
$ yarn run serve

# No terminal será exibido o link em que poderá visualizar a aplicação front-end rodando, geralmente na http://localhost:8080, mas pode variar se já estiver com essa porta ocupada.

🛠 Tecnologias
As seguintes ferramentas foram usadas na construção do projeto:

Frontend (Vue + Vuetify)
Axios
Dayjs
Toastify
SweetAlert2
Veja o arquivo package.json

Backend (PHP)
Docker
Nginx
PostgreSQL
