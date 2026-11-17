# Relatório parcial de execução · Sifit

[← Índice](README.md) · [Bugs](3-relatorio-de-bugs.md) · [Matriz](5-matriz-de-rastreabilidade.md)

**Data:** 21/10/2026 · **Fase:** exploração da interface e verificações delimitadas.

## Resultado da etapa

Foram visitados os **44 itens do menu principal**, além do login e do perfil. Foram inspecionados formulários, modais, campos condicionais, as quatro abas de avaliação e as sete abas de configurações. Isso dá cobertura de navegação dos destinos visíveis nesta conta; não comprova cobertura de todos os estados internos nem execução integral dos fluxos.

O escopo registrado compreende **15 verificações executadas**: **9 aprovadas, 5 reprovadas e 1 inconclusiva**. As demais funcionalidades integram o inventário e as possibilidades de avaliação complementar, sem inclusão no escopo atual de execução. Não foram feitos cadastros, edições ou exclusões deliberadas de registros existentes; os formulários preenchidos para cálculo foram descartados. A sessão foi encerrada e restaurada para verificar autenticação.

## Resumo verificável

| Medida | Quantidade |
| --- | ---: |
| Destinos do menu visitados | 44 |
| Requisitos catalogados | 46 |
| Executados | 15 |
| Aprovados | 9 |
| Reprovados | 5 |
| Inconclusivos | 1 |
| Bugs registrados | 5 |
| Vídeos anexados aos bugs | 0 |
| Operações de persistência conciliadas com banco | 0 |

## Casos executados

| Caso | Objetivo | Resultado | Observação / ocorrência |
| --- | --- | --- | --- |
| CT-RF01-01 | Entrar com credenciais válidas | Aprovado | Redirecionou para /dashboard; interface mostrou Jair. |
| CT-RF01-02 | Rejeitar credenciais inválidas | Aprovado | Credenciais fictícias rejeitadas com O nome de usuário e senha não correspondem. |
| CT-RF01-03 | Impedir entrada com campos vazios | Aprovado | Não entrou com campos vazios. Na primeira tentativa apareceu mensagem genérica; em uma repetição não houve mensagem inline perceptível. Aprovação restrita ao bloqueio de acesso. |
| CT-RF01-04 | Abrir recuperação de senha | Reprovado | Link não abriu recuperação nem orientação; permaneceu na tela de login. BUG-001 |
| CT-RF01-05 | Encerrar sessão | Aprovado | Sair do sistema retornou para /login. |
| CT-RF01-06 | Proteger rota após logout | Aprovado | Abrir /clientes após logout redirecionou para /login. |
| CT-RF02-01 | Carregar Página Inicial | Aprovado | Resumo, indicadores e menus carregaram. Aprovação de apresentação, sem homologar totais. |
| CT-RF02-02 | Conciliar cartão Sem Matrículas e detalhamento | Inconclusivo | Inicialmente cartão mostrou 6 e modal 0. Na revisão, modal mostrou 6 registros e total 6, compatíveis com o cartão. A divergência inicial não se repetiu; conciliação completa ainda depende do banco. INV-001 |
| CT-RF03-01 | Identificar corretamente o Dashboard | Reprovado | /dash exibiu título Despesas Fixas. BUG-002 |
| CT-RF07-08 | Tratar vencimento inválido no perfil | Reprovado | Perfil do registro de teste exibiu vencimento e próximo vencimento 30/11/-0001. Persistência/causa não verificadas. BUG-004 |
| CT-RF08-08 | Preencher matrícula por diária sem salvar | Aprovado | Plano Diário preencheu parcela e total 20,00, término no mesmo dia e ocultou Dia Vencimento; formulário descartado sem salvar. |
| CT-RF09-08 | Calcular IMC na interface sem salvar | Aprovado | 1,75 m e 70 kg resultaram em 22.857142857142858 na interface; operação cancelada. |
| CT-RF09-09 | Exibir unidade correta do IMC | Reprovado | Rótulo apresentou IMC kg/m³. BUG-003 |
| CT-RF43-01 | Navegar pelas sete abas sem salvar | Aprovado | As sete abas e a subaba Endpoints & Tokens abriram; nenhuma configuração foi salva. |
| CT-RF46-01 | Exibir perfil coerente com a conta | Reprovado | Meu perfil abriu conteúdo de demonstração Hello Jesse/Jessica Jones. BUG-005 |

## Evidências e limites

As 8 capturas disponíveis estão no [índice de evidências](evidencias/README.md). Logout, proteção de rota, cálculo de diária e navegação de abas possuem registro textual de observação. O BUG-001 possui evidência complementar em vídeo pendente; os demais defeitos estão demonstrados por capturas. Os valores utilizados no cálculo de IMC são fictícios e foram descartados.

O ambiente apresentou dados já cadastrados de testes e alterações de contadores durante o carregamento. Não se atribuiu toda variação a defeito. Perfil, cliente e cálculo foram reobservados; não foi inferida causa raiz a partir do aspecto da tela.

## Situação da entrega

Evidência em vídeo do BUG-001 pendente. A investigação INV-001 permanece inconclusiva. Retestes dependem da disponibilização de correções. A etapa documentada é uma avaliação parcial da interface e não constitui homologação integral do sistema.
