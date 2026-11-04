# Sifit · Documentação e qualidade de software

> Projeto de extensão · Versão 0.1 · Levantamento inicial em 21/10/2026

Documentação do sistema de gestão de academias **Sifit**, organizada a partir da exploração da interface e do modelo acadêmico do professor.

**Estado da entrega:** 44 destinos do menu visitados, 46 requisitos catalogados, 267 casos especificados, 15 verificações executadas e 5 bugs registrados. Banco e gravações JAM ainda pendentes. A documentação é inicial; fluxos completos e todos os estados de cada botão ainda não estão homologados.

## Documentos principais

| Documento | Conteúdo |
| --- | --- |
| [1 · Análise de requisitos](1-analise-de-requisitos.md) | Capacidades observadas, atores e critérios propostos |
| [2 · Plano de testes](2-plano-de-testes.md) | Escopo, estratégia, prioridades, riscos e critérios de saída |
| [3 · Relatório de bugs](3-relatorio-de-bugs.md) | Reprodução, esperado/obtido, impacto e capturas |
| [4 · Relatório parcial de execução](4-relatorio-de-execucao.md) | Resultados reais e limites da etapa |
| [5 · Matriz de rastreabilidade](5-matriz-de-rastreabilidade.md) | RF → casos → execução → ocorrência |
| [6 · Roteiro banco e JAM](6-roteiro-banco-e-jam.md) | Preparação, consultas por ID e gravações CRUD |
| [7 · Pendências e melhorias](7-pendencias.md) | Suspeitas, indisponibilidades e caminhos não alcançados |
| [8 · Referência e metodologia](8-referencia-e-metodologia.md) | Fonte acadêmica e decisões de adaptação |
| [Evidências](evidencias/README.md) | Capturas estáticas e registro para vídeos |

## Inventário de telas, campos e botões

- [Acesso e Principal](inventario/01-acesso-e-principal.md)
- [Operação da academia](inventario/02-operacao.md)
- [Treinamento](inventario/03-treinamento.md)
- [Financeiro e Comercial](inventario/04-financeiro-e-comercial.md)
- [Gestão](inventario/05-gestao.md)
- [Saúde, Inteligência e Configurações](inventario/06-saude-inteligencia-configuracoes.md)

O inventário descreve filtros, campos, ações, observações e validações pendentes de cada módulo. As suítes de cenários estão ligadas pela matriz. Não há credenciais nos arquivos.

## Como usar

Começar pelo inventário para conhecer o sistema; consultar o requisito e os cenários do fluxo escolhido; executar com massa isolada; preencher evidências; atualizar o relatório de execução e os bugs. Para filmar operações e comprová-las no banco, seguir o roteiro específico.

## Próxima etapa

O acesso pela conexão salva no MySQL Workbench foi confirmado em 22/10/2026; o esquema ainda precisa ser mapeado e as regras do ambiente confirmadas. Executar criação, edição, cancelamento e exclusão com massa controlada, conferir os IDs e anexar os vídeos. Dados acadêmicos da capa também aguardam preenchimento.

As gravações podem começar pelos casos com pré-condições atendidas, enquanto os links são acrescentados ao [registro de evidências](evidencias/registro-de-evidencias.md). O [fluxo de gravação e atualização no Git](evidencias/fluxo-de-gravacao.md) orienta o uso do JAM e das cópias no Google Drive. Publicar a documentação em andamento não significa homologar os casos pendentes.
