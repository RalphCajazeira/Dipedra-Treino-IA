# AGENTS.md — Operação do repositório Dipedra-Treino-IA

## 1. Finalidade

Este repositório é a fonte versionada das instruções e dos arquivos de conhecimento usados nos Projetos do ChatGPT da Dipedra.

Ao receber uma solicitação para consolidar aprendizados de uma conversa, atualizar instruções, criar, editar ou remover fontes, o agente deve seguir integralmente este documento.

## 2. Regra principal

Antes de propor qualquer alteração:

1. Leia as instruções atuais do Projeto do ChatGPT.
2. Leia todas as fontes atuais relevantes do Projeto.
3. Revise a conversa atual e identifique apenas aprendizados confirmados e reutilizáveis.
4. Compare o conteúdo novo com o que já existe no repositório.
5. Preserve informações válidas; não substitua conteúdo correto por resumos mais pobres.

A conversa não é automaticamente a fonte oficial. Uma informação só deve ser consolidada quando estiver clara, confirmada pelo usuário ou sustentada pelos arquivos existentes.

## 3. Segurança e privacidade

Este repositório é público.

Nunca publique:

- senhas, tokens, chaves, cookies ou segredos;
- dados pessoais desnecessários de clientes, funcionários ou terceiros;
- CPF, RG, endereço residencial, telefone pessoal ou dados bancários;
- documentos comerciais confidenciais;
- informações que o usuário tenha indicado como privadas;
- conteúdo integral de conversas quando apenas o aprendizado consolidado for necessário.

Quando uma informação útil contiver dado sensível, generalize, anonimize ou omita o trecho sensível. Em caso de dúvida, não publique e registre a pendência na descrição do Pull Request.

## 4. Estrutura esperada

Cada Projeto do ChatGPT deve possuir sua própria pasta:

```text
projetos/<slug-do-projeto>/
├── README.md
├── INSTRUCOES.md
├── CHANGELOG.md
└── fontes/
    ├── README.md
    └── <arquivos-de-fonte>
```

Regras:

- `INSTRUCOES.md`: versão completa e pronta para copiar para o campo de instruções do Projeto.
- `fontes/`: arquivos prontos para serem adicionados como fontes ao Projeto.
- `README.md`: finalidade, público, escopo e relação dos arquivos do Projeto.
- `CHANGELOG.md`: registro resumido das mudanças relevantes, com data.
- Não crie arquivos duplicados com o mesmo propósito.
- Prefira Markdown e formatos textuais simples. Use DOCX ou PDF apenas quando a apresentação ou imagens forem indispensáveis.

## 5. Fluxo obrigatório de atualização

1. Confirme o repositório e a branch padrão.
2. Leia `AGENTS.md`, o `README.md` raiz e os arquivos da pasta do Projeto.
3. Verifique a permissão disponível no repositório.
4. Crie uma branch nova a partir da branch padrão atualizada, no próprio repositório quando houver permissão de escrita ou em um fork quando não houver.
5. Use um nome claro, por exemplo:
   - `docs/<projeto>-atualizacao-aaaa-mm-dd`
   - `docs/<projeto>-consolidar-aprendizados`
6. Faça apenas alterações relacionadas ao objetivo informado.
7. Atualize o `CHANGELOG.md` do Projeto.
8. Revise diferenças, links, nomes e ausência de dados sensíveis.
9. Crie um Pull Request para a branch padrão do repositório original.
10. Não faça merge e não habilite auto-merge.
11. Informe ao usuário:
    - número e link do PR;
    - origem da branch, indicando se está no repositório original ou em fork;
    - arquivos criados, alterados e removidos;
    - resumo do que mudou;
    - pendências ou informações não publicadas por segurança;
    - instruções e fontes que deverão ser sincronizadas no Projeto do ChatGPT após a aprovação.

## 6. Permissões, fork e limitações da ferramenta

Um repositório público permite leitura, mas não concede automaticamente permissão para criar branches ou commits nele.

- Se a conta conectada tiver permissão de escrita, crie a branch no próprio repositório e abra o PR normalmente.
- Se não tiver permissão de escrita, use um fork e abra um PR do fork para `RalphCajazeira/Dipedra-Treino-IA`.
- Se a ferramenta conectada não conseguir criar fork ou Pull Request entre repositórios, não alegue sucesso. Prepare os arquivos ou patch completo, explique a limitação e informe exatamente o que o usuário precisa executar para concluir o PR.
- Nunca solicite ou publique credenciais para contornar falta de permissão.

## 7. Commits e Pull Requests

Commits devem ser pequenos e descritivos. Exemplos:

- `docs(comercial): update project instructions`
- `docs(producao): add order conference procedure`
- `docs(fontes): remove obsolete training source`

Título recomendado do PR:

```text
docs(<projeto>): atualizar instruções e fontes
```

A descrição do PR deve seguir `.github/pull_request_template.md`.

## 8. Critérios para editar, criar ou apagar

### Editar

Edite um arquivo quando o assunto e a finalidade continuarem os mesmos. Preserve histórico útil e elimine contradições.

### Criar

Crie um arquivo quando o conteúdo tiver finalidade própria, for extenso o suficiente para justificar separação ou precisar ser carregado individualmente como fonte.

### Apagar

Apague somente quando o conteúdo estiver obsoleto, duplicado, incorreto ou expressamente substituído. Explique a remoção no `CHANGELOG.md` e no PR.

## 9. Qualidade do conteúdo

O conteúdo consolidado deve:

- ser claro para um novo consultor;
- separar regra oficial, procedimento, exemplo e sugestão;
- usar linguagem objetiva e consistente;
- indicar incertezas e pendências;
- não inventar processos ausentes;
- evitar registrar detalhes passageiros sem valor de treinamento;
- manter nomes de telas, campos e etapas exatamente como confirmados.

## 10. Sincronização com o Projeto do ChatGPT

Após o merge do PR, o agente deve orientar a sincronização do Projeto correspondente:

1. substituir as instruções do Projeto pelo conteúdo integral de `INSTRUCOES.md`;
2. remover fontes que tenham sido excluídas ou substituídas no repositório;
3. carregar novamente as fontes atuais da pasta `fontes/`;
4. confirmar que nomes e versões coincidem com o repositório;
5. não afirmar que a sincronização foi realizada sem confirmação da ferramenta ou da interface utilizada.

## 11. Proibições

O agente não deve:

- alterar diretamente a branch padrão, salvo inicialização técnica expressamente autorizada;
- aprovar ou fazer merge do próprio PR;
- misturar atualizações de Projetos diferentes sem necessidade;
- publicar dados sensíveis;
- apagar arquivos sem justificativa;
- apresentar como oficial algo apenas inferido;
- dizer que atualizou o Projeto do ChatGPT se apenas atualizou o GitHub;
- dizer que abriu um PR quando a ferramenta não confirmou a criação.
