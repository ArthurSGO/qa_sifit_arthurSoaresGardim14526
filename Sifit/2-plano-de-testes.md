# Plano de testes · Sifit

[← Índice](README.md) · [Requisitos](1-analise-de-requisitos.md) · [Cenários](5-matriz-de-rastreabilidade.md)

## Identificação

| Item | Definição |
| --- | --- |
| Projeto | Extensão — documentação e testes manuais do Sifit |
| Ambiente | https://sifit.centrion.com.br/login |
| Versão do sistema | Não informada |
| Data de elaboração | 21/10/2026 |
| Revisão documental | 04/11/2026 |
| Responsável acadêmico | Não informado |
| Plataforma observada | Windows; navegador integrado do Codex; versão não coletada |
| Tipo de ambiente | Informado como banco de testes; correspondência com a aplicação a confirmar |
| Estado | Exploração inicial concluída; execução funcional parcial |

## Objetivo

Verificar funcionalidades, mensagens, consistência e persistência do sistema por meio de testes manuais rastreáveis. O levantamento abrange 44 destinos do menu principal, autenticação e perfil, organizados em 46 requisitos e 267 casos de teste.

## Escopo

Inclui consultas, formulários, caminhos condicionais, autenticação, mensagens de erro, cadastros, vínculos, exclusões e integrações disponíveis em ambiente de teste. Cada módulo possui cenários e limitações documentadas.

Não estão incluídos nesta etapa: homologação do aplicativo do aluno, catraca física, biometria, comunicações para alunos reais, transações financeiras reais, desempenho/carga, testes de segurança e compatibilidade entre navegadores.

## Estratégia

| Frente | Abrangência | Situação |
| --- | --- | --- |
| Exploração da interface | Menus, formulários, campos, ações e estados | Levantamento inicial concluído |
| Validação funcional | Caminhos positivos, negativos, limites e cancelamento | 15 casos executados |
| Persistência | Valores, identificadores, relacionamentos e alterações de estado | Pendente de mapeamento do banco |
| Gestão de defeitos | Reprodução, resultado esperado/obtido, impacto e evidências | 5 bugs registrados |
| Retestes | Verificação dos casos relacionados após correção | Não realizados |

## Técnicas

Particionamento de equivalência; análise de valores-limite; transição de estados; análise de dependências; testes por permissão; exploração de campos condicionais e comparação de cálculos.

## Priorização

| Prioridade | Fluxos |
| --- | --- |
| Alta | Login/sessão; cliente → plano → matrícula → contas; check-in/presença; avaliações/anamnese; permissões |
| Média | Fichas/exercícios/modelos; relatórios; turmas/Box; fornecedores; despesas; automações |
| Baixa | Personalização visual, editor de contrato e recursos comerciais auxiliares |

## Estados de execução

| Estado | Definição |
| --- | --- |
| Não executado | Caso especificado, ainda não realizado |
| Aprovado | Resultado observado atende ao objetivo do caso |
| Reprovado | Resultado observado diverge do esperado |
| Inconclusivo | Informações insuficientes para avaliar o resultado |
| Bloqueado | Pré-condição necessária indisponível |
| Não aplicável | Caso fora do escopo ou funcionalidade indisponível, com justificativa |

## Critérios de entrada e saída

**Entrada:** ambiente disponível, permissões compatíveis e dados de teste adequados ao caso. As verificações de persistência dependem do esquema do banco; integrações dependem de infraestrutura de teste.

**Saída:** casos do escopo executados ou com impedimentos documentados; resultados e evidências registrados; defeitos relacionados aos casos e retestes documentados quando houver correção. A etapa atual ainda não atende aos critérios de encerramento.

## Evidências e defeitos

As execuções possuem registro de resultado e capturas disponíveis no [índice de evidências](evidencias/README.md). Vídeos complementam os registros de bugs quando a sequência de ações ou o comportamento dinâmico é necessário para demonstrar a ocorrência.

O [relatório de bugs](3-relatorio-de-bugs.md) contém identificador, descrição, passos de reprodução, resultado esperado e obtido, severidade, prioridade, ambiente, caso relacionado, evidências e situação do reteste. Investigações e funcionalidades indisponíveis constam nas [pendências](7-pendencias.md).

## Riscos e dependências

| Risco ou dependência | Impacto nos testes |
| --- | --- |
| Ambiente compartilhado e dados mutáveis | Variação de registros e indicadores entre execuções |
| Massa e integrações de teste | Limitação de cadastros, exclusões, comunicações e operações financeiras |
| Carregamento assíncrono | Estados transitórios podem afetar a observação |
| Esquema do banco não documentado | Validação de persistência e relacionamentos pendente |
| Regras de negócio não confirmadas | Critérios de aceitação sujeitos à validação |

## Marcos

| Marco | Situação |
| --- | --- |
| Exploração inicial | Realizada em 21/10/2026 |
| Requisitos, inventário e cenários | Versão inicial preparada |
| Acesso ao banco pelo MySQL Workbench | Confirmado em 22/10/2026 |
| Esquema do banco e regras de negócio | Pendentes |
| Execução de operações persistentes | Não iniciada |
| Evidências complementares dos bugs | Pendentes |
| Retestes e encerramento | Pendentes |

## Entregáveis

Análise de requisitos; inventário de telas; plano de testes; cenários BDD; matriz de rastreabilidade; relatório de bugs; relatório de execução; índice de evidências e registro de pendências. Documentos em Markdown e capturas em PNG.
