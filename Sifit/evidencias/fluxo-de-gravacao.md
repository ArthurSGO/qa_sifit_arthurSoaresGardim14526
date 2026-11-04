# Gravações e atualização da documentação

[← Evidências](README.md) · [Registro de execuções](registro-de-evidencias.md) · [Roteiro](../6-roteiro-banco-e-jam.md)

A documentação é uma entrega em andamento. A ausência de vídeo não impede o versionamento dos requisitos, cenários e resultados já observados. Deixar `Pendente` onde ainda não houver link real; não marcar um caso como executado por ter apenas roteiro escrito.

## Antes de gravar

1. Escolher os casos pelo roteiro e conferir as pré-condições.
2. Reservar um identificador de vídeo, como `VID-001`, e anotar os casos que ele demonstrará.
3. Preparar a massa fictícia e, quando necessário, as consultas de leitura pelo ID.
4. Fazer uma gravação curta de ensaio para confirmar que site e Workbench aparecem e que o vídeo pode ser preservado no Drive.

Considerando o limite de 30 vídeos do JAM informado para esta conta, agrupar casos relacionados em uma gravação quando a sequência continuar clara. Registrar os trechos de cada caso, por exemplo `00:40–01:15`. Não é necessário criar um vídeo por caso.

## Depois de cada gravação

1. Revisar o vídeo e registrar uma nova execução para cada caso efetivamente realizado, com data, resultado e ID da massa.
2. Acrescentar o identificador do vídeo, trecho e link real do JAM ao registro. Uma nova gravação não deve ser atribuída à execução histórica de 21/10/2026.
3. Preservar uma cópia do vídeo no Google Drive, quando disponível, conferir sua reprodução e o acesso para quem avaliará o trabalho; então preencher a coluna Drive. Manter o link JAM como referência enquanto funcionar.
4. Atualizar o relatório de execução, a matriz e os bugs correspondentes quando houver novos resultados. Retestes recebem nova execução e preservam a falha anterior.
5. Versionar o lote concluído, sem esperar terminar todas as gravações:

```powershell
git status --short
git diff
git add -- Sifit
git commit -m "docs: registra evidencias do lote de autenticacao"
```

Adaptar a mensagem ao conteúdo real do lote. Após configurar o repositório remoto e sua branch de acompanhamento, usar `git push` para publicar os commits.

## Onde guardar cada coisa

| Conteúdo | Local |
| --- | --- |
| Requisitos, cenários, resultados e links | Markdown neste repositório |
| Capturas estáticas existentes | `imagens/` |
| Vídeos | JAM e cópia no Google Drive |
| Senhas, configurações locais e exportações do banco | Fora do repositório |

O registro de execuções é a referência principal para os links. Nos demais documentos, apontar para a execução correspondente em vez de duplicar URLs. Arquivos de vídeo e exportações SQL estão ignorados pelo Git para manter o repositório focado na documentação.
