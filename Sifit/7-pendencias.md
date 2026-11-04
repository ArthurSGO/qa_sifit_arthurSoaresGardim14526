# Pendências, investigações e melhorias

[← Índice](README.md) · [Bugs confirmados](3-relatorio-de-bugs.md)

## Investigações abertas

| ID | Observação | Por que ainda não é conclusão | Próxima ação |
| --- | --- | --- | --- |
| INV-001 | Inicialmente Sem Matrículas 6 versus modal 0; revisão mostrou 6/6 | Divergência não se repetiu; possível estado transitório, sem causa comprovada | Não classificar como bug confirmado; conciliar origem com banco; CT-RF02-02 |
| INV-002 | Desistências: total 2, lista vazia | Pode haver diferença entre agregado e consulta | Conciliar período, status, academia e dados |
| INV-003 | Personais: ícones apontam /visualizar-cliente/{id} | Pode haver identidade compartilhada ou destino incorreto | Confirmar vínculo colaborador/cliente; não inferir pelo ID igual |
| INV-004 | Check-in: Filtros não mostrou mudança ao clique | Falta gravação e confirmação do comportamento previsto | Reproduzir visualmente e registrar no JAM |
| INV-005 | Perfil de cliente: Editar objetivos não respondeu visivelmente | Fluxo/regra não confirmados e sem gravação | Repetir em massa isolada e conferir implementação/banco |
| INV-006 | Check-ins no perfil e tabela de presenças divergiram | Podem ser fontes distintas | Mapear eventos, presença, entrada/saída e datas |
| INV-007 | Configurações: dias de ausência com valor negativo preexistente | Não foi testado se o formulário aceita salvar negativo | Validar limite em ambiente isolado e origem no banco |
| INV-008 | Tipos de pagamento: ativos/uso em outros formulários a conciliar | Pode haver regra legada ou filtro diferente | Conferir status e elegibilidade em matrícula/contas |
| INV-009 | Contas a Pagar: totais zerados com linha pendente | Critérios dos indicadores não conhecidos | Comparar período, status, valores e consultas |
| INV-010 | Pagar.me: valores -- e gráfico preenchido | Integração e fonte não confirmadas | Validar configuração e sandbox; não realizar saque |
| INV-011 | Produtos/Pontuação: botões sem nome na acessibilidade | Não comprova ausência visual de dados | Inspecionar visual e teclado; corrigir nomes acessíveis se confirmado |
| INV-012 | Cadastro de pergunta não mostrou categoria | Vínculo pode ser definido em outro fluxo | Verificar edição, montador e esquema |
| INV-013 | Login fornecido identifica Jair | Não comprova erro de identidade | Confirmar login → colaborador → academia no banco |
| INV-014 | + Modalidade sem dados não mostrou retorno visível | Pode ser ação de salvar do formulário inline | Confirmar validação e semântica em ambiente de teste |
| INV-015 | Configurar Aniversariantes mostrou critérios e preview de risco de evasão | Pode haver formulário genérico ou mapeamento incorreto | Confirmar regra e efeito no banco, sem executar envio real |

## Funcionalidades declaradas indisponíveis

Na Central de Automações, Avaliações vencendo, Frequência em queda, Financeiro diário e Cobranças automáticas estão identificadas como **Em desenvolvimento**. Registrar como indisponibilidade explícita; não criar resultado aprovado nem defeito de implementação baseado apenas nessa ausência. Se o escopo contratual exigir essas funções, discutir a lacuna com o responsável.

O WhatsApp estava desconectado e sem configuração. Conectar, Testar, Enviar e Desconectar estavam desabilitados. Isso é uma pré-condição ausente, não prova de defeito.

## Caminhos ainda não alcançados

- Editor posterior à criação de ficha e modelo de treino, com lista inicial vazia.
- Etapas de seleção de modelo/respostas/conclusão da anamnese.
- Detalhes de aula, reservas e capacidade após geração no Box.
- PDFs dos sete relatórios; comparação de avaliações e links de resultado. Os filtros foram inspecionados.
- Execução e histórico de automações; coerência da configuração de Aniversariantes.
- Persistência do vínculo de funções do colaborador; suas quatro abas foram inspecionadas.
- Ações de linhas ausentes em bandeiras, objetivos e modelos; moderação sem posts/denúncias de teste.
- Fluxos financeiros de abertura/fechamento/reabertura, baixas e integrações.
- Todos os efeitos persistentes de cadastrar, editar, cancelar e excluir.

Esses caminhos dependem de massa, gravação, banco ou operações que não foram concluídas. A visita de todos os itens do menu não os transforma em testados.

## Melhorias propostas

| ID | Proposta | Evidência ou motivação |
| --- | --- | --- |
| MEL-001 | Arredondar apresentação do IMC sem perder precisão armazenada | Exemplo exibiu muitas casas decimais |
| MEL-002 | Melhorar contraste no SifitBox em tema escuro | Cartões brancos com textos muito claros na inspeção |
| MEL-003 | Ajustar layout da situação financeira do cliente | Texto de próximo vencimento/total quebrava excessivamente no viewport inspecionado |
| MEL-004 | Diferenciar carregamento, vazio e erro | Indicadores frequentemente aparecem zerados antes dos dados |
| MEL-005 | Mensagens claras em botões sem retorno e obrigatoriedade | Investigações de Filtros/Objetivos/Modalidade e variação na validação de login vazio |
| MEL-006 | Clarificar destino de Segurança e Preferências | Ambos apontam /configuracoes; não foi encontrado fluxo próprio de segurança nesse destino |

## Informações acadêmicas pendentes

Nome do aluno e integrantes; curso/turma; instituição; professor; título oficial do projeto; cronograma e critérios de avaliação. Não foram preenchidos com dados presumidos.
