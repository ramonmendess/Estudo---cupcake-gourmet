# Cupcake Gourmet

**Aluno:** Ramon Cássio Alves Mendes  
**RGM:** 31435351

**Situação-Problema escolhida:** Situação-Problema 3 — Testes, correções e validação da solução.

## Objetivo
Aplicação no-code desenvolvida no Glide para centralizar, de forma intuitiva e simples, a venda e personalização de cupcakes. O sistema permite que clientes personalizem produtos, façam pedidos e avaliem suas compras; e que administradores gerenciem produtos, pedidos e usuários.

## Tecnologias
- Plataforma: **Glide (No-code)**  
- Banco de dados: **Glide internal database (Collections)**  
- Hospedagem: automática pelo Glide

## Perfis de usuário
- **Cliente:** navegar catálogo, montar cupcake personalizado, adicionar ao carrinho, finalizar pedido, visualizar histórico e avaliar pedidos entregues.
- **Administrador:** cadastrar/editar produtos, alterar status de pedidos, visualizar histórico de pedidos, gerenciar usuários.

## Telas principais
- Login / Cadastro / Recuperação de senha  
- Catálogo de produtos (cupcakes tradicionais)  
- Cupcakes Personalizados (opções de massa, recheio, cobertura, decoração e tamanho)  
- Carrinho / Checkout (edição antes de confirmar)  
- Histórico de pedidos (status, data, última movimentação)  
- Avaliações (nota e comentário)  
- Perfil do usuário  
- Área administrativa (produtos, pedidos, usuários, relatórios simples)

## Regras de negócio principais
- Usuário **deve estar logado** para realizar pedidos.  
- Pedido sempre nasce com status **Pendente**; apenas o admin altera status.  
- Cliente não pode alterar status do pedido.  
- Cupcake personalizado: livre escolha entre opções disponíveis; preço é **padrão por tamanho** (P/M/G).  
- Apenas admin pode criar/alterar produtos, preços e estoque.

## Estrutura de dados (resumo)
Tabelas principais: `Usuários`, `Produtos`, `CupcakesPersonalizados`, `Pedidos`, `OrderItems`, `Avaliações`.

(Dicionário completo das tabelas e campos no arquivo `DOCUMENTACAO.md`.)

## Como acessar
- Link do app Glide: *(https://silky-error-7936.glide.page)*  
- Link do vídeo demonstrativo (YouTube / Drive): *(inserir link)*

## Evidências e documentação
- `DOCUMENTACAO.md` — documentação técnica (requisitos, modelagem, dicionário de dados)  
- `LAUDO-QUALIDADE.md` — laudo de qualidade com evidências dos testes  
- `assets/` — prints das telas e diagramas

---

## Contato
Ramon Cássio Alves Mendes — RGM 31435351