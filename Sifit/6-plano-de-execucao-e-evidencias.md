# Plano de execução e evidências · Sifit

[← Índice](README.md) · [Inventário e cobertura](5-matriz-de-rastreabilidade.md) · [Execuções](4-relatorio-de-execucao.md)

**Data:** 17/11/2026 · **Situação:** planejado, ainda não executado.

## Dimensionamento

| Evidência | Existente | Prevista nesta etapa |
| --- | ---: | ---: |
| Gravações de fluxos funcionais | 0 | 22 |
| Vídeo complementar de defeito | 0 | 1 |
| Capturas de tela | 8 | 12 adicionais |

O planejamento totaliza 23 vídeos e 20 capturas, incluindo as 8 imagens existentes. As gravações agrupam operações relacionadas; não há arquivo separado por botão, operação CRUD ou caso de teste. A contagem é uma estimativa de organização desta execução, sujeita aos bloqueios e defeitos encontrados, e não uma quantidade prescrita pela referência acadêmica.

## Comprovação de operações persistentes

Os fluxos incluem cadastro, consulta, alteração e exclusão ou cancelamento quando essas ações estiverem disponíveis. A evidência relaciona a operação realizada na interface ao mesmo identificador no banco: registro criado, valores alterados, vínculos e estado após exclusão ou cancelamento. O resultado de persistência fica pendente quando a consulta ao banco não estiver disponível.

Cancelamento e exclusão são avaliados conforme a ação e o efeito efetivamente encontrados. Editores e ações posteriores ao cadastro, ainda não observados em listas vazias, permanecem como pontos de confirmação dentro do respectivo fluxo. Acesso ao banco foi confirmado; tabelas, chaves e consultas ainda precisam de mapeamento.

## Gravações funcionais

Uma gravação pode comprovar várias entidades e operações relacionadas. Todos os fluxos abaixo estão não executados, salvo as verificações parciais já registradas no relatório histórico.

| ID | RF | Fluxo | Operações e evidência no banco |
| --- | --- | --- | --- |
| VF01 | RF16, RF25 | Grupos e planos | Cadastro, consulta, alteração e exclusão disponíveis; vínculo grupo/plano; modalidades de cobrança e valores salvos |
| VF02 | RF07 | Clientes | Cadastro, pesquisa, edição e exclusão de cliente de teste; identificador e campos persistidos |
| VF03 | RF08 | Matrículas | Cadastro, consulta, edição, cancelamento e exclusão disponíveis; vínculos com cliente/plano, datas, valores e contas geradas |
| VF04 | RF04, RF05 | Check-in e presenças | Entrada e saída manuais, tentativa duplicada, consulta por período; evento e identificação do cliente no banco |
| VF05 | RF09 | Avaliações físicas | Agendamento, alteração, realização, consulta e exclusão disponíveis; medidas, estado e vínculo com aluno; resultado/PDF e comparação quando disponíveis |
| VF06 | RF14, RF13 | Grupos musculares e exercícios | Cadastro, consulta, alteração e exclusão disponíveis; vínculo do exercício ao grupo e referência de mídia |
| VF07 | RF15, RF44, RF12 | Objetivos, modelos e fichas de treino | Cadastro de objetivo/modelo, aplicação à ficha, composição de exercícios e consulta; edição e exclusão conforme ações disponíveis; vínculos e conteúdo persistidos |
| VF08 | RF17 | Turmas | Cadastro, edição e exclusão; horários, dias, plano e estado persistidos |
| VF09 | RF18, RF19, RF06 | Categorias Crossfit, modalidades, turmas Box e aulas | Cadastro, edição e exclusão disponíveis; geração de aulas e repetição da geração; vínculos, datas e ausência de duplicação |
| VF10 | RF31, RF32 | Fornecedores e tipos de documentos | Cadastro, consulta, alteração e exclusão disponíveis; aplicação do documento e dados do fornecedor |
| VF11 | RF10 | Contas a receber | Cadastro, consulta, alteração/recebimento e exclusão disponíveis; valores, vencimento, estado, cliente e efeitos no caixa de teste |
| VF12 | RF22, RF11 | Despesas fixas e contas a pagar | Cadastro, consulta, alteração/baixa e exclusão disponíveis; fornecedor, recorrência, valores e estado; geração periódica conforme execução disponível |
| VF13 | RF20 | Caixa | Abertura, consulta e fechamento; contas associadas, datas, valores e estado. Reabertura apenas se a ação estiver disponível |
| VF14 | RF28, RF27 | Bandeiras e tipos de pagamento | Cadastro e uso no formulário financeiro; taxas, parcelas, estado e vínculo com bandeira; edição/exclusão conforme ações disponíveis |
| VF15 | RF30, RF29 | Funções, permissões e colaboradores | Cadastro, edição, associação/remoção de função e consulta; autorização com conta de teste e vínculos persistidos; exclusão apenas onde disponível |
| VF16 | RF24 | Prospecção | Cadastro, pesquisa, edição de estágio e exclusão de lead; dados e transição de estado no banco |
| VF17 | RF26 | Modelos de contrato | Cadastro, consulta, variáveis e preview; edição e exclusão conforme ações disponíveis; texto e estado persistidos |
| VF18 | RF33, RF35, RF34 | Atividades, produtos e pontuação | Cadastro e alterações disponíveis; produto de venda/pontuação, campanha, datas e vínculos de resgate; exclusão conforme ações disponíveis |
| VF19 | RF36 | Enquetes | Cadastro, consulta, alteração e exclusão disponíveis; pergunta e alternativas no banco. Votação no app condicionada a conta e ambiente de teste |
| VF20 | RF39, RF40, RF38, RF37 | Categorias, perguntas, modelos e fichas de anamnese | Cadastro, edição e exclusão disponíveis; montagem do modelo, aplicação ao aluno e respostas; ordem, obrigatoriedade, vínculos e estado persistidos |
| VF21 | RF43 | Configurações locais | Alteração de uma configuração não sensível, consulta após recarregar e restauração; valor correspondente no banco. Dispositivos, credenciais e integrações externas não incluídos |
| VF22 | RF41, RF42 | Automação e resultados no painel | Configuração com canal Apenas painel, execução e consulta do resultado; configuração, execução e efeitos no banco. Condicionado à disponibilidade dessa modalidade sem envio externo |

## Capturas adicionais

| ID | RF | Resultado a registrar |
| --- | --- | --- |
| PF01 | RF01 | Estado da sessão após fechar/reabrir o navegador com Manter conectado; resultado conforme regra disponível |
| PF02 | RF02 | Página Inicial em período selecionado, com indicadores carregados |
| PF03 | RF02 | Detalhamento de indicador no mesmo período; resultado da comparação e eventual divergência |
| PF04 | RF03 | Dashboard e gráficos carregados |
| PF05 | RF23 | PDF de Avaliações gerado com período identificado |
| PF06 | RF23 | PDF de Clientes gerado com período identificado |
| PF07 | RF23 | PDF de Colaboradores gerado com período identificado |
| PF08 | RF23 | PDF de Matrículas com filtros identificados |
| PF09 | RF23 | PDF de Contas a Receber com filtros identificados |
| PF10 | RF23 | PDF de Contas a Pagar com período identificado |
| PF11 | RF23 | PDF de Caixas com formato e período identificados |
| PF12 | RF46 | Resultado da verificação de tema e notificações; comportamento e destinos do menu da conta registrados na execução |

Os PDFs são artefatos da execução; as capturas registram sua geração e apresentação. Conferências de dados ficam relacionadas aos registros de teste dos fluxos funcionais. Uma imagem pode servir a mais de uma verificação; falhas ou resultados distintos podem exigir evidências adicionais.

## Defeitos já registrados

| Bug | Evidência disponível | Complemento previsto |
| --- | --- | --- |
| BUG-001 — Recuperação de senha | Captura da tela | VB01: vídeo do clique e da ausência de resposta, se reproduzido |
| BUG-002 — Título do Dashboard | Captura do título | Sem gravação adicional prevista |
| BUG-003 — Unidade do IMC | Captura do rótulo e cálculo | Sem gravação adicional prevista; pode ser reobservado em VF05 |
| BUG-004 — Ano negativo no vencimento | Captura da situação financeira | Sem gravação adicional prevista; origem a investigar em VF02/VF03 |
| BUG-005 — Conteúdo de demonstração no perfil | Captura do conteúdo | Sem gravação adicional prevista; pode ser reobservado em PF12 |

## Bloqueios e cobertura condicionada

| Área | Limitação conhecida | Tratamento na execução |
| --- | --- | --- |
| RF21 — Pagar.me | Sandbox, credenciais e origem dos dados não confirmados | Testes transacionais bloqueados; inventário mantido. Sem vídeo incluído na contagem atual |
| RF45 — Aplicativo | Envio de aviso destinado a Todos os alunos; grupo isolado e sessão de aluno não disponíveis | Envio e moderação bloqueados até ambiente dedicado. Sem vídeo incluído na contagem atual |
| RF04/RF43 — QR, biometria e catraca | Hardware e configuração de teste não disponíveis | Cobertura manual em VF04; integrações com dispositivos bloqueadas |
| RF41 — Automações em desenvolvimento | Quatro automações identificadas como Em desenvolvimento | Indisponibilidade registrada; VF22 abrange apenas o recurso executável no painel |
| RF43 — WhatsApp e gateways | Integrações desconectadas ou sem configuração de teste | Fora da alteração local de VF21; execução externa bloqueada |
| Editor posterior de ficha/modelo, objetivos, bandeiras, produtos e contrato | Parte das ações não estava visível em listas vazias ou sem nome acessível | Confirmação durante o fluxo correspondente; sem presumir edição/exclusão não observadas |

Uma gravação bloqueada permanece sem execução e sem evidência, com motivo registrado. A presente previsão não declara cobertura integral de todos os estados, integrações ou combinações de campos.
