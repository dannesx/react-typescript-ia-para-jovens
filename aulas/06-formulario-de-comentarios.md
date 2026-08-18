# Aula 6 — Formulário de comentários

> Aula realizada. Este registro serve para revisão e alinhamento com as aulas seguintes.

## Ficha da aula

- **Duração:** 80 minutos
- **Conceito principal:** transformar uma ação do usuário em mudança de estado
- **Produto do encontro:** formulário que adiciona comentários à página
- **Pré-requisito:** props e `useState`

## Objetivos

- Responder aos eventos do formulário.
- Adicionar um item a uma lista sem apagar os anteriores.
- Renderizar os comentários com `map`.
- Limpar o campo depois do envio.

## Preparação do professor

- Manter uma versão funcional para demonstração.
- Preparar uma lista inicial curta.
- Separar visualmente formulário e lista, mesmo que ainda estejam no mesmo componente.

## Roteiro de 80 minutos

1. **10 min — Revisão:** acompanhar o texto digitado no estado.
2. **15 min — Envio:** capturar o evento e impedir o recarregamento.
3. **20 min — Lista:** adicionar o novo comentário ao estado.
4. **25 min — Renderização:** usar `map` para exibir a lista.
5. **10 min — Teste:** adicionar vários comentários e limpar o campo.

## Desafio essencial

- Digitar uma mensagem.
- Enviar o formulário sem recarregar a página.
- Ver a nova mensagem na lista.
- Manter os comentários anteriores.
- Limpar o campo após o envio.

## Extensão

Desabilitar o botão quando o campo estiver vazio.

## Verificação rápida

- A página permanece aberta após o envio?
- Um novo item é criado sem alterar os anteriores?
- Cada item é renderizado pelo `map`?

## Erros esperados

- Esquecer `preventDefault`.
- Substituir a lista inteira pelo novo comentário.
- Usar uma `key` instável ou repetida.
- Limpar o campo antes de usar seu conteúdo.

## Plano de recuperação

Fornecer a função de envio com três lacunas: mensagem atual, lista anterior e limpeza do campo. Preencher uma por vez e testar após cada alteração.
