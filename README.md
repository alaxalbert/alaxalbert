# Alax Albert Alves Barbosa

Desenvolvimento de software para operações de RH e logística. Trabalho com aplicações desktop, APIs e fluxos web e mobile.

## Estudos de caso

### RH desktop · recuperação de cadastros e relatórios reutilizáveis

Aplicação em Python, PyQt6 e PostgreSQL para gerir cadastros de empresas e colaboradores e gerar relatórios operacionais.

- **Recuperação de cadastros.** A interface separa registros ativos dos que estão na lixeira. A restauração fica na camada de persistência e pode ser acionada pela tela para o registro selecionado.
- **Relatórios recorrentes.** A aplicação persiste modelos de relatório e separa interface, processamento e exportação para Excel. Isso permite reabrir uma configuração já salva antes de gerar a planilha.
- **Verificação.** O repositório inclui uma suíte com pytest e uma rotina de verificação de integridade. Um cenário de demonstração com dados fictícios é remover um cadastro, restaurá-lo e conferir sua volta à lista ativa.

### Plataforma de pedidos e entregas · arquitetura e operação

Plataforma com API em TypeScript e NestJS, interfaces web e aplicativo Flutter. O backend usa PostgreSQL/PostGIS e Redis.

- **Fluxo operacional.** A loja recebe pedidos de clientes, e a operação de entrega tem interfaces próprias para lojistas, entregadores e administração. A API concentra as regras compartilhadas pelos canais.
- **Publicação.** O projeto mantém configuração Docker Compose e workflows de CI. A documentação descreve a checagem de dependências de produção e o procedimento de reversão de uma alteração publicada.
- **Recuperação.** O guia operacional documenta backup e restauração do banco. Um cenário de demonstração em ambiente de teste é criar um pedido fictício, acompanhar as transições de estado e conferir se cada papel vê apenas as ações previstas.

Os estudos descrevem a arquitetura e os fluxos dos projetos. As demonstrações propostas usam dados fictícios.
