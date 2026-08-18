# React, TypeScript e IA para jovens

Plano de 18 aulas introdutórias de desenvolvimento de interfaces para uma turma com idade média de 13 anos.

O material apresenta React de forma gradual, usa DaisyUI como biblioteca visual já conhecida, TypeScript como apoio para encontrar erros na IDE e desenvolvimento assistido por IA com OpenCode. A proposta prioriza prática guiada, projetos pequenos e compreensão do código acima da memorização de sintaxe.

## Objetivos

Ao final da sequência, espera-se que os alunos consigam:

- Dividir uma interface em componentes.
- Passar informações usando props.
- Alterar a tela com `useState`.
- Trabalhar com eventos, formulários e listas.
- Montar interfaces consistentes com componentes DaisyUI.
- Criar tipos simples para props e objetos.
- Interpretar avisos básicos do TypeScript.
- Consumir e apresentar dados de uma API simples.
- Pedir ajuda à IA, revisar suas sugestões e testar o resultado.
- Construir e apresentar uma aplicação pequena.

## Os três projetos

| Projeto | Aulas | Produto e conteúdo |
| --- | --- | --- |
| Página de vídeo | 1–6 | Componentes, JSX, imports, props, `useState`, eventos, formulário de comentários e `map` |
| Todo List | 7–13 | Novo projeto com TypeScript, tarefas tipadas, formulário, conclusão, exclusão e filtros |
| Aplicação com API e IA | 14–18 | Planejamento, JSON, API, estados da tela, interação assistida, testes e apresentação |

As aulas 1–6 registram conteúdos já realizados. Na aula 7, a turma começa um projeto completamente novo e deixa o contexto da página de vídeo para trás. TypeScript começa junto com o Todo List, e o OpenCode passa a ser usado continuamente da aula 10 até o projeto final.

## Documentos

- [Plano completo das 18 aulas](PLANO_AULAS_REACT.md)
- [Índice dos roteiros individuais](aulas/README.md)
- [Aulas individuais](aulas/)
- [Wireframe HTML da aula 7](wireframes/aula-07.html)

Cada roteiro individual contém:

- Objetivos observáveis.
- Preparação do professor.
- Roteiro de 80 minutos.
- Prática essencial e atividade de extensão.
- Erros esperados e plano de recuperação.
- Verificação ou evidência de aprendizagem.
- Prompts e limites para o OpenCode, quando aplicável.

## Como utilizar

1. Leia o [plano geral](PLANO_AULAS_REACT.md) para compreender a progressão.
2. Abra o roteiro individual antes de cada encontro.
3. Prepare o projeto-base, os erros intencionais e os planos de contingência indicados.
4. Adapte o tempo à realidade da turma.
5. Só avance quando a maioria conseguir explicar e aplicar o conceito anterior.
6. Registre dificuldades recorrentes para retomá-las no início da aula seguinte.

O ritmo sugerido para uma aula de 80 minutos é:

1. 10 minutos de revisão.
2. 15 minutos de demonstração.
3. 25 minutos de prática guiada.
4. 20 minutos de desafio curto.
5. 10 minutos de fechamento.

## Uso de TypeScript

TypeScript não é tratado como um conteúdo avançado. Ele funciona como uma rede de proteção para que os alunos encontrem erros na IDE antes de descobri-los somente ao abrir a página.

O curso se concentra em:

- `string`, `number` e `boolean`.
- Tipagem de props.
- Tipos simples de objetos.
- Arrays tipados.
- Tipagem básica de `useState`.

Assuntos como generics avançados, tipos condicionais, assertions e tipos utilitários ficam fora do escopo.

## Uso de DaisyUI

DaisyUI é assumido como conteúdo já apresentado à turma. Todos os projetos-base devem chegar com Tailwind CSS e DaisyUI configurados pelo professor. As aulas usam classes conhecidas para concentrar o tempo em React, TypeScript e lógica.

Os exemplos deste material seguem DaisyUI 5 com Tailwind CSS 4. No projeto Vite, o professor prepara as dependências e o plugin do Tailwind; no arquivo CSS principal, a base esperada é:

```css
@import "tailwindcss";
@plugin "daisyui";
```

Caso a turma utilize outra versão, ajuste as classes do material antes da aula em vez de realizar uma migração ao vivo.

Componentes recorrentes:

- `navbar`, `card`, `avatar` e `divider` na página de vídeo.
- `input`, `textarea`, `btn`, `badge` e `checkbox` nos formulários e listas.
- `alert`, `loading` e `skeleton` nos estados de requisição.
- `tabs`, `select` e `stats` em filtros e resumos.

DaisyUI resolve a base visual, mas não substitui HTML semântico. Campos continuam precisando de labels, botões devem ter nomes compreensíveis e todas as ações precisam funcionar por teclado.

## Uso de IA com OpenCode

O OpenCode é apresentado como parceiro de investigação, não como substituto da aprendizagem. A turma utiliza o protocolo **PARE**:

1. **Pedir:** descrever uma tarefa pequena e seus limites.
2. **Analisar:** ler a resposta e as alterações propostas.
3. **Rodar:** testar a página e conferir os avisos da IDE.
4. **Explicar:** descrever com palavras próprias o que mudou.

A autonomia da IA cresce gradualmente:

- Aula 10: oferece pistas e explicações, sem editar.
- Aulas 11–14: sugere planos, explicações, testes e revisões sem assumir o projeto.
- Aulas 15–18: pode editar tarefas pequenas depois de apresentar um plano e receber aprovação.

### Segurança e privacidade

- Não inserir nomes completos, contatos, fotos, senhas ou dados pessoais.
- Nunca compartilhar chaves de API ou tokens.
- Manter aprovação manual para edições e comandos.
- Não permitir instalação de pacotes sem autorização do professor.
- Não compartilhar publicamente conversas ou projetos dos alunos.
- Manter cópias recuperáveis antes de atividades com edição por IA.

O professor ou a instituição deve verificar previamente as políticas aplicáveis, as permissões e a forma adequada de acesso para menores.

## Abordagem pedagógica

- Um conceito principal por aula.
- Exemplos relacionados a jogos, vídeos, música e escola.
- Testes frequentes depois de pequenas alterações.
- Trabalho em duplas ou trios quando necessário.
- Valorização da explicação e da evolução individual.
- Avaliação prática, contínua e sem dependência de prova teórica.

## Segundo projeto: Todo List

Entre as aulas 7 e 13, os alunos constroem uma lista de tarefas do zero. Esse projeto ensina TypeScript dentro de um contexto diferente do primeiro projeto e termina com:

- Criação de tarefas.
- Validação de entrada.
- Conclusão e reabertura.
- Exclusão pelo identificador.
- Filtros de todas, pendentes e concluídas.
- Separação entre formulário, filtros e lista.

## Terceiro projeto: aplicação com API e IA

Nas aulas 14–18, os alunos trabalham em grupos para planejar e construir uma aplicação baseada em uma API aprovada pelo professor. O tema pode envolver personagens, criaturas de jogos, países, imagens espaciais ou livros.

O escopo mínimo inclui uma API, tipo TypeScript, componentes, estados de carregamento, erro, vazio e sucesso, uma lista com `map` e uma interação principal criada com apoio do OpenCode.

## Status

- [x] Plano curricular com 18 aulas
- [x] Roteiros individuais
- [x] Progressão de TypeScript
- [x] DaisyUI integrado aos três projetos
- [x] Uso contínuo e responsável de OpenCode
- [x] Projeto final e rubrica de avaliação

## Licença

Este repositório ainda não possui uma licença definida. Antes de aceitar contribuições ou reutilização externa, escolha uma licença compatível com o objetivo do material.
