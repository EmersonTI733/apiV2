# intrucao para utilizar o projeto
    apos baixar:
    $ npm i
    verifique se as configuracoes .env estao de acordo com o banco 
    $ npx sequelize-cli db:migrate
    para rodar o projeto
    $ nodemon app.js
    ou
    $ npm run play

INICIAR E CRIANCAO DO PROJETO
# npm init

instalar o sequelize
# npm i sequelize ou 
# npm install --save sequelize

instalação do drive para o banco de dados mysql
# npm install --save mysql2

sequelize CLI
# npm install --save-dev sequelize-cli

configuração cli
Para criar um projeto vazio, você precisará executar o comandoinit
# npx sequelize-cli init

CRIAR DATABASE NO WORKBANCH
### CREATE DATABASE residuum03 CHARACTER SET utf8mb4  COLLATE utf8mb4_unicode_ci;
se nao funcionar crie diretamente no ambiente do banco

TRABALHANDO COM VARIAVEIS DE AMBIENTE
# npm install dotenv --save

# CRIAR A MIGRATION usuario
    npx sequelize-cli model:generate --name usuario --attributes usuario_nome:string,usuario_matricula:integer,usuario_senha:string
# CRIAR A MIGRATION tabela instituicao
    npx sequelize-cli model:generate --name instituicao --attributes instituicao_nome:string,instituicao_cnpj:integer
# Criar a migation tabela categoria_Instituicao
    npx sequelize-cli model:generate --name categoria_Instituicao --attributes categoria_Instituicao:string
# Criar a migation tabela endereco
    npx sequelize-cli model:generate --name endereco --attributes rua:string,bairro:string,cidade:string,estado:string,cep:integer,pais:string
# Criar a migation tabela categoria_usuario
    npx sequelize-cli model:generate --name categoria_usuario --attributes categoria_usuario:string
# Criar a migation tabela licenca
    npx sequelize-cli model:generate --name licenca --attributes numero_licenca:integer
# Criar a migation tabela situacao
    npx sequelize-cli model:generate --name situacao --attributes situacao:string
# Criar a migation tabela nota_fiscal
    npx sequelize-cli model:generate --name nota_fiscal --attributes nota_fiscal:integer
# Criar a migation tabela mtr_organico/outros
    npx sequelize-cli model:generate --name mtr_organico --attributes mtr_quantidadeKg:real,mtr_numero:integer,mtr_rastro:string,notaFiscal_id:integer,usuario_id:integer

  
EXECUTAR A MIGRATION
# npx sequelize-cli db:migrate

DEPENDENCIA DO EXPRESS PARA O SERVIDOR
# npm i express
# tabela user
 dados recebidos: nom, matricula, senha

# nome das tabelas  dados_empresas, dados_condominios, dados_residencias
    dados nas referidas tabelas estao relacionados aos clientes da empresa
# dados_empresas
    dados recebidos: nome_fantasia, cnpj, cep, bairro, rua, numero, razao_social, ceo, email, telefone
# dados_condominios
    dados recebidos: nome_condominio, cnpj, cep, bairro, rua, numero, email, telefone, sindico
# dados_residencias
    dados recebidos: nome_titular, cpf, cep, bairro, rua, numero, email, telefone   


    npm i --save bcryptjs para criptografias

    npm i swagger-ui-express#   a p i V 2 
 
 #   a p i V 2 
 
 