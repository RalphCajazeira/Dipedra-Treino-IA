# Prompt final para atualização do Projeto

Copie e envie este prompt ao final de uma conversa relevante no Projeto do ChatGPT.

```text
Revise esta conversa e consolide apenas os aprendizados confirmados, reutilizáveis e relevantes para o treinamento futuro deste Projeto.

Antes de alterar qualquer coisa:
1. Leia integralmente as instruções atuais deste Projeto do ChatGPT.
2. Leia todas as fontes atuais relevantes anexadas ao Projeto.
3. Acesse o repositório público RalphCajazeira/Dipedra-Treino-IA.
4. Leia primeiro AGENTS.md, README.md e a pasta correspondente a este Projeto.
5. Compare o que foi aprendido nesta conversa com o que já existe, preservando tudo que continua correto.

Depois:
- identifique quais instruções precisam ser alteradas;
- identifique quais fontes precisam ser criadas, editadas, substituídas ou apagadas;
- não publique dados pessoais, credenciais, documentos confidenciais ou informações sensíveis;
- não invente regras nem trate inferências como decisões oficiais;
- atualize o CHANGELOG.md do Projeto;
- crie uma branch nova a partir da branch padrão atualizada;
- faça as alterações de forma estruturada;
- abra um Pull Request para a branch padrão;
- não faça merge, não aprove o próprio PR e não habilite auto-merge.

Na resposta final, informe:
1. número e link do Pull Request;
2. branch criada;
3. arquivos criados, alterados e removidos;
4. resumo objetivo dos aprendizados consolidados;
5. informações que não foram publicadas por segurança ou falta de confirmação;
6. exatamente quais instruções e fontes deverão ser substituídas, removidas ou carregadas novamente no Projeto do ChatGPT depois que o PR for aprovado e integrado.

Não diga que atualizou as instruções ou fontes do Projeto do ChatGPT se você atualizou apenas o GitHub. Diferencie claramente atualização do repositório e sincronização do Projeto.
```

## Campo que pode ser acrescentado

Quando houver mais de um Projeto no repositório, acrescente ao início do prompt:

```text
A pasta deste Projeto no repositório é: projetos/<slug-do-projeto>.
```
