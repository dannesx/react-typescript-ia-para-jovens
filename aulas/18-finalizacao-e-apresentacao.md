# Aula 18 — Apresentação do projeto final

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** aplicação final com API e IA
- **Conceito principal:** demonstrar, verificar e explicar o próprio trabalho
- **Produto do encontro:** apresentação da aplicação e do processo
- **Organização:** mesmos grupos das aulas 14–17
- **OpenCode:** revisão final curta e sem ampliação de escopo
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Executar uma última verificação antes da apresentação.
- Explicar como os dados chegam da API.
- Demonstrar estados da tela e interação principal.
- Relatar como o OpenCode foi utilizado e verificado.
- Apresentar aprendizados mesmo se uma parte estiver incompleta.

## Preparação do professor

- Definir ordem e tempo das apresentações.
- Disponibilizar cronômetro visível.
- Preparar a rubrica em papel ou formulário.
- Manter JSON local e uma máquina de demonstração como contingência.
- Confirmar que nenhuma conversa ou dado pessoal será compartilhado publicamente.

## Prioridades finais

1. Fazer a página abrir.
2. Confirmar carregamento, erro, vazio e sucesso.
3. Confirmar a interação principal.
4. Preparar a explicação.
5. Corrigir somente bloqueios.

## Roteiro de 80 minutos

1. **5 min — Organização:** distribuir papéis e revisar prioridades.
2. **15 min — Verificação final:** executar testes essenciais.
3. **10 min — OpenCode:** pedir revisão somente de erros bloqueadores.
4. **10 min — Ensaio:** preparar demonstração de quatro minutos.
5. **35 min — Apresentações:** ajustar conforme a quantidade de grupos.
6. **5 min — Fechamento:** registrar conquistas e próximos passos.

> Se houver muitos grupos, organize uma feira em duas rodadas: metade apresenta enquanto a outra visita e depois os papéis são trocados.

## Prompt de revisão final

```text
Faça uma revisão final somente para erros que impeçam a página de abrir,
a API de mostrar seus estados ou a interação principal de funcionar.
Não instale bibliotecas, não reorganize arquivos, não altere o visual e não crie funcionalidades.
Liste os problemas por prioridade e espere aprovação antes de editar.
Para cada correção aprovada, informe qual teste deve ser repetido.
```

## Testes mínimos

| Teste | Resultado esperado | Resultado observado | Situação |
| --- | --- | --- | --- |
| Abrir a página | Interface principal aparece |  |  |
| Carregar dados | Um dos estados previstos aparece |  |  |
| Usar a interação | Resultados mudam corretamente |  |  |
| Entrada sem resultado | Orientação apropriada aparece |  |  |

## Uso de DaisyUI

Antes da apresentação, confira se `card`, `btn`, `input`, `select`, `alert`, `loading` e `badge` são usados de forma consistente. Não troque o tema ou redesenhe a página nesta aula. Na fala, o grupo deve citar um componente DaisyUI e explicar qual problema visual ou de estado ele resolveu.

**Verificação:** a demonstração precisa incluir foco por teclado e pelo menos um estado além do sucesso.

## Roteiro de apresentação

Cada grupo responde:

1. Qual pergunta ou necessidade o projeto atende?
2. Qual API foi usada?
3. Qual tipo representa os dados principais?
4. Como carregamento, erro, vazio e sucesso aparecem?
5. Quais componentes foram criados?
6. Qual é a interação principal?
7. Em qual tarefa o OpenCode ajudou?
8. Como a resposta da IA foi verificada?
9. Qual sugestão da IA foi alterada, adiada ou recusada?
10. Qual seria o próximo passo do projeto?

## Rubrica rápida

| Critério | Em desenvolvimento | Atingiu o esperado | Foi além |
| --- | --- | --- | --- |
| API e estados | Dados ou estados ainda apresentam erros | API e quatro estados são demonstrados | Contingências também são explicadas |
| React e TypeScript | Explica somente com muita ajuda | Identifica componentes, props, estado e tipo | Justifica a organização dos dados |
| Interação | Funciona apenas em um caso | Casos neutro, positivo e vazio funcionam | A interação também é acessível por teclado |
| Uso da IA | Aceitou mudanças sem revisar | Revisou, testou e explicou | Questionou ou recusou sugestão inadequada |
| Comunicação | Mostra a tela sem explicar o processo | Explica ideia, API, código e testes | Relata problema, tentativa e aprendizado |

## Se o projeto estiver incompleto

O grupo ainda apresenta:

- A parte funcional.
- O estado atual do erro.
- Uma hipótese sobre a causa.
- O teste que faria após a correção.
- A forma como usou ou recusou ajuda da IA.
- O que aprendeu durante a tentativa.

Não substitua uma solução compreendida por uma versão maior gerada pela IA minutos antes da apresentação.

## Fechamento coletivo

Cada aluno completa:

- “Hoje eu consigo criar” — indicar uma habilidade aprendida.
- “Quando uso dados de uma API, preciso” — indicar uma verificação importante.
- “Quando a IA sugere código, preciso” — indicar uma atitude responsável.

## Evidência de aprendizagem

Aplicação, tabela de testes, registro do prompt principal e explicação oral do grupo.
