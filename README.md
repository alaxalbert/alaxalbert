# Alax Albert Alves Barbosa

**Desenvolvedor de software · Departamento Pessoal, comércio local e logística**

Desenvolvo e mantenho dois produtos de ponta a ponta. O **BRTX Pro** organiza a rotina do Departamento Pessoal, da pré-admissão ao desligamento. O **BRTX Flash** permite que o comércio local receba pedidos on-line e coordene a entrega, do catálogo à confirmação do recebimento. Sou responsável pela modelagem, pelas interfaces, pela implementação, pelos testes e pela publicação dos dois projetos.

## BRTX Pro · gestão de RH e Departamento Pessoal

Criei uma aplicação desktop para equipes que precisam acompanhar o histórico dos colaboradores, fechar as rotinas de cada mês e controlar quem pode lançar, aprovar e consultar informações. O produto reúne dossiês, documentos, apontamentos, folha e prazos em fluxos ligados à empresa, à unidade e à competência.

**Como o trabalho passa pelo sistema**

1. O operacional preenche a pré-admissão e reúne os documentos. Com a aprovação e a efetivação, as informações passam a compor o cadastro e o dossiê do colaborador.
2. Durante o mês, a equipe registra ocorrências e envia lançamentos para revisão. O supervisor pode aprovar ou devolver com motivo. A folha recebe os eventos aplicáveis, e o calendário de competências reúne vencimentos e contas a pagar do DP.
3. O dossiê reúne a situação do vínculo e dá acesso a rotinas como férias, afastamento, aviso prévio e rescisão, além de documentos como a ficha de registro. Relatórios e exportações seguem as permissões de acesso.

**Decisões de engenharia**

- Separei a pessoa do vínculo jurídico, da categoria do eSocial e da forma de processamento. Na migração, os casos ambíguos seguiram para revisão.
- Estruturei a rescisão como uma operação transacional. Nos lançamentos mensais, a aprovação repetida não duplica o evento, e a edição simultânea usa controle de versão para evitar sobrescrita.
- Implementei acesso por empresa e unidade, além de permissões específicas para valores, rubricas e exportações. Incluí uma rotina para restaurar o último backup em um banco separado de homologação.

**Tecnologias** · Python, PyQt6 e PostgreSQL.

## BRTX Flash · pedidos e entregas para o comércio local

Criei uma plataforma para mercados, farmácias, restaurantes e outras lojas locais venderem por site ou aplicativo e conduzirem o pedido até a entrega. O mesmo fluxo conecta cliente, lojista, entregador e administração, com interfaces próprias para o trabalho de cada um.

**Como o pedido passa pelo sistema**

1. O cliente informa o endereço, vê a oferta da região, monta o carrinho e acompanha o pedido. A plataforma contempla conferência de estoque, frete e confirmação do Pix.
2. O lojista organiza catálogo e estoque, recebe o pedido no balcão e marca as etapas de aceite, preparo e retirada. Para mercados, há venda por peso e importação de catálogo por planilha ou integração com ERP.
3. O despacho considera proximidade e veículo compatível. O entregador acompanha a rota e confirma a entrega por código. A administração gerencia papéis e aprovações, e a plataforma contempla divisão do pagamento e repasses.

**Decisões de engenharia**

- Corrigi um login intermitente separando a identificação dos serviços de teste e produção e acrescentei uma verificação no CI para evitar a regressão.
- Tratei a disputa pelo mesmo pedido com aceite transacional e transições condicionadas ao estado esperado. Usei Redis para compartilhar estado e eventos entre réplicas.
- Ampliei a verificação automatizada com testes de módulos e 12 roteiros de ponta a ponta no CI.

**Tecnologias** · TypeScript, NestJS, PostgreSQL/PostGIS, Redis, React e Flutter.

## Marcos registrados no GitHub

| Data em 2026 | Projeto | Entrega |
| --- | --- | --- |
| 4–7 ago. | BRTX Pro | Registro da versão anterior à refatoração e separação do modelo de pessoa e vínculo. |
| 9–18 out. | BRTX Flash | Registro da versão 1.0, preparação operacional e correção da colisão entre ambientes. |
| 26–27 out. | Ambos | Rescisão transacional e deduplicação de anexos no Pro. Venda por peso e ajustes de endereço, frete e imagens no Flash. |
| 3–7 nov. | Ambos | Concorrência entre réplicas e ampliação do CI no Flash. Acesso por unidade e ajustes de folha e importação no Pro. |
| 9–12 nov. | BRTX Pro | Evolução do dossiê, ficha de registro em PDF e restauração de backup em homologação. |
| 11 nov. | BRTX Flash | Atualização do build Android e teste do service worker no fluxo de imagens da loja. |

_Os repositórios dos produtos são privados._
