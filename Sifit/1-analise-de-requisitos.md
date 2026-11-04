# Análise de requisitos · Sifit

[← Índice](README.md) · [Plano de testes](2-plano-de-testes.md)

> **Versão 0.1 — levantamento inicial por interface, em 21/10/2026.** Os requisitos abaixo são derivados dos controles observados e de critérios propostos para teste. Ainda precisam de validação com o responsável pelo sistema. Não constituem especificação oficial obtida do código ou banco.

## Objetivo e contexto

Documentar o sistema de gestão de academias Sifit e organizar a avaliação manual de sua qualidade para um projeto de extensão. O levantamento usa a interface web acessível pela conta fornecida e adapta a organização do exemplo do professor, sem transportar regras de RH do OrangeHRM para a academia.

## Atores e limites conhecidos

| Ator | Evidência e limite |
| --- | --- |
| Usuário autenticado | Conta fornecida abriu menus administrativos; a interface mostrou Jair. Vínculo entre login, colaborador e academia a confirmar no banco. |
| Admin/Normal/Sem login | Opções observadas no cadastro de colaborador; diferenças de autorização ainda não testadas. |
| Personal/Avaliador | Campos em funções e colaboradores; atuação observada em turma, ficha e avaliação. |
| Aluno/usuário do app | Entidade visível nos cadastros, check-ins, anamnese, notificações e postagens; aplicativo do aluno não foi acessado. |
| Responsável pela academia | Necessário para aprovar regras e validar efeitos financeiros, dispositivos e comunicações. |

## Requisitos funcionais

Cada item liga uma capacidade observada a um critério verificável. As ações destrutivas e operações externas permanecem planejadas.

### RF01 · Autenticação e sessão

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Entrar; Esqueci minha senha; Sair do sistema no menu da conta.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Persistência de Manter conectado após fechar e reabrir o navegador; expiração de sessão; diferentes perfis; recuperação de senha após correção.

[Cenários RF01](cenarios/RF01.md)

### RF02 · Página Inicial

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Ver detalhes; cartões de ausentes, sem matrícula, personais, matrículas e desistências; Ver análise completa; Cobrar agora; Enviar mensagem; Ver avaliações; Ver todas as mensalidades; Cobrar todos no WhatsApp; Ver agenda; Ver todos nas entradas e aniversários.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Conciliar indicadores com o banco e regras de período. Cartão Sem Matrículas mostrou 6 e modal inicialmente mostrou 0, mas na revisão exibiu 6 registros e total 6; a divergência inicial não se repetiu; desistências mostrou total 2 e lista vazia. Confirmar critérios antes de classificar causa. Atalhos de mensagem, exportação e registro financeiro não foram concluídos.

[Cenários RF02](cenarios/RF02.md)

### RF03 · Dashboard analítico

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Ver Inteligência; navegação global.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Validar origem, período, séries e agregações dos gráficos com o banco. Título registrado em BUG-002.

[Cenários RF03](cenarios/RF03.md)

### RF04 · Check-in

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Check-in manual; Escanear QR Code; Realizar check-in; Registrar entrada na linha; Ver todos nos presentes; notificações.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Executar entrada e saída em cliente de teste, duplicidade, matrícula inativa, unidade, visitante, QR e biometria. Investigar Filtros com gravação. Não foram registrados check-ins por esta exploração.

[Cenários RF04](cenarios/RF04.md)

### RF05 · Presenças

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Consultar e alternar períodos.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Usar intervalo com registros e comparar contagens, unidades, horários e fronteiras de datas com o banco.

[Cenários RF05](cenarios/RF05.md)

### RF06 · SifitBox — aulas

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Gerar aulas.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Geração baseada em turmas recorrentes, repetição sem duplicidade, vagas, reservas e ações de aula que só aparecem com dados.

[Cenários RF06](cenarios/RF06.md)

### RF07 · Clientes

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Cliente; visualizar; Deletar; no formulário, Cancelar e Cadastrar Cliente. Perfil: Alterar imagem, Alterar dados, Editar objetivos, Aplicar Anamnese, Enviar mensagem, Agendar avaliação, Registrar pagamento, Ver todas as presenças e Ver histórico completo.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Criar, alterar e excluir apenas massa isolada; verificar obrigatórios, documentos, foto, responsável, duplicidade e vínculos. Explicar divergências entre histórico de check-ins e presenças. Confirmar identidade da conta no banco. Não registrar senhas na documentação.

[Cenários RF07](cenarios/RF07.md)

### RF08 · Matrículas

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Cadastrar Matrícula (/adicionar-matricula); Visualizar; Cancelar matrícula; Deletar; Editar dentro da visualização; Salvar/Cancelar formulário.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Conferir geração de contas, datas, desconto, diária variável, período fixo, recorrência, renovação, personal/dependentes e anamnese após conclusão. Cancelamento e exclusão são operações diferentes.

[Cenários RF08](cenarios/RF08.md)

### RF09 · Avaliações físicas

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Cadastrar Avaliação; Alterar e Fazer Avaliação nas pendentes; Imprimir, Relatório completo (PDF), Visualizar, Link e Comparação nas realizadas; Deletar; Salvar/Cancelar nos formulários.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Validar agendamento, edição, realização, fórmulas aprovadas pelo responsável, unidades, arredondamento, formatos decimais, PDF, comparação e vínculos financeiros. Fórmulas corporais e interpretações clínicas não foram homologadas.

[Cenários RF09](cenarios/RF09.md)

### RF10 · Contas a Receber

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Conta; Visualizar; Deletar; Pesquisar cliente; Cancelar; Salvar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Confirmar estados Pendente/Recebido, resíduos, cópias, descontos/multas/juros, baixa parcial, conciliação com caixa e exclusão vinculada. Operações reais de recebimento ficam fora da execução atual.

[Cenários RF10](cenarios/RF10.md)

### RF11 · Contas a Pagar

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Conta; Visualizar; Deletar; Pesquisar fornecedor; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Conferir fornecedor/colaborador, categoria, documento, baixa parcial/total, vencimento, despesas fixas e caixa. Investigar totais zerados diante de conta pendente, respeitando os filtros.

[Cenários RF11](cenarios/RF11.md)

### RF12 · Fichas de Treino

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Cadastrar Ficha; Pesquisar aluno; Criar Nova Ficha; Usar Modelo de Ficha; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Criar ficha isolada para descobrir editor de exercícios, séries, repetições, impressão e ações de linha realmente disponibilizadas. Não presumir campos ou exclusão ainda não observados.

[Cenários RF12](cenarios/RF12.md)

### RF13 · Exercícios

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Adicionar por grupo; Visualizar; Deletar; Procurar imagem/vídeo; Salvar; Cancelar; Fechar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Persistir mídia de teste, limites e extensões; alteração de nome/mídia; integridade com ficha e grupo; tratamento de exclusão vinculada.

[Cenários RF13](cenarios/RF13.md)

### RF14 · Grupos Musculares

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Cadastrar grupo; Visualizar; Deletar; Escolher arquivo; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Tipos permitidos, imagem, nomes repetidos e exclusão quando há exercícios vinculados.

[Cenários RF14](cenarios/RF14.md)

### RF15 · Objetivos Treino

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Objetivo; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Cadastrar objetivo de teste e descobrir edição/exclusão disponíveis; vincular à ficha. Não assumir CRUD completo por analogia.

[Cenários RF15](cenarios/RF15.md)

### RF16 · Grupos

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Grupo; Visualizar; Deletar; Salvar Grupo; Cancelar; Fechar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Verificar impacto do grupo nos planos, home e caixa; exclusão com vínculos.

[Cenários RF16](cenarios/RF16.md)

### RF17 · Turmas

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Cadastrar Turma; Editar; Deletar; selecionar dias; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Horários iguais/invertidos, dias vazios, personal condicional, sobreposição e vínculos com plano.

[Cenários RF17](cenarios/RF17.md)

### RF18 · Categorias Crossfit

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Categoria; Editar; Deletar; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Atualização das datas, unicidade e exclusão com vínculos de exercícios.

[Cenários RF18](cenarios/RF18.md)

### RF19 · SifitBox — turmas e modalidades

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Botões + Modalidade e + Turma; ícones de editar e excluir nas duas listas.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Validar significado dos botões e mensagens de obrigatoriedade com massa isolada; edição, exclusão, limite de vagas e geração de aulas. Gravação não executada.

[Cenários RF19](cenarios/RF19.md)

### RF20 · Caixas

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Abrir Caixa; Visualizar; Imprimir; no fechamento Buscar Contas, Salvar, Cancelar e Fechar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Detalhar abertura, fechamento, reabertura, conferência e ajuste após criar ambiente financeiro de teste; conciliar contas e totais. Ações adicionais constam nas permissões, mas não foram executadas.

[Cenários RF20](cenarios/RF20.md)

### RF21 · Pagar.me

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Solicitar saque; Ver previsão; Ver recebíveis; Ver relatório completo; Ver extrato completo; Nova cobrança; Configurações; Ver todas as transações e demais Ver todas.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Confirmar sandbox e token com responsável; testar apenas nesse ambiente. Saques, cobranças, transferência e mudanças na integração não foram acionados.

[Cenários RF21](cenarios/RF21.md)

### RF22 · Despesas Fixas

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Despesa; Visualizar; Deletar; Salvar Despesa; Cancelar; Fechar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Geração das contas periódicas, datas, repetição sem duplicar e efeito de inativação.

[Cenários RF22](cenarios/RF22.md)

### RF23 · Relatórios

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Selecionar tipo por cartão ou lista; Gerar Relatório (PDF).

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Gerar PDFs dos sete tipos com massa conhecida e comparar linhas, totais e datas com consultas ao banco.

[Cenários RF23](cenarios/RF23.md)

### RF24 · Prospecção

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Adicionar Lead; Visualizar; Deletar; Salvar Lead; Cancelar; Fechar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Estágios e transições permitidas, duplicidades, contato inválido, edição e exclusão.

[Cenários RF24](cenarios/RF24.md)

### RF25 · Planos

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Plano; Visualizar; Deletar; adicionar benefício; Salvar Plano; Salvar também na Pagar.me quando disponível; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Persistência de cada tipo, datas e parcelas, benefícios, dependentes, personal e conciliação do ranking. Integração Pagar.me apenas em sandbox.

[Cenários RF25](cenarios/RF25.md)

### RF26 · Modelos de Contrato

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Adicionar Modelo Contrato (/adicionar-modelo-contrato); estilos de parágrafo/cabeçalho; negrito, itálico, sublinhado, tachado, alinhamento, listas, link, desfazer/refazer; Atualizar preview; inserir variável; Como usar?; Ver todas as variáveis; Salvar modelo; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Testar editor, substituição de variáveis e contrato gerado com dados fictícios. Ações de edição/exclusão em lista vazia não foram observadas. Nenhum contrato foi assinado.

[Cenários RF26](cenarios/RF26.md)

### RF27 · Tipos de Pagamento

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo; Visualizar; Deletar; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Efeito de status, seleção de bandeira e gateway nos formulários financeiros; exclusão com vínculos.

[Cenários RF27](cenarios/RF27.md)

### RF28 · Bandeiras

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Bandeira; Adicionar Parcela; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Criar bandeira de teste, mapear edição/exclusão após criação e validar taxas e parcelamento com massa conhecida.

[Cenários RF28](cenarios/RF28.md)

### RF29 · Colaboradores

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Colaborador (/adicionar-colaborador); Funções; Visualizar (/visualizar-colaborador/{id}); Deletar; Salvar; Cancelar. Perfil do colaborador: Editar; abas Resumo, Funções, Alunos e Recebimentos; selecionar e Adicionar função; Remover função.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Vincular função e conferir acesso com contas de teste dedicadas; testar Sem login e restrições sem conceder acesso real. Validar persistência das associações e o preenchimento das abas com massa conhecida.

[Cenários RF29](cenarios/RF29.md)

### RF30 · Funções e permissões

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Função; Permissões; Visualizar; Salvar Função; Salvar permissões; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Testar autorização no servidor e na interface com perfis isolados, incluindo acesso direto às rotas. Exclusão de função não foi observada.

[Cenários RF30](cenarios/RF30.md)

### RF31 · Fornecedores

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Fornecedor; Visualizar; Deletar; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Testar documentos por tipo de pessoa, estado/cidade, duplicidade e exclusão com contas vinculadas.

[Cenários RF31](cenarios/RF31.md)

### RF32 · Tipos de Documentos

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Tipo; Visualizar; Deletar; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Verificar disponibilidade por aplicação nas contas e exclusão com referências.

[Cenários RF32](cenarios/RF32.md)

### RF33 · Atividades

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Atividade; Visualizar; Deletar; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Validade de pontuação negativa/zero, vínculo com campanhas e efeitos de alteração/exclusão.

[Cenários RF33](cenarios/RF33.md)

### RF34 · Pontuação

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Pontuação; selecionar produto; Adicionar; Salvar; Cancelar; ações nas linhas sem nome acessível.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Campanhas, produtos de resgate, pontos necessários, datas, crédito/resgate e ações de linha devem ser verificadas com massa isolada. Auditar nomes acessíveis dos botões.

[Cenários RF34](cenarios/RF34.md)

### RF35 · Produtos

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo; Salvar; Cancelar; escolher imagens; ações de linha sem nome acessível.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Validar persistência de produto por pontuação, edição, exclusão, mídia e vínculos com campanhas. Não inferir controle de estoque: campo de estoque não foi observado.

[Cenários RF35](cenarios/RF35.md)

### RF36 · Enquetes

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Enquete; Visualizar; Deletar; Adicionar resposta; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Pergunta/respostas obrigatórias, múltiplas alternativas, votação no app, contagem e alterações após votos.

[Cenários RF36](cenarios/RF36.md)

### RF37 · Fichas de Anamnese

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Anamnese; buscar aluno; Próxima; Fechar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Selecionar modelo e iniciar em massa fictícia, responder perguntas condicionais, salvar pendente/concluída, reabrir e conferir histórico. Não presumir que apenas abrir o assistente cria ficha.

[Cenários RF37](cenarios/RF37.md)

### RF38 · Modelos de Anamnese

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Novo Modelo (/anamnese/modelos/novo); Editar; Preview; excluir; Adicionar ao modelo; Remover; Limpar tudo; reordenar por arraste; Mostrar preview; Salvar Modelo; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Persistir ordem e obrigatoriedade; preview versus aplicação real; edição/exclusão de modelo já aplicado.

[Cenários RF38](cenarios/RF38.md)

### RF39 · Categorias de Anamnese

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Categoria; Editar; Excluir; Criar Categoria; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Validar ícones/cor, vínculo com perguntas e exclusão referenciada.

[Cenários RF39](cenarios/RF39.md)

### RF40 · Perguntas de Anamnese

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Pergunta; Visualizar; Deletar; Salvar; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Verificar como pergunta se vincula à categoria, comportamento condicional e impacto em modelos e respostas anteriores.

[Cenários RF40](cenarios/RF40.md)

### RF41 · Inteligência e Automação

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Executar agora; Configurar; Ver resultados do risco; liga/desliga; Salvar configuração; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Executar em ambiente isolado, conferir logs e destinatários, origem dos critérios e dados enviados. Nenhuma automação foi executada, ativada ou desativada. Confirmar se a configuração de Aniversariantes deveria usar critérios e preview próprios de aniversário.

[Cenários RF41](cenarios/RF41.md)

### RF42 · Resultados IA

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Alternar período; consultar resultados.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Conferir janela temporal, cálculo e consistência entre central, resultados e home; executar automação isolada para observar resultados adicionais.

[Cenários RF42](cenarios/RF42.md)

### RF43 · Configurações

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Cancelar; Salvar Configurações; em Aniversário alternar Mensagens/Endpoints & Tokens; inserir variáveis. WhatsApp: Salvar Configuração, Conectar por QR, Testar, Enviar Teste, Desconectar e Atualizar Status.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Validar limites e efeitos em ambiente isolado; obter autorização e infraestrutura para catraca, WhatsApp e gateway. Valores de senhas, IPs, tokens e chaves não integram esta documentação.

[Cenários RF43](cenarios/RF43.md)

### RF44 · Modelos de Ficha

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Nova Ficha; Criar Modelo; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Criar modelo de teste para acessar o editor posterior e conferir aplicação em ficha. Ações de edição/exclusão não foram observadas em lista vazia.

[Cenários RF44](cenarios/RF44.md)

### RF45 · Aplicativo

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Criar Notificação; Visualizar/Deletar aviso existente; Ver todas as notificações; Só pendentes; Ver todas as postagens; Ver todas denúncias; Enviar aviso; Cancelar.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Limites 179/180/181, edição de texto, entrega no app e moderação devem ser testados com grupo de teste isolado. Ações internas de posts/denúncias dependem de massa.

[Cenários RF45](cenarios/RF45.md)

### RF46 · Meu perfil e controles globais

**Capacidade esperada:** disponibilizar a consulta e as ações documentadas para este módulo, respeitando os dados e permissões do usuário.

**Escopo observável:** Meu perfil; Segurança; Preferências; Sair do sistema; abrir notificações; Marcar como lidas; tema; Edit profile; Show more; botão Abrir Academy Assistant em telas internas.

**Critérios de aceitação propostos:** apresentar dados e mensagens coerentes; validar entradas aplicáveis; permitir cancelamento sem gravação; quando houver gravação, persistir valores e vínculos corretos e manter o resultado após recarregar. Integrações devem apresentar sucesso/falha explícitos.

**Validação específica pendente:** Corrigir perfil, confirmar destino de Segurança e Preferências, testar acessibilidade, tema e notificações com conta de teste. Não foram alteradas senhas, preferências ou permissões.

[Cenários RF46](cenarios/RF46.md)

## Requisitos não funcionais propostos

| ID | Requisito | Como verificar |
| --- | --- | --- |
| RNF01 | Autenticação e autorização | Logout, sessão expirada, acesso direto e matriz por função com contas dedicadas. |
| RNF02 | Integridade | Persistência por ID, relacionamentos, exclusão lógica/física e ausência de duplicidade. |
| RNF03 | Usabilidade e consistência | Títulos corretos, estados vazio/carregando/erro distintos e retorno claro dos botões. |
| RNF04 | Acessibilidade | Nomes acessíveis de botões, teclado, foco, contraste e leitura em temas. |
| RNF05 | Responsividade | Inspecionar desktop e, em fase futura, resoluções menores; não homologado nesta sessão. |
| RNF06 | Rastreabilidade | Correlacionar caso, execução, registro no banco, evidência e bug. |
| RNF07 | Proteção de dados | Não incluir credenciais, tokens ou dados identificáveis desnecessários nas evidências compartilhadas. |
| RNF08 | Tempo de resposta | Medir com critério acordado; não há meta de desempenho definida nem ensaio de carga nesta etapa. |

## Regras que dependem de confirmação

Cadastro obrigatório e unicidade de CPF/login; escopo por academia/unidade; duração da diária; renovação; cancelamento versus exclusão; geração automática de contas; fórmulas financeiras e corporais; multa/juros; critérios de ausência e risco; preservação de históricos; status de produtos/perguntas/categorias; agenda/fuso de automações; propagação de permissões. A interface sugere essas regras, mas não comprova sua implementação no servidor.
