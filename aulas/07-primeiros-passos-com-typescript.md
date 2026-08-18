# Aula 7 — Novo projeto e primeiros passos com TypeScript

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** tipos básicos como pistas da IDE
- **Produto do encontro:** estrutura visual inicial da lista de tarefas
- **Pré-requisito:** componentes, props, estado, eventos e `map`
- **OpenCode:** ainda não será usado

## Mudança de contexto

A partir desta aula, a turma inicia uma aplicação nova, com arquivos, visual e dados próprios. O encontro começa diretamente pelo problema de organizar tarefas.

## Objetivos

- Compreender a proposta do Todo List.
- Reconhecer arquivos `.tsx`.
- Identificar `string`, `number` e `boolean`.
- Usar uma mensagem da IDE para corrigir um erro simples.
- Criar componentes estáticos para a nova interface.

## Preparação do professor

- Criar um projeto vazio em React com TypeScript para cada aluno ou dupla.
- Confirmar que o projeto abre sem erros.
- Preparar uma imagem simples de referência para o Todo List.
- Deixar um CSS-base simples e próprio para o Todo List.
- Criar três erros independentes envolvendo os tipos básicos.

## Vocabulário

- **Todo List:** lista de coisas que precisam ser feitas.
- **Tipo:** formato de informação esperado pelo código.
- **`string`:** texto.
- **`number`:** número.
- **`boolean`:** verdadeiro ou falso.

## Roteiro de 80 minutos

1. **10 min — Encerramento e recomeço:** lembrar o que foi aprendido no projeto 1 e apresentar o novo desafio.
2. **10 min — Planejamento visual:** desenhar título, formulário, filtros e lista.
3. **15 min — TypeScript:** classificar exemplos do Todo List nos três tipos básicos.
4. **30 min — Prática guiada:** criar `CabecalhoLista` e a estrutura visual inicial.
5. **10 min — Caça aos erros:** corrigir três erros preparados.
6. **5 min — Fechamento:** explicar uma pista mostrada pela IDE.

## Demonstração

```ts
const nomeDaLista: string = "Tarefas da semana";
const quantidade: number = 3;
const possuiPendencias: boolean = true;
```

Troque um valor de propósito, leia a primeira frase do erro e traduza-a com a turma antes de corrigir.

## Prática essencial

- Alterar o título da aplicação.
- Criar a área do formulário sem comportamento.
- Criar a área reservada à lista.
- Declarar um exemplo de cada tipo básico.
- Corrigir ao menos um erro usando a indicação da IDE.

## Extensão

Criar um componente `ResumoTarefas` que, por enquanto, exiba uma quantidade fixa e um texto fixo.

## Verificação rápida

- O aluno sabe que o projeto atual não depende do anterior?
- Consegue identificar texto, número e verdadeiro/falso?
- Localiza arquivo e linha indicados pela IDE?

## Erros esperados

- Pensar que `"3"` é número porque possui algarismo.
- Tentar copiar componentes do projeto anterior.
- Alterar várias linhas antes de testar.

## Plano de recuperação

Classificar valores usando cartões antes de voltar ao código. Se necessário, entregar a estrutura visual pronta e concentrar a prática nos tipos e nas mensagens da IDE.

## Evidência de aprendizagem

Cada aluno registra: “A IDE esperava ___, recebeu ___ e a correção foi ___”.
