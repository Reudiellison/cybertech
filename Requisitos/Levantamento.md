#Indice

[TOC]

# Documento de Definição de Requisitos

Projeto: CyberTech RH

Responsáveis: Amilton, Reudiellison, Ronei e Wanderson.

## 1. Introdução

Este documento apresenta os requisitos de usuário do sistema CyberTech RH e está organizado da seguinte forma:
* Seção 2 contém uma descrição do propósito do sistema;
* Seção 3 apresenta uma descrição do dominio apresentando o problema; e a Seção 4 apresenta as listas de requisitos de usuário levantados junto ao cliente.

## 2. Descrição do Propósito do Sistema

Temos como proposito desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto do colaborador e o controle de folha, gerando assim, a praticidade do processo.

## 3. Descrição do Dominio

Desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto, visualização da folha de ponto, do contracheque, envio de atestado e reclamação salarial, VT e VA.

## 4. Requisitos de Usuário

Tomando por base o contexto do sistema, foram identificados os seguintes requisitos de usuário:

### 4.1 Requisito Funcional

|Identificação|Descrição|Prioridade|Depende de| Perfil|
|:--------------:|:----------:|:------------:|:-------------:|:----------:|
|RF01| Usuário precisa fazer login| Alta| ---| Comum|
|RF02| Usuário precisa bater ponto| Alta| RF01| Comum|
|RF03| Usuário precisa ver folha de ponto| Média| RF01,RF02| Comum|
|RF04| Usuário precisa visualizar contra-cheque| Média| RF01,RF02| Comum|
|RF05| Usuário precisa solicitar abono| Média| RF01,RF02| Comum|
|RF06| Usuário precisa enviar atestado| Alta| RF01,RF02| Comum|
|RF07| Usuário precisa fazer download/visualizar/compartilhar contra-cheque| Baixa| RF01,RF02| Comum|
|RF08| Usuário precisa de sistema de busca| Baixa| RF01,RF02| Comum|
|RF09| Usuário precisa do sistema de constestação e mensagem/comentario| Média| RF01,RF02| Comum|
|RF10| Usuário precisa visualizar registros inválidos| Alta| RF01,RF02| Comum|
|RF11| Precisa analisar constestação do usuário| Média| RF09| Secundário/Gerência|
|RF12| Precisa responder abono| Alta| RF05| Secundário/Gerência|
|RF13| Precisa visualizar colaboradores do seu setor| Alta| RF02| Secundário/Gerência|
|RF14| Repassar ao "Mestre" contestação que não possa resolver| Alta| RF11| Secundário/Gerência|
|RF15| Pode cadastrar biometria no ponto físico| Alta| RF01| Secundário/Gerência|
|RF16| Enviar notificação (mensagem e avisos)| Média| RF09| Secundário/Gerência|
|RF17| Precisa receber login mestre (equipe de DBA)| Alta| ---| Mestre|
|RF18| Cadastrar unidades da empresa (filial e matriz)| Alta| RF17| Mestre|
|RF19| Cadastrar funcionarios da emrpesa| Alta| RF17| Mestre|
|RF20| Alterar perfil| Alta| RF17| Mestre|
|RF21| CRUD (criar, ler, atualizar, deletar e desativar)| Alta| RF17| Mestre|
|RF22| Analizar contestações passadas (responder)| Alta| RF14| Mestre|
|RF23| Imprimir folhas de ponto| Alta| ---| Mestre|
|RF24| Criar/visualizar  equipes por departamentos| Alta| ---| Mestre|
|RF25| Recuperação de senha| Alta| ---| Mestre|
|RF26|Envio de Atestado| Baixo| ---| Mestre|


### 4.2 Regras de Negócio

|Identificação|Descrição|Prioridade|Depende de|Apoio do RF|
|:--------------:|:----------:|:------------:|:-------------:|:-------------:|
|RN01|Validar contas (se possui na base)|Alta|---|RF19|
|RN02|Opção de usar CPF ou CNPJ| Alta|RN01|RF21|
|RN03|Receber senha provisória por e-mail de 6 dígitos| Alta|RN01|RF01|
|RN04|Senha de login no mínimo 6 dígitos|Alta|RN03|RF01|
|RN05|Opção de manter conectado|Baixa|---|---|
|RN06|Senha deverá conter letras maiúsculas, minúsculas, caracteres especiais e alfa-numérico|Alta|---|RF01|
|RN07|Ícone personalizado para registro de ponto|Baixa|---|---|
|RN08|Para evitar duplicidade haverá tempo mínimo para o próximo registro|Média|---|---|
|RN09|a folha de ponto será preenchida automáticamente de acordo com o registro de ponto|Alta|---|RF02|
|RN10|O horário do sistema deverá alinhar com o servidor NTP para registro| Alta|---|---|
|RN11|Tipos de abonos (SCROLL)|Alta|---|RF05
|RN12|Campos (data inicial, final e total de horas)|Alta|RN11|---|
|RN13|Campos para escrever justificativa. 255 caracteres|Média|RN11|RF22|
|RN14|A solicitação deverá mostrar status que se encontra|Média|RN11|RF22|
|RN15|Campos de preenchimentos (Atestado)|Alta|---|RF06|
|RN16|Tipos de Atestado, motivo, data, início e fim|Alta|RN15|RF06|
|RN17|CID, CRM do profissional, nome do profissional e ícone para anexar o arquivo|Alta|RN16|RF06|
|RN18|Visualização da Folha de Ponto|Alta|---|RF03|
|RN19|Mostrar erros no resgitro inconsistente|Alta|RN18|RF03|
|RN20|Tipos de erros inconsistentes (faltas, falta hora)|Média|RN19|RF03|
|RN21|Status da folha (aberto, fechado)|Alta|---|RF03|
|RN22|Calcular horas trabalhadas para resumo diário|Alta|RN21|RF03|
|RN23|Pesquisar e realizar downloads/compartilhar de qualquer mês|Média|---|RF07|
|RN24|O contra-cheque será em arquivo PDF|RN23|RF07|
|RN25|Filtro da folha de pagamento por período(dia, mês e ano)|Baixa|---|RF08|
|RN26|Filtro de contestação (data, número e status)|Alta|---|RF09|
|RN27|São três tipos (salário, vale alimentação e transporte)|Alta|---|RF09|
|RN28|Puxar nome, matrícula, função, departamento e campo de discrição com 255 caracteres|Alta|RN27|RF09|
|RN29|Todo login mestre será concedido pela equipe de desenvolvimento|Alta|---|---|


### 4.3 Requisitos Não Funcionais

|Identificação|Descrição|Categoria|Escopo|Prioridade|Depende de|
|:--------------:|:----------:|:------------:|:-------------:|:-------------:|:------------:|
|RNF01|Plataforma Web/Mobile|Disponibilidade|Sistema|Alta|---|
|RNF02|Certificado digital (HTTPS)|Segurança de acesso|Funcionalidade|Alta|RNF01|
|RNF03|Sistema deverá suportar no mínimo 1000 usuários conectados simultaneamente|Eficiência|Sistema|Alta|RNF01|
|RNF04|A senha de login (CPF,CNPJ) deverá conter letras maiúsculas, minúsculas, caracteres especiais e numérico|Segurança de acesso|Funcionalidade|Alta|RNF01|
|RNF05|Deverá conter três servidores: Dev, Homologação e produção|Interoperabilidade|Sistema|Alta|RNF01|
|RNF06|O Sistema deve ser executado em Mobile/Desktop|Disponibilidade|Sistema|Média|RNF01|
|RNF07|O produto será desenvolvido para máquinas com pelo menos 2 GB de Ram|Interoperabilidade|Sistema|Média|RNF01|
