# Aula 9 — Objetos, arrays e o tipo `Tarefa`

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** objeto tipado dentro de uma lista
- **Produto do encontro:** lista inicial renderizada com `map`
- **Pré-requisito:** props tipadas e uso anterior de `map`
- **OpenCode:** ainda não será usado
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Entender uma tarefa como um objeto.
- Criar o tipo `Tarefa`.
- Ler `Tarefa[]` como lista de tarefas.
- Renderizar objetos usando `map` e `id` como `key`.

## Preparação do professor

- Preparar três tarefas com identificadores únicos.
- Manter somente `id`, `titulo` e `concluida`.
- Criar um objeto incompleto e outro com uma propriedade incorreta.

## Exemplo-base

```ts
export type Tarefa = {
  id: number;
  titulo: string;
  concluida: boolean;
};

const tarefasIniciais: Tarefa[] = [
  { id: 1, titulo: "Estudar React", concluida: true },
  { id: 2, titulo: "Fazer o exercício", concluida: false },
  { id: 3, titulo: "Organizar a mochila", concluida: false },
];
```

## Roteiro de 80 minutos

1. **10 min — Revisão:** listar as informações necessárias para descrever uma tarefa.
2. **15 min — Objeto:** agrupar as informações em `Tarefa`.
3. **15 min — Array tipado:** montar e ler `Tarefa[]`.
4. **30 min — Prática:** substituir chamadas repetidas por `map`.
5. **10 min — Fechamento:** usar autocomplete e corrigir objetos inválidos.

## Prática essencial

- Criar o tipo `Tarefa`.
- Montar uma lista com três objetos válidos.
- Renderizar `ItemTarefa` usando `map`.
- Usar `tarefa.id` como `key`.
- Corrigir dois objetos inválidos fornecidos pelo professor.

## Uso de DaisyUI

Renderize a coleção em `ul` e mantenha cada item como `card card-compact border border-base-300`. Use `checkbox checkbox-primary` com `checked={tarefa.concluida}` e `readOnly`, pois a interação será implementada depois.

**Verificação:** a `key` pertence ao elemento criado pelo `map`; DaisyUI não substitui `id`, tipagem ou estrutura da lista.

## Extensão

Adicionar `categoria: string` ao tipo, aos dados e à interface.

## Verificação rápida

- Todos os objetos seguem o mesmo formato?
- A lista está escrita como `Tarefa[]`?
- O `map` passa as props corretas para `ItemTarefa`?

## Erros esperados

- Esquecer os colchetes ao tipar a lista.
- Adicionar uma propriedade ao tipo sem atualizar os objetos.
- Usar o índice do `map` mesmo possuindo `id`.

## Plano de recuperação

Entregar o tipo pronto e pedir que o aluno selecione quais objetos respeitam o contrato. Depois renderizar somente duas tarefas.

## Evidência de aprendizagem

O aluno cria uma nova tarefa usando as sugestões automáticas da IDE e explica o papel do `id`.
