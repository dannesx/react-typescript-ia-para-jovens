# Aula 11 — Formulário para adicionar tarefas

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** transformar o formulário em uma nova tarefa tipada
- **Produto do encontro:** inclusão de tarefas pendentes
- **Pré-requisito:** `useState<Tarefa[]>` e eventos de formulário
- **OpenCode:** planeja e revisa; alunos implementam
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Controlar o título digitado com `useState`.
- Validar uma entrada vazia.
- Criar um objeto compatível com `Tarefa`.
- Adicionar sem apagar as tarefas anteriores.
- Limpar o campo depois do envio.

## Preparação do professor

- Manter a geração de `id` simples e previamente escolhida.
- Preparar exemplos de entrada válida, vazia e formada somente por espaços.
- Testar o prompt de planejamento sem edição.
- Garantir que a versão inicial da aula 10 esteja recuperável.

## Fluxo da interação

```text
digitar -> enviar -> validar -> criar Tarefa -> atualizar lista -> limpar campo
```

## Roteiro de 80 minutos

1. **10 min — Revisão:** localizar o estado da lista e o formulário visual.
2. **10 min — OpenCode:** pedir um plano curto e três testes.
3. **20 min — Demonstração:** controlar o campo e validar o texto.
4. **30 min — Prática:** criar e adicionar a nova tarefa.
5. **10 min — Revisão:** solicitar à IA uma explicação da função, sem edição.

## Prompt inicial

```text
Tenho um Todo List em React com TypeScript e um estado Tarefa[].
Quero adicionar uma tarefa com id, titulo e concluida igual a false.
Crie um plano curto e três testes manuais.
Não altere arquivos e não escreva a implementação completa.
```

## Prática essencial

- Criar o estado do campo de título.
- Impedir envio vazio ou somente com espaços.
- Criar uma nova tarefa com `concluida: false`.
- Atualizar a lista preservando as tarefas anteriores.
- Limpar o campo após um envio válido.
- Mostrar uma orientação para entrada inválida.

## Uso de DaisyUI

Use `fieldset`, `label`, `input` e `btn btn-primary` no formulário. Apresente validação com `alert alert-error` e o novo item com o mesmo `card` usado na lista. O atributo `disabled` pode ser combinado com o botão, mas a validação também deve existir na função de envio.

**Verificação:** testar envio pelo botão e pela tecla Enter; o campo precisa manter um nome acessível e o foco deve continuar visível.

## Testes manuais

| Entrada | Resultado esperado |
| --- | --- |
| Título válido | Nova tarefa pendente aparece |
| Campo vazio | Nada é adicionado e aparece uma orientação |
| Somente espaços | Nada é adicionado |

## Extensão

Mostrar a quantidade de caracteres e limitar o título a 60 caracteres.

## Erros esperados

- Limpar o campo antes de criar o objeto.
- Substituir a lista inteira pela nova tarefa.
- Criar a tarefa inicialmente como concluída.
- Validar o texto sem remover espaços externos.

## Plano de recuperação

Entregar pronta a função que cria a tarefa e pedir que os alunos conectem estado, campo e envio. Depois incluir a validação vazia.

## Evidência de aprendizagem

Cada dupla entrega a tabela de testes preenchida e explica por que a nova tarefa respeita o tipo `Tarefa`.
