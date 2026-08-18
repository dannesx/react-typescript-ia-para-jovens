# Aula 4 — Props

> Aula realizada. Este registro serve para revisão e alinhamento com as aulas seguintes.

## Ficha da aula

- **Duração:** 80 minutos
- **Conceito principal:** props
- **Produto do encontro:** comentários diferentes usando o mesmo componente
- **Pré-requisito:** criar, exportar e importar componentes

## Objetivos

- Entender props como informações recebidas por um componente.
- Identificar quem envia e quem recebe cada informação.
- Reutilizar um componente com conteúdos diferentes.

## Explicação em linguagem simples

O componente é como um molde. As props são as informações colocadas no molde para produzir resultados diferentes.

## Preparação do professor

- Preparar dois comentários com nomes e mensagens diferentes.
- Manter inicialmente poucas props: `nome`, `mensagem` e `avatar` opcional no exercício avançado.

## Roteiro de 80 minutos

1. **10 min — Revisão:** reutilizar um componente idêntico duas vezes.
2. **15 min — Problema:** perguntar como mudar somente o texto de cada cópia.
3. **20 min — Demonstração:** enviar e receber `nome` e `mensagem`.
4. **25 min — Prática:** criar três comentários diferentes.
5. **10 min — Fechamento:** turma aponta remetente e destinatário de cada prop.

## Desafio essencial

Criar um componente `Comentario` que receba e mostre:

- Nome da pessoa.
- Mensagem do comentário.

## Extensão

Adicionar uma prop para quantidade de curtidas.

## Verificação rápida

- O conteúdo não está fixo dentro do componente?
- O mesmo componente exibe informações diferentes?
- O aluno sabe indicar onde a prop é enviada e recebida?

## Erros esperados

- Usar nomes diferentes ao enviar e receber a prop.
- Esquecer as chaves ao mostrar uma prop no JSX.
- Criar um componente diferente para cada comentário.

## Plano de recuperação

Começar com apenas uma prop chamada `mensagem`. Acrescentar `nome` somente após a primeira funcionar.

