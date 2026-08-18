# Aula 8 — Componente `ItemTarefa` e props tipadas

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** contrato de props
- **Produto do encontro:** tarefas estáticas exibidas pelo mesmo componente
- **Pré-requisito:** tipos básicos e criação de componentes
- **OpenCode:** ainda não será usado
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Criar um componente visual para uma tarefa.
- Definir um `type` para suas props.
- Diferenciar título e estado de conclusão.
- Corrigir props ausentes ou incompatíveis usando a IDE.

## Preparação do professor

- Manter `ItemTarefa` na mesma pasta de `App`.
- Preparar três tarefas de exemplo: duas pendentes e uma concluída.
- Usar somente `titulo` e `concluida` nesta aula.
- Preparar uma chamada correta e duas incorretas.

## Explicação em linguagem simples

O componente é o molde visual de uma tarefa. As props informam qual texto entra no molde e se aquela tarefa já foi concluída.

## Exemplo-base

```tsx
type ItemTarefaProps = {
  titulo: string;
  concluida: boolean;
};

export default function ItemTarefa({ titulo, concluida }: ItemTarefaProps) {
  return (
    <li>
      <span>{titulo}</span>
      <strong>{concluida ? "Concluída" : "Pendente"}</strong>
    </li>
  );
}
```

## Roteiro de 80 minutos

1. **10 min — Revisão:** classificar o título e o estado de uma tarefa.
2. **15 min — Componente:** criar a estrutura de `ItemTarefa`.
3. **15 min — Contrato:** escrever `ItemTarefaProps` coletivamente.
4. **30 min — Prática:** renderizar tarefas diferentes e corrigir props inválidas.
5. **10 min — Fechamento:** usar autocomplete e explicar um aviso.

## Prática essencial

- Criar e exportar `ItemTarefa`.
- Importá-lo em `App`.
- Renderizar três tarefas com títulos diferentes.
- Exibir visualmente se cada tarefa está pendente ou concluída.
- Criar um erro de tipo intencional e corrigi-lo.

## Uso de DaisyUI

Monte `ItemTarefa` como `card card-compact`, represente a situação com `badge badge-success` ou `badge badge-warning` e mostre um `checkbox` apenas visual. Nesta aula, as props controlam texto e aparência; o checkbox ainda não altera o estado.

**Verificação:** `concluida` deve decidir qual badge aparece. Não crie dois componentes diferentes para pendente e concluída.

## Extensão

Adicionar a prop `prioridade: string` somente como texto visual, sem criar regras de prioridade.

## Verificação rápida

- O mesmo componente exibe tarefas diferentes?
- As props possuem os tipos corretos?
- O aluno sabe apontar onde uma prop é enviada e recebida?

## Erros esperados

- Escrever `"false"` como texto em vez de usar o booleano `false`.
- Usar nomes diferentes no `type` e na desestruturação.
- Criar um componente separado para cada tarefa.

## Plano de recuperação

Começar somente com `titulo: string`. Quando duas tarefas diferentes aparecerem, acrescentar `concluida: boolean`.

## Evidência de aprendizagem

O aluno cria uma chamada errada de propósito, prevê o aviso e demonstra a correção.
