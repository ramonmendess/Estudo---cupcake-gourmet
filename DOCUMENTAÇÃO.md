Tabela: Usuários

id (string) — Identificador único (ex.: user-0001)

nome (string) — Nome completo do usuário

email (string) — Email (único)

senha (string) — Senha (armazenamento conforme Glide)

telefone (string) — Telefone de contato

endereco (string) — Endereço para entrega

tipo_usuario (string) — admin ou cliente

data_cadastro (date) — Data de criação do cadastro

Tabela: Produtos

id (string) — product-0001

nome (string) — Ex.: “Cupcake Red Velvet”

tipo (string) — Ex.: Tradicional / Promoção (uso informativo)

preco (number) — Preço unitário (ex.: 8.00)

initial_stock (number) — Estoque inicial

descricao (string) — Ingredientes e observações

imagem (image url) — Link/imagem no Glide

ativo (boolean) — Disponível para venda (TRUE/FALSE)

Tabela: CupcakesPersonalizados

id (string) — custom-0001

usuario_id (ref → Usuários.id) — Quem criou

massa (choice) — Ex.: Baunilha, Chocolate, Red Velvet, etc.

recheio (choice) — Ex.: Brigadeiro, Doce de Leite, Nutella, etc.

cobertura (choice) — Ex.: Chantilly, Ganache, Buttercream, etc.

decoracao (choice) — Granulado, Frutas, Raspas, etc.

tamanho (choice) — P, M, G

preco_total (number) — Preço calculado por tamanho (mapa de preço)

imagem (image url) — opcional

Observação: os campos de escolha devem ser Choice fields no Glide (não permitir texto livre).

Tabela: Pedidos

id (string) — order-0001

usuario_id (ref → Usuários.id)

data_pedido (date/time)

valor_total (number) — soma dos itens (rollup)

endereco_entrega (string)

status (choice) — Pendente, Em Preparo, A Caminho, Entregue, Cancelado

metodo_pagamento (choice) — Pix, Cartão, Dinheiro

observacoes (text) — observações do cliente

Tabela: OrderItems

id (string) — item-0001

order_id (ref → Pedidos.id)

product_id (ref → Produtos.id) — null se custom

custom_id (ref → CupcakesPersonalizados.id) — null se padrão

quantidade (number)

preco_unitario (number)

subtotal (number) = quantidade * preco_unitario

Tabela: Avaliacoes

id (string)

usuario_id (ref → Usuários.id)

pedido_id (ref → Pedidos.id)

nota (number 1..5)

comentario (text)

data (date)

publicado (boolean) — TRUE/FALSE

Observações técnicas rápidas (configuração no Glide)

massa, recheio, cobertura, decoracao, tamanho → Choice component (valores fixos).

preco_total → Lookup para PriceMap (P=8.00, M=10.00, G=12.00) ou cálculo direto.

valor_total → Rollup na tabela Pedidos somando OrderItems.subtotal.

Visibilidade das telas admin → condição current_user.tipo_usuario = admin.