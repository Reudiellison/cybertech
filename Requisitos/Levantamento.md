# Documento de Definição de Requisitos

**Projeto:** CyberTech RH

F*Responsáveis:** Amilton, Reudiellison, Ronei e Wanderson.

## 1. Introdução

Este documento apresenta os requisitos de usuário do sistema CyberTech RH e está organizado da seguinte forma: a Seção 2 contém uma descrição do propósito do sistema; a Seção 3 apresenta uma descrição do dominio apresentando o problema; e a Seção 4 apresenta as listas de requisitos de usuário levantados junto ao cliente.

## 2. Descrição do Propósito do Sistema

Temos como proposito desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto do colaborador e o controle de folha, gerando assim, a praticidade do processo.

## 3. Descrição do Dominio

Descrição do dominio

Desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto, visualização da folha de ponto, visualização do contracheque, envio de atestado e reclamação salarial, VT e VA para que

## 4. Requisitos de Usuário
omando por base o contexto do sistema, foram identificados os seguintes requisitos de usuário:

# Requisitos funcionais

|Identificação|Descrição|Prioridade|Depende de|
|:--------------:|:-----------:|:----------:|:------------:|
|RF01|O sistema permitirá a criação de 3 perfis: Mestre (RH), Intermediário (Supervisor) e Usuário comum (Colaborador)|Alta|---|
|RF02|O perfil mestre (RH) permitirá adicionar/alterar/excluir/pesquisa cadastrais sob os demais perfis (Intermediário e Usuário comum)|Alta|RF01|
|RF03|Tela de login deverá ser preenchido com o CPF se for usuário comum ou CNPJ se for Empresa|Alta|RF01,RF02|
|RF04|A senha de login (CPF,CNPJ) deverá conter letras maiúsculas, minúsculas, caracteres especiais e numérico|Alta|RF03|
|RF05|Para primeiro acesso ao sistema, a empresa deverá realizar o cadastro|Alta|RF01,RF03|
|RF06|Para primeiro acesso ao sistema, o colaborador receberá por e-mail os procedimentos para realizar o login com CPF e a senha provisória|Alta|RF01,RF05|
|RF07|Na tela de login deverá ter a opção de recuperação de senha (CPF,CNPJ), no qual o usuário deverá informar o e-mail no qual chegará uma nova senha provisória|Alta|RF03,RF04|
|RF08|Em todo os módulos leverá ter a funcionalidade de apoio a usuários com deficiências auditivas e visual|Alta|RF03,RF04,RF05,RF06,RF07|



Descrição: Realização de primeiro cadastro da empresa
Prioridade: Alta

- Campo: NOME - Tipo: TEXTO - Caracteres: 255
- Campo: Data de nascimento - Tipo: DATA - Caracteres: 10
- Campo: E-mail - Tipo: TEXTO - Caracteres: 255
- Campo: Endereço - Tipo: TEXTO - Caracteres: 255
- Campo: nº - Tipo: TEXTO - Caracteres: 255

**RF04** - Cadastrar colaborador

Descrição: Realização de primeiro cadastro
Prioridade: Alta

- Campo: NOME - Tipo: TEXTO - Caracteres: 255
- Campo: Data de nascimento - Tipo: DATA - Caracteres: 10
- Campo: E-mail - Tipo: TEXTO - Caracteres: 255
- Campo: Endereço - Tipo: TEXTO - Caracteres: 255
- Campo: nº - Tipo: TEXTO - Caracteres: 255


# Requisitos não-funional 
