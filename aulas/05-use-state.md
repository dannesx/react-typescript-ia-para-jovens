# Aula 5 — Estado com `useState`

> Aula realizada. Este registro serve para revisão e alinhamento com as aulas seguintes.

## Ficha da aula

- **Duração:** 80 minutos
- **Conceito principal:** estado
- **Produto do encontro:** campo de comentário controlado pelo React
- **Pré-requisito:** componentes e props
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Diferenciar uma informação fixa de uma informação que muda.
- Criar um estado com `useState`.
- Atualizar o estado e observar a nova renderização.

## Explicação em linguagem simples

Estado é a memória do componente. Quando essa memória muda, o React atualiza a parte necessária da tela.

## Preparação do professor

- Preparar um contador curto como demonstração inicial.
- Manter o formulário apenas com um campo de texto.
- Projetar o valor do estado na tela durante a explicação.

## Roteiro de 80 minutos

1. **10 min — Pergunta inicial:** quais informações de uma página podem mudar?
2. **15 min — Demonstração:** contador com estado.
3. **15 min — Anatomia:** valor atual e função de atualização.
4. **30 min — Prática:** controlar o campo de comentário.
5. **10 min — Fechamento:** explicar por que a tela acompanha a digitação.

## Desafio essencial

- Criar o estado do texto.
- Ligar o valor do campo ao estado.
- Atualizar o estado quando o aluno digitar.
- Mostrar o texto atual abaixo do campo.

## Uso de DaisyUI

Use `input` no campo, `btn btn-primary` no botão de demonstração e `badge` na contagem de caracteres. Mostre que o estado altera valores e textos, enquanto DaisyUI controla a aparência dos elementos.

**Verificação:** a interação deve continuar funcionando quando um modificador visual, como `btn-primary`, for trocado por outro tema.

## Extensão

Exibir também a quantidade de caracteres digitados.

## Verificação rápida

- O campo recebe o valor do estado?
- A função de atualização é chamada no evento?
- O texto mostrado acompanha a digitação?

## Erros esperados

- Chamar a função de atualização imediatamente no JSX.
- Alterar diretamente a variável de estado.
- Esquecer de importar `useState`.

## Plano de recuperação

Entregar o `useState` pronto e pedir que o aluno conecte primeiro o `value`, depois o evento de alteração.
