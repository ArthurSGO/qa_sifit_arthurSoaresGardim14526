# Registro de evidências e execuções

[← Evidências](README.md) · [Roteiro de gravação](../6-roteiro-banco-e-jam.md)

Preencher uma linha por execução real. Os campos pendentes são texto, não links fictícios. Não sobrescrever uma falha após reteste. Links do JAM e do Drive podem ser preenchidos depois; seguir o [fluxo de gravação e atualização](fluxo-de-gravacao.md). Cada nova gravação deve apontar para a execução realizada naquela data, preservando o histórico abaixo.

| Execução | Caso | Data | Resultado | ID da massa | Banco verificado | JAM | Drive | Vídeo/trecho | Bug/ocorrência |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EXE-001 | CT-RF01-01 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-002 | CT-RF01-02 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-003 | CT-RF01-03 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-004 | CT-RF01-04 | 21/10/2026 | Reprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | BUG-001 |
| EXE-005 | CT-RF01-05 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-006 | CT-RF01-06 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-007 | CT-RF02-01 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-008 | CT-RF02-02 | 21/10/2026 | Inconclusivo | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | INV-001 |
| EXE-009 | CT-RF03-01 | 21/10/2026 | Reprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | BUG-002 |
| EXE-010 | CT-RF07-08 | 21/10/2026 | Reprovado | 414 | Não | Pendente | Pendente | Não registrado | BUG-004 |
| EXE-011 | CT-RF08-08 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-012 | CT-RF09-08 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-013 | CT-RF09-09 | 21/10/2026 | Reprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | BUG-003 |
| EXE-014 | CT-RF43-01 | 21/10/2026 | Aprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | — |
| EXE-015 | CT-RF46-01 | 21/10/2026 | Reprovado | Não aplicável ou não registrado | Não | Pendente | Pendente | Não registrado | BUG-005 |

## Modelo para a próxima execução

| Campo | Preencher |
| --- | --- |
| Execução | EXE-<sequência> |
| Caso | CT-RFxx-yy |
| Data/hora e fuso | Data real; America/Sao_Paulo |
| Ambiente/versão | Confirmar |
| Massa/ID | Identificador QA e chave gerada |
| Antes | Estado inicial no site e banco |
| Depois | Valores/status após recarregar e reconsultar |
| Consulta/arquivo | Consulta real aprovada ou referência ao registro |
| Resultado | Aprovado/Reprovado/Inconclusivo/Bloqueado |
| JAM | Colar link real após revisar vídeo |
| Drive | Colar link da cópia preservada e conferir acesso |
| Vídeo/trecho | VID-<sequência> e início–fim do trecho correspondente ao caso |
| Bug/reteste | ID e execução anterior, quando houver |
