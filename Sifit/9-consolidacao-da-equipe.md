# Consolidação das evidências da equipe

[← Índice](README.md) · [Registro dos 73 casos](evidencias/registro-equipe.md)

**Data:** 18/11/2026 · **Situação:** análise documental concluída; revisão das mídias iniciada; persistência não verificada.

## Fonte e dimensão

Material de Felipe Pestana, [Pestanadev/extensao-qa — SIFIT](https://github.com/Pestanadev/extensao-qa/tree/82b552089584394795036768a169cfb24206cc51/SIFIT), revisão `82b552089584394795036768a169cfb24206cc51`. Foram lidos o README, os quatro documentos principais e os 37 arquivos de cenários SIFIT. O conteúdo OrangeHRM herdado do exemplo não integra esta contagem.

| Indicador da fonte | Quantidade |
| --- | ---: |
| Arquivos de cenários | 37 |
| Casos identificados | 73 |
| Links JAM distintos | 73 |
| Links classificados como vídeo | 70 |
| Links classificados como print | 3 |
| Resultados “A confirmar” | 70 |
| Resultados “FALHOU” | 2 |
| Resultado “PARCIAL” | 1 |
| Bugs descritos pelo autor | 3 |

Os 73 casos não equivalem a 73 vídeos novos nem a 73 testes aprovados. Vários casos agrupam operações de CRUD. Os links recebidos já constituem o acervo da equipe e serão reaproveitados após avaliação. As 15 verificações históricas locais permanecem separadas, pois ainda não houve conciliação de duplicidades, ambientes e datas.

## Revisão das evidências

Duas mídias foram inspecionadas parcialmente no navegador. As outras 71 aguardam revisão individual. O [registro da equipe](evidencias/registro-equipe.md) distingue resultado informado pelo autor, observação local e verificação no banco.

| Caso | Constatação local | Limite da conclusão |
| --- | --- | --- |
| FP-CT-31 — Perguntas | A 0:32 aparece “Erro ao salvar pergunta” | Cadastro e alteração precisam de resultados separados. O bug da fonte descreve falha na edição; o título do caso menciona cadastro |
| FP-CT-56 — Planos | A 0:57 aparece “Erro ao deletar Plano”, após a confirmação de exclusão visível a 0:52 | Falha observada na tentativa de exclusão; regra aplicável, vínculo impeditivo e causa ainda não determinados. Cadastro, alteração e inativação não receberam aprovação nesta revisão |

As linhas do tempo possuem marcadores HTTP 500. A associação entre requisição, operação e causa exige análise dos detalhes técnicos. A falha de exclusão de plano não está entre os três bugs descritos pelo autor; permanece como ocorrência em análise, sem duplicar o relatório histórico de defeitos.

Os bugs da fonte recebem prefixo FP: FP-BUG-01 (botão junto a Competência), FP-BUG-02 (criação de modelo de ficha) e FP-BUG-03 (edição de pergunta). Não há consolidação numérica com os cinco bugs locais antes da comparação de reprodução e contexto. A recuperação de senha, por exemplo, já possui ocorrência local e também aparece entre os casos recebidos.

## Ambientes e banco

As duas mídias inspecionadas identificam o domínio `sifitalfa.centrion.com.br`. A exploração histórica local utilizou `sifit.centrion.com.br`. Essa diferença impede presumir que os dados, versões e configurações são os mesmos.

O colega relatou encontrar tabelas de comércio eletrônico e divergência na quantidade de produtos no esquema consultado. Esse relato não foi confirmado por consulta nesta revisão. Diferenças de esquema, academia, filtros, datas ou ambiente podem explicar divergências; a estrutura incorreta do banco ainda não está comprovada.

Não há comprovação de persistência concluída para os casos recebidos. A conferência depende da identificação da instância, esquema, academia e chaves correspondentes ao ambiente gravado. Uma consulta atual pode comprovar o estado atual de um registro, mas não recupera sozinha o estado anterior de uma edição ou exclusão histórica. Operações sem registro correlacionável podem exigir nova execução pontual, documentada por prints da interface e do banco.

## Cobertura e lacunas

O relacionamento documental alcança 42 dos 46 requisitos locais. Isso indica correspondência de assunto, sem demonstrar execução integral ou aprovação. RF05 (presenças), RF06 (geração de aulas Box), RF07 (clientes) e RF08 (matrículas) não possuem caso explicitamente correspondente nesta relação.

A própria análise do colega aponta pendências em clientes/alunos, edição de atividade, senha inválida e comparação com o banco. Outros módulos e operações, incluindo pedidos e aulas experimentais, são citados como pontos de confirmação. Casos rotulados apenas como “cadastro” não comprovam edição ou exclusão. O caso de relatórios também não comprova isoladamente os sete relatórios locais.

| Módulo da fonte | Casos recebidos | RF relacionado |
| --- | --- | --- |
| Login | FP-CT-01, FP-CT-02, FP-CT-03 | RF01 |
| Dashboard | FP-CT-04, FP-CT-05 | RF02, RF03, RF04 |
| Notificações | FP-CT-06 | RF46 |
| Financeiro | FP-CT-07, FP-CT-08, FP-CT-09, FP-CT-10, FP-CT-11 | RF02, RF34, RF21 |
| Treinos | FP-CT-12 | RF44 |
| Configurações | FP-CT-13, FP-CT-14, FP-CT-15, FP-CT-16, FP-CT-17, FP-CT-18, FP-CT-19 | RF43 |
| Inteligência e Automação | FP-CT-20, FP-CT-21, FP-CT-22, FP-CT-23 | RF42, RF41 |
| Atividades | FP-CT-24, FP-CT-25, FP-CT-26 | RF33 |
| Produtos | FP-CT-27, FP-CT-44 | RF35 |
| Aplicativo | FP-CT-28, FP-CT-29 | RF45 |
| Bandeiras de Cartão | FP-CT-30, FP-CT-53 | RF28 |
| Perguntas | FP-CT-31, FP-CT-32, FP-CT-33 | RF40 |
| Categorias | FP-CT-34, FP-CT-35, FP-CT-36 | RF39 |
| Modelos de Análise | FP-CT-37, FP-CT-38, FP-CT-39, FP-CT-40 | RF38 |
| Fichas de Análise | FP-CT-41 | RF37 |
| Enquetes | FP-CT-42, FP-CT-43 | RF36 |
| Tipos de Documentos | FP-CT-45, FP-CT-46 | RF32 |
| Fornecedores | FP-CT-47 | RF31 |
| Funções | FP-CT-48 | RF30 |
| Colaboradores | FP-CT-49, FP-CT-50 | RF29 |
| Turmas | FP-CT-51, FP-CT-52, FP-CT-59 | RF17, RF19 |
| Tipos de Pagamento | FP-CT-54 | RF27 |
| Modelos de Contrato | FP-CT-55 | RF26 |
| Planos | FP-CT-56 | RF25 |
| Grupos | FP-CT-57 | RF16 |
| Prospecção | FP-CT-58 | RF24 |
| Categorias de Crossfit | FP-CT-60 | RF18 |
| Objetivos de Treino | FP-CT-61 | RF15 |
| Grupos Musculares | FP-CT-62, FP-CT-63 | RF14 |
| Biblioteca de Exercícios | FP-CT-64, FP-CT-65 | RF13 |
| Fichas de Treino | FP-CT-66, FP-CT-67 | RF12 |
| Contas a Receber | FP-CT-68 | RF10 |
| Contas a Pagar | FP-CT-69 | RF11 |
| Caixas | FP-CT-70 | RF20 |
| Avaliações | FP-CT-71 | RF09 |
| Despesas Fixas | FP-CT-72 | RF22 |
| Relatórios | FP-CT-73 | RF23 |

“Modelos/Fichas de Análise” foram associados provisoriamente à anamnese. A confirmação depende da mídia e da nomenclatura do ambiente.

## Pendências de consolidação

| Pendência | Estado |
| --- | --- |
| Revisão das 73 mídias e classificação por operação | Iniciada: duas amostras parciais |
| Conciliação com os 15 resultados históricos locais | Pendente |
| Identificação do banco correspondente ao ambiente gravado | Pendente |
| SELECT e comprovação de persistência dos registros correlacionáveis | Não executados |
| Dados usados no bug de modelo de ficha | Campo incompleto no relato da fonte |
| Classificação de cadastro/edição de perguntas e falha ao excluir plano | Em análise |
| Conclusão do relatório recebido | Ainda contém campo a preencher na fonte |
| Novas capturas | Restritas às lacunas após revisão; quantidade não fechada |

Os 22 fluxos locais permanecem como referência de cobertura. Não representam uma obrigação de repetir integralmente o material recebido. Novas evidências serão em prints, conforme a orientação adicional informada para o trabalho; os vídeos existentes continuam aproveitáveis.

## Materiais acadêmicos consultados

Os seis PDFs fornecidos foram examinados. Os materiais sobre princípios, processo e erro/defeito/falha sustentam priorização, rastreabilidade e comparação entre resultado esperado e observado.

Na apresentação do segundo bimestre, a página 4 descreve a documentação SIFIT individual; a página 5 descreve separadamente o trabalho em grupo do TCC, incluindo manual, sistema/banco e vídeo. Essas duas atividades não foram tratadas como uma única exigência. A organização atual em grupo e a aceitação de prints seguem a orientação posterior relatada pelo integrante.

Revisão documental independente realizada com Claude, sem alteração dos arquivos da fonte ou consulta ao banco. A inspeção das duas mídias e o registro de suas observações integram esta consolidação.
