Descrição do Projeto

Este projeto implementa um sistema de composição de pedidos de restaurante utilizando o padrão de projeto Decorator. O sistema permite combinar um prato principal com diversos acompanhamentos, bebidas e sobremesas de forma flexível, calculando automaticamente o preço total e gerando a descrição completa do pedido.

Padrão Decorator

O Decorator é um padrão estrutural que permite adicionar novos comportamentos a objetos dinamicamente, colocando-os dentro de objetos especiais que contêm esses comportamentos.

Neste projeto:

Pedido é a interface comum

PratoPrincipal é o componente concreto base

PedidoDecorator é a classe abstrata decoradora

Acompanhamento, Bebida e Sobremesa são decoradores concretos

Funcionalidades

Criar pedidos com pratos principais

Adicionar múltiplos acompanhamentos

Adicionar bebidas ao pedido

Incluir sobremesas

Calcular preço total automaticamente

Gerar descrição completa do pedido


Como Usar

1-Crie um prato principal:

Pedido pedido = new PratoPrincipal("Filé Mignon", 45.0f);

2-Adicione acompanhamentos:

pedido = new Acompanhamento(pedido, "Batata Frita", 8.0f);

3-Adicione bebidas:

pedido = new Bebida(pedido, "Refrigerante", 6.0f);

4-Adicione sobremesas:

pedido = new Sobremesa(pedido, "Sorvete", 10.0f);

5-Obtenha informações:

float precoTotal = pedido.getPreco();

String descricao = pedido.getDescricao();


Testes:

O projeto inclui testes unitários abrangentes que verificam:

Criação de pratos principais

Adição de cada tipo de decorador

Combinações múltiplas de decoradores

Cálculo correto do preço total

Geração correta da descrição

Para executar os testes:

mvn test


Requisitos:

Java 8 ou superior

JUnit 4 ou 5 para testes

Maven (opcional)
