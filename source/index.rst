.. API TECSUS documentation master file, created by
   sphinx-quickstart on Mon Jun  5 09:28:49 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to API TECSUS's documentation!
======================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

.. _index:

Estação Meteorológica - API Tecsus
==================================

Links dos Repositórios
----------------------

- [Estacao-Metereologica-Front-end]
https://github.com/EquipeGfour/Estacao-Metereologica-Front-end

- [Estacao-Metereologica-Back-end]
https://github.com/EquipeGfour/Estacao-Metereologica-Back-end

- [Estacao-Metereologica-Back-end-Embarcado]
https://github.com/EquipeGfour/Estacao-Metereologica-Back-end-Embarcado

Objetivo do Projeto
-------------------

O objetivo deste projeto é criar uma estação meteorológica que coleta dados meteorológicos em tempo real, como temperatura, umidade, pressão atmosférica, direção e velocidade do vento, radiação solar, entre outros.

A estação meteorológica será composta por sensores que coletam esses dados e os enviam para um servidor na nuvem por meio de uma API. Os dados coletados serão armazenados em um banco de dados e estarão disponíveis para acesso e visualização pelos usuários.

Além disso, o projeto também contempla o desenvolvimento de um front-end para exibir os dados coletados de forma gráfica e intuitiva, permitindo que os usuários acompanhem as condições meteorológicas em tempo real.

Backlog do Produto
------------------

.. csv-table:: Backlog do Produto
   :header: "#", "Backlog do Produto", "Status"
   :align: left

   #1, Fluxo Do Projeto, Alto
   #2, Estruturar Banco De Dados Relacional, Alto
   #3, Estruturar Banco de Dados Não Relacional, Alto
   #4, Desenvolvimento Da Lógica Do Projeto, Alto
   #5, Lógica De Recebimento De Dados Da Estação, Alto
   #6, Lógica Do Envio De Dados Da Estação, Alto
   #7, Criação Do Layout Do Projeto, Alto
   #8, Cadastro Da Estação, Alto
   #9, Cadastro Dos Parâmetros, Alto
   #10, Cadastro De Alertas, Médio
   #11, Cadastro De Usuário Administrador, Baixo
   #12, Criação De Testes, Médio
   #13, Editar e Excluir Parâmetros, Alto
   #14, Criação De Gráficos Com os Dadaos Gerados, Alto
   #15, Desenvolvimento Do Datalogger, Alto
   #16, Montagem Da Estação, Alto
   #17, Simulação De Envio De Dadaos Da Estação, Médio
   #18, Tutorial Para Os Alunos, Baixo

   🔗, `Backlog por Sprint <https://docs.google.com/document/d/1kECz8mn7UBylxL2PJYfd3QBeSv1SXjSDf6k_uKoqY1A/edit?usp=sharing>`_

User Stories
------------

.. csv-table:: User Stories
   :header: "#", "Ator", "Ação", "Motivo"
   :align: left

   #1, Administrador, Criar Estações, Gerar Dados
   #2, Administrador, Cadastrar Sensores, Ter Variedades De Dados
   #3, Administrador, Gerar Conteúdos, Objetivar Os Dados Gerados
   #4, Usuário, Cadastro, Ter Acesso A Mais Informações
   #5, Usuário, Navegar No Portal, Buscar Informações Metereológicas
   #6, Usuário/Administrador, Pesquisa, Gerar Conteúdos Para Melhorias Para O Uso Dos Dados

Modelo de Dados
---------------

.. image:: /docs/db.png
   :align: center

