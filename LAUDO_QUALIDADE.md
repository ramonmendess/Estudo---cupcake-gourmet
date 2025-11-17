# Laudo de Qualidade — Cupcake Gourmet
**Aluno:** Ramon C. A. Mendes — RGM 314-35351

## Resumo
Foram realizados 5 testes com usuários, cobrindo os fluxos principais: login, personalização, pedido, checkout, histórico e avaliação. As evidências foram coletadas (prints) e as correções aplicadas conforme indicado.

## Problemas identificados e correções aplicadas
1. **Atualização de tela após confirmação do pedido**  
   - *Sintoma:* status do pedido não aparecia no admin imediatamente.  
   - *Correção:* adicionar ação de "Refresh Data" / forçar reload após confirmação.

2. **Opção vazia em Choice (personalização)**  
   - *Sintoma:* aparecia opção em branco ao escolher massa/cobertura.  
   - *Correção:* remover entradas vazias e configurar Choice fields com valores fixos.

3. **Imagem do item não carregava no detalhe do pedido**  
   - *Sintoma:* imagem ausente no detalhe do pedido.  
   - *Correção:* corrigir campo Image Source para apontar para a coluna de imagem correta.

4. **Avaliação aceita nota 0**  
   - *Sintoma:* usuário conseguiu inserir nota = 0.  
   - *Correção:* validação de nota mínima (1..5).

5. **Observações do pedido não salvas**  
   - *Sintoma:* campo observações não persistia em algumas ações.  
   - *Correção:* incluir campo nas ações de gravação do pedido.

## Resultado geral
Após as correções, os fluxos críticos (cadastro, login, personalização, pedido e acompanhamento) funcionam conforme os requisitos. Não foram encontrados bugs críticos que impeçam o uso. Recomenda-se adicionar no futuro: controle de estoque detalhado e integração de pagamentos real (fora do escopo do MVP).

## Evidências
- Vídeo com demonstração das correções (link no README)
