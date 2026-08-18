# Aula 16 — Interação principal criada com OpenCode

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** aplicação final com API e IA
- **Conceito principal:** delegar uma funcionalidade pequena e verificável
- **Produto do encontro:** busca, filtro ou categoria funcionando
- **Pré-requisito:** dados da API renderizados
- **OpenCode:** edita após plano e aprovação

## Objetivos

- Escrever um pedido com contexto, objetivo, limites e testes.
- Avaliar o plano antes de permitir edição.
- Preservar os dados originais recebidos da API.
- Ler os arquivos modificados.
- Testar a interação em pelo menos três situações.

## Escolha de uma interação

Cada grupo implementa somente uma:

- Buscar por nome.
- Filtrar por categoria existente nos dados.
- Selecionar uma opção e mostrar seus detalhes.

A interação precisa usar campos já aprovados. Não é permitido trocar de API ou adicionar uma segunda fonte de dados.

## Preparação do professor

- Confirmar que a versão da aula 15 funciona.
- Criar uma cópia recuperável do projeto.
- Definir arquivos permitidos para edição.
- Preparar um pedido vago e um delimitado para comparação.
- Demonstrar `/undo` em uma cópia descartável.

## Roteiro de 80 minutos

1. **10 min — Escolha:** definir a única interação do grupo.
2. **10 min — Prompt:** preencher contexto, objetivo, limites e testes.
3. **15 min — Plano:** ler, questionar e aprovar ou pedir ajuste.
4. **30 min — Implementação:** acompanhar cada arquivo alterado.
5. **15 min — Verificação:** executar três testes e explicar o fluxo.

## Prompt-base para busca

```text
Estou em um projeto React com TypeScript que já recebe e mostra dados de uma API.
Quero adicionar uma busca pelo campo de nome sem alterar a lista original.
Antes de editar, apresente um plano e diga quais arquivos pretende modificar.
Não instale bibliotecas, não reorganize pastas, não troque a API e não altere estilos fora da busca.
Considere estes testes: texto vazio, nome encontrado e nome não encontrado.
Depois da aprovação, faça somente essa mudança e explique cada alteração com palavras simples.
```

## Critérios para aprovar o plano

- Resolve somente a interação escolhida?
- Preserva os dados originais?
- Usa tipos e estados existentes?
- Evita bibliotecas e reorganizações?
- Inclui todos os testes definidos?

## Prática essencial

- Registrar o prompt enviado.
- Solicitar ajuste se o plano ultrapassar o escopo.
- Aprovar somente arquivos esperados.
- Ler cada trecho alterado.
- Executar três testes.
- Usar `/undo` se a alteração sair do escopo e registrar o motivo.

## Testes mínimos

| Situação | Resultado esperado |
| --- | --- |
| Entrada neutra ou vazia | Todos os itens continuam visíveis |
| Correspondência encontrada | Apenas resultados correspondentes aparecem |
| Nenhuma correspondência | Mensagem específica aparece |

## Extensão

Melhorar a interação para ignorar diferenças entre letras maiúsculas e minúsculas, sem alterar o escopo restante.

## Erros esperados

- Aprovar o plano sem ler.
- Substituir a lista original pelos resultados filtrados.
- Testar somente o caso de sucesso.
- Permitir alterações visuais amplas junto com a lógica.

## Plano B

Se o OpenCode estiver indisponível, usar um plano e um diff simulados preparados pelo professor. A turma revisa o material, encontra uma mudança fora de escopo e implementa a versão corrigida.

## Evidência de aprendizagem

Cada grupo entrega prompt, plano aprovado, três resultados de teste e uma explicação de como verificou a resposta da IA.

