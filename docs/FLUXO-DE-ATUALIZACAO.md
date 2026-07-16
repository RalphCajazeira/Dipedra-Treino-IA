# Fluxo de atualização das instruções e fontes

## 1. Durante o uso

O consultor utiliza o Projeto normalmente. Correções, decisões, novos procedimentos e dúvidas resolvidas podem se tornar aprendizados, mas não são publicados automaticamente.

## 2. Encerramento da conversa

O consultor envia o conteúdo de `templates/PROMPT-FINAL-DE-ATUALIZACAO.md`.

O agente deve revisar:

- instruções atuais do Projeto;
- fontes anexadas ao Projeto;
- arquivos já versionados no GitHub;
- decisões confirmadas na conversa.

## 3. Classificação

Cada informação deve ser classificada como:

- regra ou orientação permanente para `INSTRUCOES.md`;
- conhecimento de referência para um arquivo em `fontes/`;
- correção de conteúdo existente;
- conteúdo obsoleto que deve ser removido;
- pendência sem confirmação, que não deve ser publicada como oficial.

## 4. GitHub

A atualização deve ocorrer em branch separada e resultar em Pull Request. A branch padrão não deve ser alterada diretamente.

O PR precisa permitir que o responsável compreenda:

- por que a mudança é necessária;
- qual conversa ou aprendizado motivou a mudança, sem copiar dados sensíveis;
- quais arquivos mudaram;
- o que precisa ser sincronizado no Projeto depois do merge.

## 5. Aprovação

O responsável revisa o PR e pode aprovar, pedir alterações ou fechar sem integrar.

Até o merge, as mudanças são apenas propostas e não devem ser tratadas como fonte oficial.

## 6. Sincronização do Projeto

Depois do merge:

1. copie `INSTRUCOES.md` para as instruções do Projeto;
2. remova do Projeto as fontes excluídas no repositório;
3. substitua arquivos alterados;
4. carregue os novos arquivos da pasta `fontes/`;
5. confirme que o Projeto corresponde à versão integrada na branch padrão.

A atualização do GitHub e a atualização do Projeto do ChatGPT são etapas diferentes e devem ser confirmadas separadamente.
