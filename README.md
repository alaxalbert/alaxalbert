# Alax Albert Alves Barbosa

**Desenvolvedor de software · RH, logística e automação de operações**

Sou o responsável técnico pelos dois projetos deste portfólio. Conduzo o trabalho de ponta a ponta, da modelagem do domínio e das interfaces à implementação, aos testes, à publicação e à manutenção.

## Linha do tempo dos projetos

| Período em 2026 | Projeto | Marco registrado no GitHub |
| --- | --- | --- |
| 4–7 ago. | RH desktop | Registrei a versão anterior à refatoração e separei pessoa, vínculo jurídico, categoria eSocial e forma de processamento. |
| 9–18 out. | Pedidos e entregas | Registrei a versão 1.0, avancei na preparação operacional e corrigi uma colisão entre serviços de teste e produção. |
| 26 out. | Ambos | No RH, tratei a consistência da rescisão e dos anexos. Na plataforma de entregas, incluí venda por peso e melhorei o tratamento de endereços e frete. |
| 3–7 nov. | Ambos | Na plataforma de entregas, tratei concorrência entre réplicas e ampliei o CI. No RH, incluí acesso por unidade e ajustei regras de folha e importação. |
| 9–12 nov. | RH desktop | Evoluí o dossiê do colaborador, a ficha de registro e a recuperação do banco em homologação. |

## Sistema de RH desktop · da modelagem do vínculo à homologação

**Python, PyQt6 e PostgreSQL**

- **4–7 de agosto.** A primeira referência do histórico é uma versão anterior à refatoração. Em seguida, separei a pessoa do vínculo jurídico, da categoria do eSocial e da forma de processamento. Na migração de reclassificação, encaminhei os casos ambíguos para revisão em vez de atribuir uma categoria automaticamente.
- **26 de outubro.** Estruturei a rescisão como uma operação que conclui por inteiro ou falha por inteiro. Na mesma etapa, reorganizei as migrações em um pacote preservando o conteúdo das 70 existentes e passei a identificar anexos repetidos pelo hash SHA-256 do conteúdo.
- **3–7 de novembro.** Implementei restrição de acesso por unidade dentro da empresa. Ajustei a importação incremental para preservar a data e o motivo de encerramento de vínculos e unifiquei a origem dos dias úteis e do descanso semanal remunerado no calendário da competência.
- **9–12 de novembro.** Levei ações de férias e rescisão para o contexto do dossiê. Adicionei a ficha de registro em PDF e um teste que lê o documento gerado. Também incluí uma rotina que restaura o último backup em um banco separado de homologação e ajustei a inicialização para evitar repetir alterações de esquema em um banco já migrado.

## Plataforma de pedidos e entregas · do fluxo comercial à concorrência

**TypeScript, NestJS, PostgreSQL/PostGIS, Redis, React e Flutter**

- **9–18 de outubro.** Registrei a versão 1.0. Em seguida, avancei nas rotinas de fila de e-mail, backup externo e ambiente de teste. Corrigi um login intermitente causado por colisão entre serviços de teste e produção, separei seus nomes e acrescentei uma verificação no CI para detectar a regressão.
- **26–27 de outubro.** Adaptei a plataforma para venda por peso, refinei o endereço usado na entrega e o cálculo de frete e corrigi o carregamento de imagens da loja no fluxo com service worker.
- **3 de novembro.** Tratei a concorrência no aceite de entregas com uma transação e condicionei transições de estado ao estado esperado. Usei Redis para compartilhar estado e eventos entre réplicas, defini uma instância líder para rotinas periódicas e serializei a execução das migrações. Ampliei a verificação automatizada com testes de módulos e 12 roteiros de ponta a ponta no CI.
- **11 de novembro.** Atualizei a ferramenta de build do Android e acrescentei um teste de service worker ao revisar o carregamento de imagens no site da loja.

_As datas correspondem aos marcos registrados no histórico do GitHub. Os repositórios dos produtos são privados._
