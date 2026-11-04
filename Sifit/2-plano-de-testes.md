# Plano de testes · Sifit

[← Índice](README.md) · [Requisitos](1-analise-de-requisitos.md) · [Cenários](5-matriz-de-rastreabilidade.md)

## Identificação

| Item | Definição |
| --- | --- |
| Projeto | Extensão — documentação e testes manuais do Sifit |
| Ambiente | https://sifit.centrion.com.br/login |
| Versão do sistema | Não informada; não inferida pelo aspecto da interface |
| Data | 21/10/2026 |
| Responsável acadêmico | A preencher pelo aluno |
| Plataforma observada | Windows; navegador integrado do Codex; versão não coletada |
| Tipo de ambiente | Não confirmado como produção, homologação ou sandbox |
| Estado | Fase 1: exploração da interface e planejamento; fase 2: banco e evidências integradas pendentes |

## Objetivo

Verificar funcionalidades, mensagens, consistência e persistência do sistema com testes manuais rastreáveis. A primeira fase mapeia os 44 destinos do menu principal, autenticação e perfil. A segunda verificará o ciclo completo de operações com banco e JAM, após disponibilização do acesso.

## Escopo

Inclui os requisitos RF01–RF46, consultas, formulários, caminhos condicionais, autenticação, mensagens de erro, cadastros, vínculos, exclusões e integrações disponíveis em ambiente de teste. Cada módulo tem arquivo de cenários e registro de limitações.

Ainda não inclui homologação do aplicativo do aluno, catraca física, biometria, disparos para alunos reais, transações reais Pagar.me, desempenho/carga, exploração de vulnerabilidades ou compatibilidade entre navegadores. As integrações serão testadas com destinos e ambiente dedicados.

## Estratégia de execução

1. Explorar menus e formulários sem salvar registros existentes; registrar telas, campos, ações e estados.
2. Confirmar regras de negócio e identificar tabelas, chaves e relacionamentos no esquema real.
3. Preparar massa isolada com identificador único e registrar o estado inicial no banco.
4. Executar caminhos positivos, negativos, limites e cancelamento; conferir persistência por ID após recarregar.
5. Gravar o fluxo no JAM e associar caso, consulta, ID e vídeo no registro de evidências.
6. Registrar bugs com passos e resultado esperado/obtido; testar novamente após correção.
7. Consolidar cobertura e pendências sem declarar aprovação de casos não executados.

## Técnicas

Particionamento de equivalência para entradas válidas/inválidas; valores-limite para datas, valores, caracteres e mídias; transição de estados em matrícula, avaliação, contas e check-in; análise de dependências em exclusões; testes por permissão; exploração de campos condicionais e comparação independente de cálculos.

## Priorização

| Prioridade | Fluxos |
| --- | --- |
| Alta | Login/sessão; cliente → plano → matrícula → contas; check-in/presença; avaliações/anamnese; permissões |
| Média | Fichas/exercícios/modelos; relatórios; turmas/Box; fornecedores; despesas; automações em ambiente isolado |
| Baixa | Personalização visual, editor de contrato e recursos comerciais auxiliares, sem dispensar sua cobertura |

## Estados de execução

| Estado | Uso |
| --- | --- |
| Não executado | Caso especificado, ainda não realizado |
| Aprovado | Objetivo delimitado atendido com observação registrada |
| Reprovado | Resultado observado diverge do esperado; vincular bug |
| Inconclusivo | Resultado observado, mas falta regra/origem suficiente para julgamento |
| Bloqueado | Pré-condição necessária indisponível no momento de executar |
| Não aplicável | Fora de escopo ou indisponibilidade confirmada e justificada |

O estado geral de uma tela é diferente do estado de um caso. A aprovação do cálculo visual não aprova a persistência nem todas as fórmulas do módulo.

## Critérios de entrada e saída

**Entrada para gravações:** ambiente e massa identificados; regras e dependências conhecidas; banco acessível; capacidade de recuperação definida; JAM pronto; destinos de teste disponíveis para comunicações.

**Saída:** casos do escopo executados ou exceções justificadas; IDs e evidências preenchidos; resultados conciliados com banco; falhas registradas; correções retestadas quando disponíveis; pendências aceitas pelo responsável. Esses critérios ainda não foram atendidos.

## Gestão de defeitos

O modelo do professor pede título, descrição, reprodução, evidência e gravidade. Esta adaptação acrescenta ID único, prioridade, requisito/caso vinculado, estado e limite da investigação. Severidade mede impacto; prioridade indica ordem sugerida de correção. Não atribuir causa raiz apenas pelo sintoma.

Defeitos observados ficam no [relatório de bugs](3-relatorio-de-bugs.md). Indisponibilidades declaradas pela interface e suspeitas ficam em [pendências](7-pendencias.md). A recuperação de senha é um defeito de fluxo observado; automações explicitamente “Em desenvolvimento” são funcionalidades indisponíveis.

## Riscos e tratamento

| Risco | Tratamento |
| --- | --- |
| Ambiente compartilhado e dados mutáveis | Identificar a execução e consultar por ID; não usar contagens globais como única prova |
| Gravações afetarem pessoas ou dinheiro | Usar massa e integrações de teste; não executar pagamentos/disparos reais |
| Exclusão irreversível | Confirmar recuperação/autorização no momento de executar; não excluir registros existentes |
| Chaves e dados pessoais no vídeo | Ocultar segredos e usar dados fictícios; revisar a gravação antes de compartilhar |
| Interface com carregamento assíncrono | Aguardar estado estável; não registrar zero transitório como falha |
| Banco não disponível | Planejar consultas e critérios sem inventar nomes de tabela ou resultado |

## Cronograma por marcos

| Marco | Situação |
| --- | --- |
| Referência e exploração inicial | Realizado em 21/10/2026 |
| Requisitos, inventário e cenários | Versão inicial preparada |
| Esquema do banco e validação de regras | Aguardando acesso e informações |
| Execução CRUD e gravações JAM | Não iniciada |
| Retestes e encerramento | Após correções/execução integrada |

## Entregáveis

Análise de requisitos; inventário de telas; plano; cenários BDD; matriz; relatório de bugs; relatório parcial de execução; roteiro banco/JAM; índice de evidências e lista de pendências. Formato documental Markdown, com capturas PNG como anexos.
