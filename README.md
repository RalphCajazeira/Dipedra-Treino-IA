# Dipedra — Treinamento de IA

Repositório público para versionamento das **instruções** e **fontes de conhecimento** utilizadas nos Projetos do ChatGPT da Dipedra.

## Objetivo

Permitir que os aprendizados obtidos durante o uso dos Projetos sejam revisados, consolidados e enviados de maneira estruturada ao GitHub, sempre por Pull Request e com aprovação humana antes de se tornarem oficiais.

## Como funciona

1. O consultor utiliza normalmente o Projeto no ChatGPT.
2. Ao final de uma conversa relevante, envia o prompt disponível em `templates/PROMPT-FINAL-DE-ATUALIZACAO.md`.
3. O ChatGPT lê as instruções e fontes atuais do Projeto.
4. O ChatGPT compara os aprendizados da conversa com o conteúdo já versionado.
5. O ChatGPT cria uma branch, atualiza os arquivos necessários e abre um Pull Request.
6. O responsável pelo repositório revisa e aprova ou solicita ajustes.
7. Após o merge, as instruções e fontes do Projeto do ChatGPT são sincronizadas com a versão aprovada.

## Estrutura

```text
.
├── AGENTS.md
├── README.md
├── .github/
│   └── pull_request_template.md
├── docs/
│   └── FLUXO-DE-ATUALIZACAO.md
├── projetos/
│   └── README.md
└── templates/
    ├── PROMPT-FINAL-DE-ATUALIZACAO.md
    └── MODELO-PROJETO.md
```

Cada Projeto deve ser criado em `projetos/<slug-do-projeto>/` conforme as regras de `AGENTS.md`.

## Documento obrigatório para agentes

Todo ChatGPT, Codex ou outro agente que trabalhar neste repositório deve ler primeiro o arquivo [`AGENTS.md`](AGENTS.md).

## Segurança

Este repositório é público. Dados pessoais, documentos confidenciais, credenciais, segredos, informações bancárias e conteúdo interno sensível não devem ser publicados.

## Regra de aprovação

As atualizações devem ser feitas em branch separada e enviadas por Pull Request. O agente que criou a alteração não deve aprovar nem fazer merge do próprio PR.
