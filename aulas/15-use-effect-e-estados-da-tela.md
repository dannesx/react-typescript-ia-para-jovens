# Aula 15 — Primeira versão consumindo a API

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** aplicação final com API e IA
- **Conceito principal:** buscar dados e representar os estados da requisição
- **Produto do encontro:** primeira lista recebida da API
- **Pré-requisito:** ficha e tipo aprovados na aula 14
- **OpenCode:** planeja e pode editar depois da aprovação do grupo
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Fazer uma requisição com `fetch`, `async` e `await`.
- Iniciar a busca em um `useEffect` simples.
- Tipar a lista recebida.
- Exibir carregamento, erro, vazio e sucesso.
- Revisar todos os arquivos modificados pela IA.

## Preparação do professor

- Confirmar novamente o funcionamento das APIs.
- Manter o JSON local pronto.
- Criar uma cópia recuperável por grupo.
- Configurar aprovação manual no OpenCode.
- Definir quais arquivos podem ser alterados.

## Modelo mental

```text
tela aparece -> inicia busca -> carregando
                           ├── resposta -> sucesso ou lista vazia
                           └── falha    -> erro
```

## Roteiro de 80 minutos

1. **10 min — Revisão:** conferir tipo, endpoint e campos escolhidos.
2. **15 min — Demonstração:** buscar uma amostra pequena e ler a resposta.
3. **10 min — Plano com IA:** solicitar etapas e arquivos envolvidos.
4. **35 min — Implementação:** aprovar, acompanhar e testar a mudança.
5. **10 min — Fechamento:** cada grupo demonstra um estado da tela.

## Prompt-base

```text
Este projeto React com TypeScript deve buscar dados da API informada quando a tela abrir.
Use apenas o type e os campos já aprovados.
A interface precisa mostrar carregamento, erro, lista vazia e sucesso.
Antes de editar, apresente um plano curto, liste os arquivos e espere aprovação.
Não instale bibliotecas, não crie novas páginas e não implemente busca ou filtros nesta aula.
Depois de cada alteração, explique qual estado devo testar.
```

## Critérios para aprovar o plano

- Usa somente a API aprovada?
- Respeita o tipo criado pelo grupo?
- Inclui os quatro estados da tela?
- Não adiciona a interação reservada para a aula 16?
- Altera somente os arquivos necessários?

## Prática essencial

- Criar estado tipado para os dados.
- Criar estados de carregamento e erro.
- Executar a requisição em um `useEffect` que roda uma vez.
- Converter a resposta JSON.
- Renderizar itens com `map`.
- Mostrar mensagens para os quatro estados.
- Repetir um teste após cada correção.

## Uso de DaisyUI

Represente carregamento com `loading loading-spinner`, erro com `alert alert-error`, vazio com `alert alert-info` e sucesso com uma coleção de `card`. Um `skeleton` pode substituir o spinner apenas como extensão; não implemente os dois durante a prática principal.

Inclua no prompt: “Preserve os componentes DaisyUI escolhidos no planejamento e não acrescente bibliotecas visuais”.

**Verificação:** cada estado deve possuir texto compreensível além de cor ou animação.

## Testes manuais

| Estado | Como verificar |
| --- | --- |
| Carregamento | Observar a mensagem antes da resposta |
| Sucesso | Confirmar itens e campos esperados |
| Vazio | Usar a amostra local vazia |
| Erro | Usar endpoint de teste inválido e depois restaurar |

## Extensão

Criar um botão “Tentar novamente” no estado de erro, reutilizando a função de busca.

## Erros esperados

- Aprovar edição antes de ler o plano.
- Usar propriedades ausentes na resposta.
- Deixar carregamento ativo depois do término.
- Criar repetição de requisições no `useEffect`.

## Plano B

Se a rede falhar, carregar o JSON local mantendo os mesmos tipos e estados visuais. O grupo deve registrar que utilizou a contingência.

## Evidência de aprendizagem

Cada grupo registra arquivos alterados, estados testados e uma mudança da IA que precisou ser compreendida antes da aprovação.
