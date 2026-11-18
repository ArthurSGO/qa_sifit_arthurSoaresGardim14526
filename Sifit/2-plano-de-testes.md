# Plano de testes · Sifit

[← Índice](README.md) · [Requisitos](1-analise-de-requisitos.md) · [Cobertura](5-matriz-de-rastreabilidade.md) · [Execução e evidências](6-plano-de-execucao-e-evidencias.md)

## Identificação

| Item | Definição |
| --- | --- |
| Projeto | Extensão — documentação e testes manuais do Sifit |
| Ambiente | https://sifit.centrion.com.br/login |
| Versão do sistema | Não informada |
| Levantamento inicial | 21/10/2026 |
| Revisão de escopo | 18/11/2026 |
| Plataforma observada | Windows; navegador integrado do Codex; versão não coletada |
| Estado | Exploração inicial concluída; execução funcional parcial e ampliação planejada |

## Objetivo

Avaliar as funcionalidades documentadas da Sifit, com resultados rastreáveis e comprovação das operações persistentes na interface e no banco de testes.

## Escopo

O inventário abrange 46 áreas funcionais. A execução planejada organiza os cadastros e operações relacionados em 22 fluxos, incluindo autenticação e consultas como verificações associadas e capturas específicas. A entrega não fica limitada às 15 verificações já realizadas.

As operações de cadastro, consulta, alteração e exclusão ou cancelamento integram o fluxo da entidade, conforme ações disponíveis. A comprovação de CRUD inclui a operação no sistema e a consulta correspondente no banco, conforme orientação acadêmica informada para o trabalho.

A análise do esquema, das chaves e das tabelas ainda está pendente. A conexão pelo MySQL Workbench foi confirmada em 22/10/2026. Sem conferência no banco, a persistência permanece não verificada, mesmo quando o comportamento da interface foi observado.

## Execução e evidências

| Componente | Situação |
| --- | --- |
| Inventário de telas, campos e ações | Disponível para as 46 áreas |
| Verificações históricas | 15 executadas: 9 aprovadas, 5 reprovadas e 1 inconclusiva |
| Fluxos funcionais FL01–FL22 | 22 referências de cobertura, sujeitas à conciliação com os casos recebidos |
| Evidências de defeitos | Capturas e descrição dos passos e resultados |
| Acervo da equipe | 73 casos, com 70 links de vídeo e três de print; revisão iniciada |
| Capturas locais | 8 existentes; complementos após conciliação da cobertura |

Novas evidências serão em capturas de tela; os vídeos recebidos da equipe serão reaproveitados após revisão. Os prints dos CRUDs incluem resultados no sistema e no banco; sua quantidade depende das operações executadas. As 12 capturas específicas de consultas e relatórios são referências sujeitas à conciliação com o acervo recebido. O detalhamento, a associação aos requisitos e a evidência de cada fluxo constam no [plano de execução e evidências](6-plano-de-execucao-e-evidencias.md).

A [consolidação da equipe](9-consolidacao-da-equipe.md) distingue resultados informados, revisão local e persistência. As mídias inspecionadas usam ambiente diferente da exploração histórica; a equivalência de dados não foi confirmada.

## Técnicas

Exploração da interface; caminhos positivos e negativos; validações de campos relevantes; transições de estado; consulta e comparação de dados persistidos; integridade de vínculos; verificação de permissões e análise de resultados e relatórios.

## Critérios de resultado

| Estado | Definição |
| --- | --- |
| Não executado | Fluxo planejado, ainda não realizado |
| Aprovado | Resultado esperado atendido, com comprovação no banco nas operações CRUD |
| Reprovado | Divergência observada e documentada |
| Inconclusivo | Evidência ou regra insuficiente para avaliar o resultado |
| Bloqueado | Acesso, dados, infraestrutura ou funcionalidade necessários indisponíveis |

Os resultados históricos conservam o objetivo de interface delimitado na execução original; não são aprovação retrospectiva dos CRUDs ainda não realizados.

## Limitações

Pagar.me, envio para Todos os alunos, WhatsApp, biometria e catraca dependem de ambiente dedicado, contas ou infraestrutura não disponíveis na exploração. Essas operações permanecem bloqueadas. A automação FL22 depende de execução com canal Apenas painel, sem envio externo. Funcionalidades Em desenvolvimento são registradas como indisponíveis.

Ações de edição e exclusão não visíveis no levantamento serão confirmadas no fluxo correspondente. Não há previsão de teste de carga ou auditoria de segurança nesta etapa.

## Gestão de defeitos

Os defeitos são registrados com reprodução, esperado/obtido, impacto, evidência e vínculo com a execução. Capturas e descrição dos passos demonstram o estado observado e o resultado da reprodução. Em comportamentos dinâmicos, o relato identifica a sequência de ações e os estados capturados. Correções disponibilizadas serão objeto de reteste. As evidências originais permanecem associadas à execução que as produziu.

## Entregáveis

Análise de requisitos; inventário; plano de testes; plano de execução e evidências; cenários e registros de execução; matriz de rastreabilidade; relatório de bugs; relatórios gerados; capturas e registro de bloqueios e investigações.
