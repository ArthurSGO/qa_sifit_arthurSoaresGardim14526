# Referência acadêmica e metodologia

[← Índice](README.md)

## Fonte utilizada

[Repositório do professor — extensao-qa](https://github.com/Adnyslougansilva/extensao-qa), branch main, revisão consultada `c490e848643956924253b73d91b5497bf16fd889`, em 21/10/2026. O ponto final do link enviado foi tratado como pontuação da mensagem; foi consultado o repositório extensao-qa.

Foram lidos o README, análise de requisitos, plano de testes, relatório de bugs, relatório de execução e exemplos de cenários de login e gestão de funcionários. A árvore do repositório contém os demais exemplos de cenários do OrangeHRM. Não foi copiado conteúdo de negócio do OrangeHRM para o Sifit.

| Exemplo do professor | Adaptação no Sifit |
| --- | --- |
| 1-Analise de requisitos.md | 1-analise-de-requisitos.md |
| 2-plano de testes.md | 2-plano-de-testes.md |
| 3-Relatorio-de-Bugs.md | 3-relatorio-de-bugs.md |
| 4- Relatorio dos testes.md | 4-relatorio-de-execucao.md, explicitamente parcial |
| Cenarios de testes | cenarios/RF01.md a RF46.md, com DADO/QUANDO/ENTÃO |
| Links de vídeo no relatório de bugs | Registro JAM pendente, sem URLs inventadas |

## Tratamento de bugs e funcionalidades ausentes

A seção Gestão de Defeitos do plano orienta documentar título, descrição, reprodução, evidência e gravidade. O relatório de exemplo distingue esperado e obtido, prioridade, status, ambiente e caso relacionado, e apresenta links JAM. Por isso, foi criado um relatório de bugs próprio, separado de suspeitas e indisponibilidades declaradas.

Não se reproduziram inconsistências de totais, IDs ou aprovação presentes em exemplos: as contagens desta documentação são derivadas dos seus próprios casos e registros. Não se exige toast de sucesso apenas por preferência: a aceitação deve considerar o resultado útil do fluxo.

## Evidência e inferência

**Observado:** elemento, campo, destino, mensagem ou resultado visível durante a navegação. **Proposto:** comportamento esperado pelo analista para validar com o responsável. **Pendente:** caminho não executado, pré-condição ausente ou efeito não conciliado. **Confirmado na interface:** defeito diretamente reproduzido, sem conclusão automática sobre sua causa no servidor ou banco.

O levantamento é de caixa-preta. Não foram fornecidos código-fonte do Sifit, esquema do banco, especificação oficial, versão da implantação ou contas de outros perfis. A documentação deve ser atualizada à medida que esses elementos forem disponibilizados.
