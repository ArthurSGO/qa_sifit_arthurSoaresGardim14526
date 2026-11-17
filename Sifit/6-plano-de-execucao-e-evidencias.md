# Plano de execução e evidências · Sifit

[← Índice](README.md) · [Inventário e cobertura](5-matriz-de-rastreabilidade.md) · [Execuções](4-relatorio-de-execucao.md)

**Data:** 17/11/2026 · **Situação:** planejado, ainda não executado.

## Dimensionamento

| Evidência | Situação |
| --- | --- |
| Vídeos | Não previstos |
| Capturas existentes | 8 disponíveis |
| Consultas, autenticação, controles e relatórios | 12 capturas adicionais previstas, PF01–PF12 |
| Operações dos 22 fluxos funcionais | Conjuntos de prints da interface e do banco; quantidade conforme as operações efetivamente disponíveis e executadas |

Os 22 fluxos são agrupamentos de testes, não quantidades de arquivos. As 12 capturas PF01–PF12 não incluem os prints de comprovação dos CRUDs. O total de imagens será consolidado na execução; não há cota de capturas por requisito ou por tela.

## Comprovação de operações persistentes

Os fluxos incluem cadastro, consulta, alteração e exclusão ou cancelamento quando essas ações estiverem disponíveis. A evidência relaciona a operação realizada na interface ao mesmo identificador no banco: registro criado, valores alterados, vínculos e estado após exclusão ou cancelamento. O resultado de persistência fica pendente quando a consulta ao banco não estiver disponível. As imagens da interface e do banco podem estar separadas ou na mesma captura, desde que o identificador e o estado do registro estejam legíveis e correlacionados.

Cancelamento e exclusão são avaliados conforme a ação e o efeito efetivamente encontrados. Editores e ações posteriores ao cadastro, ainda não observados em listas vazias, permanecem como pontos de confirmação dentro do respectivo fluxo. Acesso ao banco foi confirmado; tabelas, chaves e consultas ainda precisam de mapeamento.


| Operação | Evidência na interface | Evidência no banco |
| --- | --- | --- |
| Cadastro | Registro salvo, com identificação e valores informados | Registro criado, identificado pela chave e pelos campos da massa de teste |
| Consulta | Registro reaberto ou localizado pelos filtros | Correspondência entre o identificador e os dados consultados |
| Alteração | Mesmo registro com o valor atualizado | Mesma chave, campo alterado e referências correspondentes |
| Exclusão ou cancelamento | Resultado da operação na listagem ou no detalhe | Ausência do registro ou alteração de estado/flag, conforme a implementação |

A evidência de cadastro pode também demonstrar a consulta. O estado anterior de uma alteração pode ser comprovado pela captura da etapa anterior. Resultados e passos registrados complementam as imagens, sem exigir uma captura por clique.
## Fluxos funcionais com evidências em prints

Cada fluxo reúne operações relacionadas e um conjunto de capturas. Os prints associam o resultado na interface à consulta do mesmo registro no banco. Todos os fluxos abaixo estão não executados, salvo as verificações parciais já registradas no relatório histórico.

| ID | RF | Fluxo | Operações e evidência no banco |
| --- | --- | --- | --- |
| FL01 | RF16, RF25 | Grupos e planos | Cadastro, consulta, alteração e exclusão disponíveis; vínculo grupo/plano; modalidades de cobrança e valores salvos |
| FL02 | RF07 | Clientes | Cadastro, pesquisa, edição e exclusão de cliente de teste; identificador e campos persistidos |
| FL03 | RF08 | Matrículas | Cadastro, consulta, edição, cancelamento e exclusão disponíveis; vínculos com cliente/plano, datas, valores e contas geradas |
| FL04 | RF04, RF05 | Check-in e presenças | Entrada e saída manuais, tentativa duplicada, consulta por período; evento e identificação do cliente no banco |
| FL05 | RF09 | Avaliações físicas | Agendamento, alteração, realização, consulta e exclusão disponíveis; medidas, estado e vínculo com aluno; resultado/PDF e comparação quando disponíveis |
| FL06 | RF14, RF13 | Grupos musculares e exercícios | Cadastro, consulta, alteração e exclusão disponíveis; vínculo do exercício ao grupo e referência de mídia |
| FL07 | RF15, RF44, RF12 | Objetivos, modelos e fichas de treino | Cadastro de objetivo/modelo, aplicação à ficha, composição de exercícios e consulta; edição e exclusão conforme ações disponíveis; vínculos e conteúdo persistidos |
| FL08 | RF17 | Turmas | Cadastro, edição e exclusão; horários, dias, plano e estado persistidos |
| FL09 | RF18, RF19, RF06 | Categorias Crossfit, modalidades, turmas Box e aulas | Cadastro, edição e exclusão disponíveis; geração de aulas e repetição da geração; vínculos, datas e ausência de duplicação |
| FL10 | RF31, RF32 | Fornecedores e tipos de documentos | Cadastro, consulta, alteração e exclusão disponíveis; aplicação do documento e dados do fornecedor |
| FL11 | RF10 | Contas a receber | Cadastro, consulta, alteração/recebimento e exclusão disponíveis; valores, vencimento, estado, cliente e efeitos no caixa de teste |
| FL12 | RF22, RF11 | Despesas fixas e contas a pagar | Cadastro, consulta, alteração/baixa e exclusão disponíveis; fornecedor, recorrência, valores e estado; geração periódica conforme execução disponível |
| FL13 | RF20 | Caixa | Abertura, consulta e fechamento; contas associadas, datas, valores e estado. Reabertura apenas se a ação estiver disponível |
| FL14 | RF28, RF27 | Bandeiras e tipos de pagamento | Cadastro e uso no formulário financeiro; taxas, parcelas, estado e vínculo com bandeira; edição/exclusão conforme ações disponíveis |
| FL15 | RF30, RF29 | Funções, permissões e colaboradores | Cadastro, edição, associação/remoção de função e consulta; autorização com conta de teste e vínculos persistidos; exclusão apenas onde disponível |
| FL16 | RF24 | Prospecção | Cadastro, pesquisa, edição de estágio e exclusão de lead; dados e transição de estado no banco |
| FL17 | RF26 | Modelos de contrato | Cadastro, consulta, variáveis e preview; edição e exclusão conforme ações disponíveis; texto e estado persistidos |
| FL18 | RF33, RF35, RF34 | Atividades, produtos e pontuação | Cadastro e alterações disponíveis; produto de venda/pontuação, campanha, datas e vínculos de resgate; exclusão conforme ações disponíveis |
| FL19 | RF36 | Enquetes | Cadastro, consulta, alteração e exclusão disponíveis; pergunta e alternativas no banco. Votação no app condicionada a conta e ambiente de teste |
| FL20 | RF39, RF40, RF38, RF37 | Categorias, perguntas, modelos e fichas de anamnese | Cadastro, edição e exclusão disponíveis; montagem do modelo, aplicação ao aluno e respostas; ordem, obrigatoriedade, vínculos e estado persistidos |
| FL21 | RF43 | Configurações locais | Alteração de uma configuração não sensível, consulta após recarregar e restauração; valor correspondente no banco. Dispositivos, credenciais e integrações externas não incluídos |
| FL22 | RF41, RF42 | Automação e resultados no painel | Configuração com canal Apenas painel, execução e consulta do resultado; configuração, execução e efeitos no banco. Condicionado à disponibilidade dessa modalidade sem envio externo |

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
| BUG-001 — Recuperação de senha | Captura da tela | Captura existente e descrição da reprodução; capturas de antes/depois se necessárias ao registro da nova execução |
| BUG-002 — Título do Dashboard | Captura do título | Sem captura adicional específica prevista |
| BUG-003 — Unidade do IMC | Captura do rótulo e cálculo | Sem captura adicional específica prevista; pode ser reobservado em FL05 |
| BUG-004 — Ano negativo no vencimento | Captura da situação financeira | Sem captura adicional específica prevista; origem a investigar em FL02/FL03 |
| BUG-005 — Conteúdo de demonstração no perfil | Captura do conteúdo | Sem captura adicional específica prevista; pode ser reobservado em PF12 |

## Bloqueios e cobertura condicionada

| Área | Limitação conhecida | Tratamento na execução |
| --- | --- | --- |
| RF21 — Pagar.me | Sandbox, credenciais e origem dos dados não confirmados | Testes transacionais bloqueados; inventário mantido. Sem captura de execução prevista enquanto bloqueado |
| RF45 — Aplicativo | Envio de aviso destinado a Todos os alunos; grupo isolado e sessão de aluno não disponíveis | Envio e moderação bloqueados até ambiente dedicado. Sem captura de execução prevista enquanto bloqueado |
| RF04/RF43 — QR, biometria e catraca | Hardware e configuração de teste não disponíveis | Cobertura manual em FL04; integrações com dispositivos bloqueadas |
| RF41 — Automações em desenvolvimento | Quatro automações identificadas como Em desenvolvimento | Indisponibilidade registrada; FL22 abrange apenas o recurso executável no painel |
| RF43 — WhatsApp e gateways | Integrações desconectadas ou sem configuração de teste | Fora da alteração local de FL21; execução externa bloqueada |
| Editor posterior de ficha/modelo, objetivos, bandeiras, produtos e contrato | Parte das ações não estava visível em listas vazias ou sem nome acessível | Confirmação durante o fluxo correspondente; sem presumir edição/exclusão não observadas |

Um fluxo bloqueado permanece sem execução e sem evidência de resultado, com motivo registrado. A presente previsão não declara cobertura integral de todos os estados, integrações ou combinações de campos.
