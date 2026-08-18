# Aula 12 — Concluir e excluir tarefas

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** atualizar um item específico pelo `id`
- **Produto do encontro:** ações de concluir, reabrir e excluir
- **Pré-requisito:** lista de tarefas no estado
- **OpenCode:** explica transformações e sugere testes; alunos implementam
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Localizar uma tarefa pelo `id`.
- Alternar o valor de `concluida` sem alterar as demais.
- Remover uma tarefa específica.
- Passar funções tipadas por props.
- Exibir uma mensagem quando a lista estiver vazia.

## Preparação do professor

- Confirmar que todos os itens possuem `id` único.
- Preparar cartões para representar uma lista antes e depois de `map` e `filter`.
- Manter uma versão com várias tarefas para os testes.

## Modelo mental

- `map`: percorre a lista e pode devolver uma versão atualizada de cada item.
- `filter`: percorre a lista e mantém somente os itens que passam pela condição.

## Tipos das ações

```ts
type AcoesTarefa = {
  aoAlternar: (id: number) => void;
  aoExcluir: (id: number) => void;
};
```

## Roteiro de 80 minutos

1. **10 min — Revisão:** apontar qual propriedade identifica cada tarefa.
2. **10 min — OpenCode:** pedir explicação de `map` e `filter` sem edição.
3. **20 min — Demonstração:** alternar `concluida` pelo `id`.
4. **25 min — Prática:** implementar exclusão e passar ações por props.
5. **15 min — Testes:** concluir, reabrir, excluir e esvaziar a lista.

## Prompt da aula

```text
Explique para um iniciante a diferença entre usar map para atualizar uma tarefa
e filter para excluir uma tarefa em React.
Use um exemplo com id, titulo e concluida, mas não altere arquivos.
Depois sugira quatro testes manuais para essas duas ações.
```

## Prática essencial

- Criar `alternarTarefa(id)` no componente que possui o estado.
- Atualizar somente a tarefa com o `id` recebido.
- Criar `excluirTarefa(id)` usando `filter`.
- Passar as duas funções por props tipadas.
- Exibir “Nenhuma tarefa cadastrada” quando a lista estiver vazia.

## Uso de DaisyUI

Use `checkbox checkbox-success` para alternar conclusão, `btn btn-error btn-sm` para excluir, `line-through` para o texto concluído e `alert alert-info` para lista vazia. Todo controle precisa de texto visível ou `aria-label` específico.

**Verificação:** marcar e excluir devem funcionar por teclado. A cor não pode ser a única indicação; mantenha texto, checkbox ou decoração de texto.

## Testes manuais

1. Concluir uma tarefa pendente.
2. Reabrir a mesma tarefa.
3. Excluir uma tarefa e preservar as outras.
4. Excluir todas e visualizar a mensagem de lista vazia.

## Extensão

Adicionar uma confirmação visual simples antes da exclusão, sem usar janela do navegador.

## Erros esperados

- Alterar diretamente `tarefa.concluida`.
- Usar a posição da tarefa em vez do `id`.
- Executar a função durante a renderização do botão.
- Colocar o estado dentro de cada `ItemTarefa`.

## Plano de recuperação

Implementar somente `alternarTarefa` coletivamente. Depois fornecer `excluirTarefa` com a condição do `filter` para os alunos completarem.

## Evidência de aprendizagem

O aluno usa cartões ou desenho para mostrar qual item muda com `map` e qual desaparece com `filter`.
