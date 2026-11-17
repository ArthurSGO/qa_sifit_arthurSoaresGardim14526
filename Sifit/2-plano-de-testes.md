# Plano de testes · Sifit

[← Índice](README.md) · [Requisitos](1-analise-de-requisitos.md) · [Cobertura](5-matriz-de-rastreabilidade.md)

## Identificação

| Item | Definição |
| --- | --- |
| Projeto | Extensão — documentação e testes manuais do Sifit |
| Ambiente | https://sifit.centrion.com.br/login |
| Versão do sistema | Não informada |
| Levantamento inicial | 21/10/2026 |
| Revisão de escopo | 17/11/2026 |
| Responsável acadêmico | Não informado |
| Plataforma observada | Windows; navegador integrado do Codex; versão não coletada |
| Estado | Avaliação parcial da interface; resultados registrados |

## Objetivo

Documentar as funcionalidades observadas e os resultados de uma avaliação manual da interface, com rastreabilidade entre verificações, defeitos e evidências.

## Escopo da entrega atual

| Componente | Abrangência |
| --- | --- |
| Inventário funcional | 44 destinos do menu, autenticação e controles globais, organizados em 46 áreas funcionais |
| Execução | 15 verificações realizadas em autenticação, Página Inicial, Dashboard, clientes, matrículas, avaliações, configurações e perfil |
| Resultados | 9 aprovados, 5 reprovados e 1 inconclusivo |
| Defeitos | 5 bugs documentados com reprodução, impacto e capturas |
| Evidências | 8 capturas existentes; vídeo complementar pendente para o BUG-001 |

O inventário descreve a interface e não representa uma exigência de execução de todos os fluxos. As [verificações complementares](cenarios/complementares.md) são possibilidades de ampliação, fora desta etapa.

## Fora do escopo atual

Execução exaustiva de cadastros e operações CRUD; auditoria do banco; conciliação integral de indicadores; homologação de integrações, dispositivos e aplicativo; testes de carga, segurança e compatibilidade entre navegadores.

O acesso ao banco foi confirmado pelo MySQL Workbench em 22/10/2026. A análise do esquema e a validação direta de persistência não foram realizadas e não são pré-condições para os resultados de interface já registrados.

## Técnicas aplicadas

Exploração da interface; verificações funcionais positivas e negativas; comparação entre comportamento esperado e observado; conferência de cálculo visual e consistência de apresentação.

## Evidências

| Registro | Evidência | Situação |
| --- | --- | --- |
| BUG-001 — Recuperação de senha | Vídeo do clique e da ausência de resposta | Pendente de reprodução e gravação |
| BUG-002 — Título do Dashboard | Captura da tela | Disponível |
| BUG-003 — Unidade do IMC | Captura do rótulo e cálculo | Disponível |
| BUG-004 — Ano negativo no vencimento | Captura da situação financeira | Disponível |
| BUG-005 — Conteúdo de demonstração no perfil | Captura do conteúdo exibido | Disponível |
| Demais verificações executadas | Capturas e observações registradas no relatório | Disponíveis conforme índice de evidências |

Vídeos complementam defeitos cujo comportamento não fica demonstrado em uma imagem. Não há uma gravação prevista por caso, requisito ou área funcional. Retestes ficam associados à correção do defeito correspondente.

## Situação dos resultados

| Estado | Quantidade | Definição |
| --- | ---: | --- |
| Aprovado | 9 | Objetivo da verificação atendido |
| Reprovado | 5 | Divergência documentada em bug |
| Inconclusivo | 1 | Divergência inicial não reproduzida; origem não confirmada |

As verificações inconclusivas e as limitações permanecem identificadas no relatório. Não há execução integral ou homologação do sistema declarada nesta entrega.

## Entregáveis

Análise de requisitos; inventário de interface; plano de testes; cenários executados; matriz de rastreabilidade; relatório de bugs; relatório parcial de execução; índice de evidências e observações complementares. Documentos em Markdown e capturas em PNG.
