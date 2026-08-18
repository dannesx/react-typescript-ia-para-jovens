# Aula 13 — Filtros e conclusão do Todo List

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** derivar visualizações sem modificar a lista original
- **Produto do encontro:** Todo List finalizado e dividido em componentes
- **Pré-requisito:** adicionar, alternar e excluir tarefas
- **OpenCode:** explica o fluxo e revisa filtros, props e tipos
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Filtrar tarefas como todas, pendentes ou concluídas.
- Preservar a lista original no estado.
- Separar formulário, filtros e lista em componentes.
- Manter o estado no ancestral comum.
- Apresentar o segundo projeto funcionando.

## Preparação do professor

- Criar uma cópia recuperável antes da separação em componentes.
- Preparar cartões com `App`, `FormularioTarefa`, `FiltrosTarefa`, `ListaTarefas` e `ItemTarefa`.
- Definir o tipo simples do filtro: `"todas" | "pendentes" | "concluidas"`.

## Estrutura esperada

```text
App
├── FormularioTarefa -> envia uma nova tarefa
├── FiltrosTarefa    -> envia o filtro escolhido
└── ListaTarefas     <- recebe tarefas e ações
    └── ItemTarefa
```

## Roteiro de 80 minutos

1. **10 min — Revisão:** demonstrar adicionar, concluir e excluir.
2. **10 min — OpenCode:** pedir um desenho textual do fluxo dos componentes.
3. **20 min — Filtros:** criar estado do filtro e lista derivada.
4. **25 min — Componentes:** separar uma parte por vez, testando sempre.
5. **15 min — Apresentação curta:** demonstrar o projeto e revisar requisitos.

## Prompt inicial

```text
Desenhe com texto o fluxo entre App, FormularioTarefa, FiltrosTarefa,
ListaTarefas e ItemTarefa.
O estado original deve permanecer em App e os filtros não podem apagar tarefas.
Não altere arquivos. Explique quais dados descem e quais ações voltam ao componente pai.
```

## Prática essencial

- Criar os filtros “Todas”, “Pendentes” e “Concluídas”.
- Calcular uma lista filtrada sem alterar `tarefas`.
- Mostrar a quantidade de pendentes.
- Separar ao menos formulário, filtros e lista.
- Tipar todas as novas props.
- Confirmar que as ações anteriores continuam funcionando.

## Uso de DaisyUI

Apresente os filtros como `tabs tabs-box` com cada opção usando `tab`; a opção ativa recebe `tab-active`. Mostre a quantidade pendente com `stats` ou `badge`. Preserve botões reais e o estado ativo compreensível para leitores de tela.

**Verificação:** navegar pelos filtros com teclado, confirmar indicação visual e textual do filtro atual e testar o tema em largura estreita.

## Checklist de conclusão

- Adiciona tarefas válidas.
- Conclui e reabre uma tarefa.
- Exclui pelo `id`.
- Mostra mensagem de lista vazia.
- Filtra sem perder dados.
- Exibe contagem de pendentes.
- Não apresenta erros de TypeScript.

## Extensão

Adicionar uma ação “Limpar concluídas” depois que todo o checklist estiver funcionando.

## Erros esperados

- Salvar a lista filtrada por cima da lista original.
- Duplicar o estado em mais de um componente.
- Extrair todos os componentes de uma vez e dificultar a localização do erro.

## Plano de recuperação

Manter todos os elementos em `App` e concluir primeiro os filtros. Extrair somente `ListaTarefas` se houver tempo.

## Evidência de aprendizagem

Cada grupo demonstra o checklist e explica onde vivem o estado original, o filtro e a lista derivada.
