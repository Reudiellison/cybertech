[TOCM]

[TOC]

# Documento de Definição de Requisitos

Projeto: CyberTech RH

Responsáveis: Amilton, Reudiellison, Ronei e Wanderson.

## 1. Introdução

Este documento apresenta os requisitos de usuário do sistema CyberTech RH e está organizado da seguinte forma: a Seção 2 contém uma descrição do propósito do sistema; a Seção 3 apresenta uma descrição do dominio apresentando o problema; e a Seção 4 apresenta as listas de requisitos de usuário levantados junto ao cliente.

## 2. Descrição do Propósito do Sistema

Temos como proposito desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto do colaborador e o controle de folha, gerando assim, a praticidade do processo.

## 3. Descrição do Dominio

Desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto, visualização da folha de ponto, do contracheque, envio de atestado e reclamação salarial, VT e VA.

## 4. Requisitos de Usuário

Tomando por base o contexto do sistema, foram identificados os seguintes requisitos de usuário:

### 4.1 Requisito Funcional

|Identificação|Descrição|Prioridade|Depende de|
|:--------------:|:----------:|:------------:|:-------------:|
|RF01|O sistema permitirá a criação de 3 perfis: Mestre (RH), Intermediário (Supervisor) e Usuário comum (Colaborador)|Alta|---|
|RF02|O perfil mestre (RH) permitirá adicionar/alterar/excluir/pesquisa cadastrais sob os demais perfis (Intermediário e Usuário comum)|Alta|RF01|
|RF03|Tela de login deverá ser preenchido com o CPF se for usuário comum ou CNPJ se for Empresa|Alta|RF01,RF02|
|RF04|A senha de login (CPF,CNPJ) deverá conter letras maiúsculas, minúsculas, caracteres especiais e numérico|Alta|RF03|
|RF05|Para primeiro acesso ao sistema, a empresa deverá realizar o cadastro|Alta|RF01,RF03|
|RF06|Para primeiro acesso ao sistema, o colaborador receberá por e-mail os procedimentos para realizar o login com CPF e a senha provisória|Alta|RF01,RF05|
|RF07|Na tela de login deverá ter a opção de recuperação de senha (CPF,CNPJ), no qual o usuário deverá informar o e-mail no qual chegará uma nova senha provisória|Alta|RF03,RF04|
|RF08|Em todo os módulos leverá ter a funcionalidade de apoio a usuários com deficiências auditivas e visual|Alta|RF03,RF04,RF05,RF06,RF07|
|RF09|Para o primeiro acesso, existirá uma tela de cadastro da empresa ao sistema, no qual irá conter os seguintes campos|Alta|---|
|RF10|A empresa deverá cadastrar o colaborador através da tela de Cadastro de colaborador|Alta|RF02,RF05|
|RF11|O modulo registro de ponto deverá registrar o ponto de entrada e saída, através da localização|Alta|---|
|RF12|O modulo de registro de ponto permitirá o registro num perímetro de até 100m da localização registrada pela empresa|Alta|RF11|
|RF13|O modulo folha de ponto irá espelhar todos registros coletados durante o mês|Alta|RF11,RF12|
|RF14|O modulo folha de ponto irá conter uma função chamada registros inválidos, no qual deverá resumir os pontos de atenção|Alta|RF11|
|RF15|O módulo folha de ponto irá conter as seguintes opções por dia: Solicitar abono, envio de atestado e resumo diário|Alta|RF10,RF11,RF13|
|RF16|O módulo registro de ponto deverá conter o status da folha se encontra: em aberto ou fechada|Alta|RF11|
|RF17|O módulo registro de ponto irá ter um filtro de pesquisa para a buscar de outras folha de ponto para se caso precise futuramente|Alta|RF11|
|RF18|O módulo contracheque irá conter todos registros de pagamentos efetuados durante todo o mês|Alta|RF11|
|RF19|O módulo contracheque estará disponivel no formato PDF para as opções de: Donwloas, compartilhamento e visualização|Alta|RF18|
|RF20|O módulo contracheque irá conter um ferramenta de pesquisa de registro de pagamentos para se caso, o colaborador precisar para eventuais consultas futuras|Alta|RF18|
|RF21|O módulo contestação irá conter as seguintes opções para registro de abertura de reclamação: Salarial/Férias, Vale-Alimentação e Vale-Transporte|Alta|---|
|RF22|O módulo contestação irá conter uma ferramenta de pesquisa, de acordo com os registros que foram abertos pelo colaborador, ou seja, o histórico|Alta|RF22|

### 4.2 Requisito de Negócio

|Identificação|Descrição|Prioridade|Depende de|Depende do RF|
|:--------------:|:----------:|:------------:|:-------------:|:-------------:|
|RN01|Validar CEP|Alta|---|
|RN02|Validar CPF|Alta|---|
|RN03|Validar campos obrigatórios|Alta|---|
|RN04|Validar no máximo 3 tentativas de senha de login. Excedendo o limite de tentativas o usuário será notificado por e-mail, para se caso for ele, o mesmo procurar resetar a senha|Alta|---|
|RN05|Validar localização|Alta|---|

### 4.3 Requisitos Não Funcionais

|Identificação|Descrição|Categoria|Escopo|Prioridade|Depende de|
|:--------------:|:----------:|:------------:|:-------------:|:-------------:|:------------:|
|RNF01|Plataforma Web/Mobile|Disponibilidade|Sistema|Alta|---|
|RNF02|Certificado digital (HTTPS)|Segurança de acesso|Funcionalidade|Alta|RNF01|
|RNF03|Sistema deverá suportar num mínimo 1000 usuários conectados simultaneamente|Eficiência|Sistema|Alta|RNF01|
|RNF04|A senha de login (CPF,CNPJ) deverá conter letras maiúsculas, minúsculas, caracteres especiais e numérico|Segurança de acesso|Funcionalidade|Alta|RNF01|
|RNF05|Deverá conter três servidores: Dev, Homologação e produção|Interoperabilidade|Sistema|Alta|RNF01|
|RNF06|O Sistema deve ser executado no Sistema Operacional Windows 7 ou superior e Linux Debian|Disponibilidade|Sistema|Alta|RNF01|
|RNF07|O produto será desenvolvido para máquinas com pelo menos 2 GB de Ram|Interoperabilidade|Sistema|Alta|RNF01|
