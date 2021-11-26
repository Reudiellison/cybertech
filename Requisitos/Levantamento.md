# Documento de Definição de Requisitos

**Projeto:** CyberTech RH

**Responsáveis:** Amilton, Reudiellison, Ronei e Wanderson.

## 1. Introdução

Este documento apresenta os requisitos de usuário do sistema CyberTech RH e está organizado da seguinte forma: a Seção 2 contém uma descrição do propósito do sistema; a Seção 3 apresenta uma descrição do dominio apresentando o problema; e a Seção 4 apresenta as listas de requisitos de usuário levantados junto ao cliente.

## 2. Descrição do Propósito do Sistema

Temos como proposito desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto do colaborador e o controle de folha, gerando assim, a praticidade do processo.

## 3. Descrição do Dominio

Descrição do dominio

Desenvolver um software para o gerenciamento do RH (Recursos Humanos) para facilitar o registro de ponto remoto, visualização da folha de ponto, visualização do contracheque, envio de atestado e reclamação salarial, VT e VA para que

## 4. Requisitos de Usuário

Tomando por base o contexto do sistema, foram identificados os seguintes requisitos de usuário:

# Requisitos funcionais

## F1 - Cadastrar colaborador ##

**RF01** - O sistema permitirá a criação de 3 perfis: Mestre (RH), Intermediario (Supervisor) e Usuário comum (Colaborador).
**RF02** - O perfil mestre (RH) permitirá adicionar/alterar/excluir/pesquisa cadastrais sob os demais perfis (Intermediario e Usuário comum).
**RF03** - Cadastramento da empresa:

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


# Requisitos não-funional #

**RNF01** - Rodar em plataforma Web.
**RNF02** - Uso de HTTPS.

# Regra de negocio #

**RN01** - Validar CPF.
**RN02** - Validar CEP.
**RN03** - Validar campos obrigatórios: Nome, Endereço, E-mail...

