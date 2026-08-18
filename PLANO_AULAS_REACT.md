# Plano de aulas de React

## Visão geral

- **Público:** turma com idade média de 13 anos
- **Quantidade:** 18 aulas
- **Duração de referência:** 80 minutos por aula
- **Abordagem:** pouca teoria, demonstrações curtas e bastante prática guiada
- **Projeto 1 — aulas 1 a 6:** cópia simplificada de uma página do YouTube *(concluído)*
- **Projeto 2 — aulas 7 a 13:** lista de tarefas com React e TypeScript
- **Projeto 3 — aulas 14 a 18:** projeto final com API e desenvolvimento assistido por IA
- **TypeScript:** introduzido a partir da aula 7 como apoio da IDE para encontrar erros
- **IA no desenvolvimento:** uso contínuo do OpenCode em todas as aulas, da aula 10 até o projeto final
- **Projeto final:** aplicação pequena escolhida pela turma

O objetivo não é ensinar todo o React, mas fazer com que os alunos entendam os conceitos fundamentais, consigam alterar uma interface e sintam confiança para criar projetos simples.

O OpenCode deve entrar como um parceiro de investigação. Os alunos continuam responsáveis por explicar o código, revisar as mudanças e testar o resultado. Para essa faixa etária, o professor deve preparar as contas, os modelos e as permissões antes das aulas, sem expor chaves de API aos estudantes.

## Objetivos ao final do curso

Ao final das 18 aulas, espera-se que o aluno consiga:

- Dividir uma interface pequena em componentes.
- Passar informações por props e alterar a tela com `useState`.
- Renderizar listas e responder a eventos.
- Criar tipos simples para props e objetos.
- Usar os avisos do TypeScript para localizar erros.
- Buscar e apresentar dados de uma API simples.
- Pedir ajuda à IA de forma limitada, revisar a resposta e testar o resultado.
- Explicar as partes principais do próprio projeto.

## Ritmo sugerido para cada aula

1. **Revisão e conversa inicial — 10 min:** relembrar a aula anterior com perguntas simples.
2. **Demonstração — 15 min:** apresentar apenas um conceito novo.
3. **Prática guiada — 25 min:** professor e turma programam juntos.
4. **Desafio curto — 20 min:** alunos fazem uma pequena alteração sozinhos ou em duplas.
5. **Fechamento — 10 min:** mostrar resultados, corrigir dúvidas e salvar o projeto.

> Ajuste os tempos conforme a duração real das aulas. Para essa faixa etária, é melhor concluir uma tarefa pequena do que correr para cobrir muitos assuntos.

### Regra para avançar

Antes de apresentar o próximo conceito, faça três perguntas rápidas:

1. A maioria da turma consegue localizar o arquivo que precisa alterar?
2. A maioria consegue explicar o conceito anterior com um exemplo?
3. A maioria concluiu a interação principal, mesmo com ajuda?

Se duas respostas forem “não”, use o início da aula seguinte para repetir a prática em vez de acrescentar conteúdo.

---

## Bloco 1 — Primeiros passos e projeto do YouTube

### Aula 1 — Conhecendo o React e os componentes *(realizada)*

**Tópicos**

- O que é uma página web e onde o React entra
- Estrutura básica de um projeto React
- Componentes como “peças de LEGO” da interface
- Criação do primeiro componente

**Resultado esperado:** exibir um componente simples na tela.

### Aula 2 — JSX e divisão da página *(realizada)*

**Tópicos**

- Mistura de HTML e JavaScript com JSX
- Regras básicas do JSX
- Separação da página em componentes menores
- Início da cópia visual da página do YouTube

**Resultado esperado:** dividir a página em partes como cabeçalho, vídeo e comentários.

### Aula 3 — Reutilização de componentes *(realizada)*

**Tópicos**

- Criar componentes reutilizáveis
- Importar e exportar componentes
- Montar a página usando vários componentes
- Pequenos ajustes de estilo

**Resultado esperado:** montar a estrutura da página com componentes separados.

### Aula 4 — Props *(realizada)*

**Tópicos**

- Props como informações entregues a um componente
- Exibir textos e imagens diferentes com o mesmo componente
- Criar comentários usando dados recebidos por props

**Resultado esperado:** reutilizar o componente de comentário com conteúdos diferentes.

### Aula 5 — Estado com `useState` *(realizada)*

**Tópicos**

- Diferença entre uma variável comum e um estado
- Criação de estado com `useState`
- Atualização da tela quando o estado muda
- Campo de texto controlado pelo React

**Resultado esperado:** digitar no formulário e guardar o texto no estado.

### Aula 6 — Formulário de comentários *(realizada)*

**Tópicos**

- Evento de envio do formulário
- Eventos de clique e alteração dos campos
- Adicionar um comentário à lista
- Renderização dos comentários com `map`
- Limpar o campo depois do envio
- Uso do `useState` para controlar os comentários da página

**Resultado esperado:** enviar um novo comentário e vê-lo aparecer na página.

### Preparação entre as aulas 6 e 7

Para que a configuração não consuma a aula, o professor deve preparar previamente um novo projeto vazio em React com TypeScript:

- Confirmar que o projeto abre sem erros antes de entregá-lo à turma.
- Criar uma identidade visual simples e própria para o Todo List.
- Manter somente o mínimo necessário em `App.tsx` para começar o Todo List.
- Preparar de três a cinco erros intencionais, cada um com uma única causa.
- Disponibilizar uma cópia limpa para recuperação.

Os alunos não precisam configurar o projeto sozinhos. A aula 7 começa diretamente pelo novo problema e utiliza apenas componentes, dados e textos próprios do Todo List.

---

## Projeto 2 — Todo List: base com React e TypeScript

### Aula 7 — Novo projeto e primeiros passos com TypeScript

**Tópicos**

- Apresentação do projeto de lista de tarefas
- Planejamento visual da nova interface
- Diferença visual entre arquivos `.jsx` e `.tsx`
- Tipos básicos: `string`, `number` e `boolean`
- Como ler os sublinhados e as mensagens da IDE
- TypeScript como ferramenta para encontrar erros antes de abrir a página

**Prática:** iniciar uma nova aplicação TypeScript, desenhar a tela do Todo List e criar exemplos de título, quantidade de tarefas e estado de conclusão usando tipos básicos.

**Resultado esperado:** reconhecer os três tipos básicos e usar a mensagem da IDE para localizar um erro.

> Não é necessário explicar toda a configuração do TypeScript. O foco desta aula é mostrar que a IDE pode ajudar enquanto o código está sendo escrito.

### Aula 8 — Componente `ItemTarefa` e props tipadas

**Tópicos**

- Criação de um `type` para as props
- Props obrigatórias
- Diferença entre texto, número e verdadeiro ou falso
- Erros causados por props ausentes ou com o tipo errado
- Sugestões automáticas oferecidas pela IDE

**Prática:** criar o componente `ItemTarefa`, tipar `titulo` e `concluida` e renderizar tarefas diferentes a partir do mesmo componente.

**Resultado esperado:** criar um componente com props tipadas e interpretar os erros mostrados pela IDE.

### Aula 9 — Objetos, arrays e o tipo `Tarefa`

**Tópicos**

- Objetos como grupos de informações relacionadas
- Criação do tipo `Tarefa`
- Arrays escritos como `Tarefa[]`
- Revisão de `map` usando uma lista tipada
- Autocomplete das propriedades de cada tarefa

**Prática:** criar um tipo com `id`, `titulo` e `concluida`, montar uma lista inicial e renderizá-la com `map`.

**Resultado esperado:** representar uma lista de objetos com um tipo reutilizável.

### Aula 10 — Estado tipado e início do OpenCode

**Tópicos**

- Uso de `useState<Tarefa[]>([])`
- Tipos inferidos automaticamente pelo TypeScript
- Erros ao tentar adicionar uma tarefa inválida
- Leitura de mensagens de erro sem medo
- Revisão de imports: `export`, `import`, `./` e `../`
- Primeira demonstração do OpenCode para explicar uma mensagem de erro
- Apresentação do protocolo PARE: Pedir, Analisar, Rodar e Explicar

**Prática:** mover a lista inicial para um estado tipado e realizar uma caça aos erros no Todo List. No último erro, pedir ao OpenCode apenas uma explicação e comparar a resposta com as pistas da IDE.

**Uso do OpenCode:** pedir uma pista ou explicação sem permitir que a IA altere o código. Os alunos corrigem o erro manualmente.

**Resultado esperado:** usar o TypeScript e a IDE para encontrar erros e consultar a IA sem aceitar sua resposta automaticamente.

**Verificação rápida:** cada aluno deve corrigir ao menos um erro e explicar qual pista da IDE ou do OpenCode ajudou.

---

## Projeto 2 — Todo List: interações com apoio da IA

### Aula 11 — Formulário para adicionar tarefas

**Tópicos**

- Campo controlado com `useState`
- Envio de formulário
- Validação de título vazio
- Criação de uma nova `Tarefa`
- Atualização da lista sem apagar as tarefas anteriores

**Prática:** criar um formulário que recebe o título, adiciona uma tarefa pendente e limpa o campo depois do envio.

**Uso do OpenCode:** pedir um plano curto e três testes manuais para o formulário. Os alunos implementam a solução e usam a IA apenas para revisar a função de envio.

**Resultado esperado:** adicionar tarefas válidas mantendo a lista anterior.

### Aula 12 — Concluir e excluir tarefas

**Tópicos**

- Atualização de um item pelo `id`
- Alternância do valor `concluida`
- Remoção de um item da lista
- Funções tipadas passadas por props
- Mensagem condicional para lista vazia

**Prática:** adicionar ações para marcar uma tarefa como concluída, voltar para pendente e excluir pelo `id`.

**Uso do OpenCode:** pedir que a IA explique a diferença entre transformar a lista com `map` e remover itens com `filter`, sem editar o código. Depois, solicitar testes para as duas ações.

**Resultado esperado:** atualizar e excluir a tarefa correta sem afetar as demais.

### Aula 13 — Filtros, componentes e conclusão do Todo List

**Tópicos**

- Filtros “Todas”, “Pendentes” e “Concluídas”
- Estado no componente pai
- Separação entre formulário, filtros e lista
- Contagem de tarefas pendentes
- Revisão de props e funções tipadas

**Prática:** dividir a aplicação em componentes, adicionar os três filtros e concluir o segundo projeto.

**Uso do OpenCode:** pedir um desenho textual do fluxo entre os componentes e uma revisão limitada às props, aos tipos e aos três filtros.

**Resultado esperado:** apresentar um Todo List funcional e explicar onde vivem o estado e as ações.

---

## Projeto 3 — Aplicação final: planejamento e construção

**Requisitos mínimos do projeto final**

- Consumir uma API previamente aprovada pelo professor.
- Criar um tipo TypeScript para os dados utilizados.
- Exibir carregamento, erro, lista vazia e sucesso.
- Renderizar dados com `map` e uma `key` estável.
- Separar a interface em pelo menos três componentes.
- Possuir uma interação principal, como busca, filtro ou seleção de categoria.
- Usar o OpenCode com plano, aprovação, revisão e testes.
- Registrar o prompt principal e como a resposta foi verificada.

**Temas possíveis**

- Catálogo de personagens.
- Explorador de criaturas ou monstros de jogos.
- Consulta de países ou bandeiras.
- Galeria de imagens espaciais.
- Catálogo de livros.

O professor deve oferecer poucas APIs já testadas, com conteúdo apropriado e arquivo JSON local de contingência.

### Aula 14 — Escolha do tema, API e planejamento

**Tópicos**

- API explicada como um serviço que entrega informações
- Formato JSON
- Escolha de uma API apropriada ao tema do grupo
- Definição da pergunta que o projeto responde
- Criação de um tipo para o dado recebido
- Planejamento dos componentes e estados da interface

**Prática:** em grupos, escolher uma API entre opções previamente aprovadas, analisar uma amostra JSON, selecionar até quatro campos e planejar a interface final.

**Uso do OpenCode:** pedir que a IA explique a amostra JSON, sugira um tipo TypeScript e critique o escopo do projeto sem criar código.

**Resultado esperado:** sair da aula com tema, API, tipo principal, desenho da tela e escopo aprovado.

> Escolha previamente uma API gratuita, sem autenticação e com conteúdo apropriado para menores. Tenha também um arquivo JSON local como plano B caso a internet falhe.

### Aula 15 — Primeira versão consumindo a API

**Tópicos**

- Requisição com `fetch`, `async` e `await`
- `useEffect` como ação executada quando a tela aparece
- Estado de carregamento
- Estado de erro
- Estado de lista vazia
- Renderização dos dados com `map`

**Prática:** construir a primeira versão que busca a API, mostra carregamento, erro, vazio ou uma lista tipada.

**Uso do OpenCode:** pedir um plano de implementação e permitir edição somente depois da aprovação do grupo. Testar cada estado da tela após as mudanças.

**Resultado esperado:** criar uma tela que explique ao usuário o que está acontecendo durante a busca.

### Aula 16 — Interação principal criada com OpenCode

**Tópicos**

- Revisão do que uma IA de programação consegue e não consegue fazer
- Pedido completo com contexto, objetivo, limites e resultado esperado
- Pedir primeiro uma explicação ou um plano pequeno
- Revisar as alterações antes de aceitá-las
- Usar a IDE, a página e o TypeScript para verificar a resposta
- Desfazer uma tentativa que não funcionou

**Prática:** cada grupo usa o OpenCode para implementar uma única interação principal adequada ao projeto, como busca, filtro ou seleção de categoria.

**Uso do OpenCode:** nesta aula, a IA pode editar o código depois de apresentar um plano. A turma deve acompanhar as alterações, interromper mudanças fora do pedido e testar cada estado da busca.

**Exemplo de pedido:**

> Quero adicionar uma busca à lista recebida da API. Antes de alterar o código, explique quais arquivos serão modificados. Use o estado e os tipos que já existem. Não instale bibliotecas. Depois, explique as mudanças com palavras simples.

**Resultado esperado:** usar o OpenCode para realizar uma alteração limitada, compreender o código produzido e verificar se ele funciona.

**Regra da aula:** nenhum aluno pode dizer que terminou enquanto não conseguir explicar o que a IA alterou.

---

## Projeto 3 — Aplicação final: refinamento e apresentação

### Aula 17 — Refinamento, testes e acessibilidade

**Atividades**

- Corrigir o fluxo principal antes de acrescentar melhorias
- Executar testes de carregamento, erro, vazio e sucesso
- Revisar textos, botões, labels e navegação por teclado
- Ajustar responsividade básica
- Pedir ao OpenCode revisão limitada aos critérios definidos

**Uso do OpenCode:** pedir uma revisão focada em bugs, estados da tela e acessibilidade básica. O grupo escolhe, aprova e testa cada correção.

**Resultado esperado:** possuir uma versão estável, testada e pronta para demonstração.

> O projeto final ocupa cinco aulas. Ainda assim, mantenha somente uma API, uma tela e uma interação principal. Não comece autenticação, banco de dados ou navegação entre várias páginas.

### Aula 18 — Apresentação do projeto final

**Tópicos**

- Correção de pequenos erros
- Organização e limpeza do código
- Ajustes de texto, cores e espaçamento
- Teste das principais ações
- Revisão final com OpenCode
- Apresentação dos projetos

**Uso do OpenCode:** pedir uma revisão limitada a erros de TypeScript, imports e comportamentos quebrados. A IA pode sugerir melhorias, mas o grupo decide o que será alterado e executa novamente os testes manuais.

**Roteiro de apresentação**

1. Qual é a ideia do projeto?
2. Quais componentes foram criados?
3. Onde foram usadas props?
4. Qual tipo foi criado no projeto?
5. O que muda com `useState`?
6. Qual erro o TypeScript ajudou a encontrar?
7. Em que tarefa a IA ajudou?
8. Como o grupo verificou se a resposta da IA estava correta?
9. Qual parte foi mais divertida ou difícil?

**Resultado esperado:** apresentar uma aplicação com API, explicar a interação construída com IA e demonstrar como o grupo verificou o resultado.

**Plano de contingência:** reserve os primeiros 40 minutos para terminar e testar. Se um grupo não concluir tudo, ele apresenta a parte funcional, mostra o erro atual e explica qual seria o próximo passo. Código incompleto também pode demonstrar aprendizagem.

---

## Protocolo para usar IA em sala *(apresentar antes da aula 10)*

Uma regra curta pode ajudar a turma a não transformar a atividade em “copiar e colar”:

### PARE

1. **Pedir:** descrever uma tarefa pequena e informar o que não deve ser alterado.
2. **Analisar:** ler a explicação e observar os arquivos modificados.
3. **Rodar:** abrir a página, testar a interação e conferir os erros da IDE.
4. **Explicar:** contar com palavras próprias o que mudou no código.

### Progressão de autonomia do OpenCode

| Aulas | Papel da IA | Pode editar código? | Responsabilidade dos alunos |
| --- | --- | --- | --- |
| 10 | Dar pistas e explicar erros | Não | Fazer a correção manualmente |
| 11–14 | Sugerir planos, explicações, testes e revisões | Não | Escolher e implementar as sugestões |
| 15–18 | Implementar uma tarefa pequena e delimitada | Sim, com aprovação | Ler as mudanças, testar e explicar o resultado |

Em todas as fases, o professor pode reduzir a autonomia caso a turma esteja aceitando respostas sem compreender as alterações.

### Regras para os alunos

- Não enviar nome completo, e-mail, senha, telefone, foto ou outro dado pessoal.
- Nunca colar chaves, tokens ou senhas no chat ou no código.
- Não pedir um projeto inteiro de uma só vez.
- Não aceitar uma mudança sem ler os arquivos alterados.
- Não considerar a resposta correta apenas porque veio da IA.
- Pedir explicações simples quando não entender uma sugestão.
- Avisar o professor antes de permitir instalação de pacotes ou execução de comandos desconhecidos.
- Guardar o pedido usado e anotar, em uma frase, se a resposta ajudou ou não.

### Preparação do professor

- Instalar e conectar o OpenCode antes da aula.
- Usar contas e credenciais administradas pelo professor ou pela instituição.
- Manter aprovação manual para alterações e comandos.
- Preparar uma cópia recuperável do projeto de cada grupo.
- Demonstrar como revisar as mudanças e usar `/undo` quando uma tentativa não funcionar.
- Evitar o compartilhamento público das conversas e dos projetos dos alunos.
- Definir previamente quais modelos e limites de uso estarão disponíveis.
- Testar o OpenCode nos computadores da sala e preparar uma demonstração gravada ou capturas de tela como plano B.

### Formas adequadas de pedir ajuda

- “Explique este erro do TypeScript sem alterar o código.”
- “Encontre o possível problema e me dê uma pista, não a resposta completa.”
- “Antes de editar, diga quais arquivos pretende modificar.”
- “Faça apenas esta pequena mudança e não instale bibliotecas.”
- “Explique cada alteração como se eu tivesse 13 anos.”
- “Crie três testes manuais que eu possa fazer na página.”

### Formas inadequadas de pedir ajuda

- “Faça todo o trabalho para mim.”
- “Crie o projeto inteiro.”
- “Mude tudo que achar necessário.”
- “Execute qualquer comando sem perguntar.”

---

## Conteúdos que podem ficar para um próximo curso

Para não sobrecarregar a turma, estes assuntos não precisam fazer parte das 18 aulas:

- Context API
- Gerenciadores de estado
- Criação de hooks personalizados
- Testes automatizados
- TypeScript avançado
- Autenticação e banco de dados
- Otimizações como `useMemo` e `useCallback`
- Deploy complexo

Caso a turma avance rapidamente, uma publicação simples do projeto final pode ser apresentada como atividade extra.

## Recomendações para a turma

- Introduza no máximo **um conceito principal por aula**.
- Use exemplos próximos do cotidiano dos alunos: jogos, vídeos, música e escola.
- Evite longos períodos copiando código; pare a cada pequeno bloco para testar.
- Trabalhe em duplas quando houver diferença grande de ritmo.
- Celebre alterações visuais e resultados funcionando, mesmo que o código ainda não esteja perfeito.
- Use nomes de variáveis em português no início, se isso facilitar a compreensão.
- Traduza as mensagens do TypeScript para linguagem comum e corrija um erro por vez.
- Trate os avisos da IDE como pistas de investigação, não como punições.
- Repita os conceitos em contextos diferentes antes de aumentar a dificuldade.
- Avalie mais a compreensão e a evolução do que a memorização da sintaxe.

## Avaliação sugerida

A avaliação pode ser contínua e leve:

- **Participação e experimentação:** tenta modificar o código, observa o resultado e faz novas tentativas.
- **Compreensão de React e TypeScript:** explica componentes, props, estado e pelo menos um tipo criado.
- **Uso responsável da IA:** escreve pedidos limitados, lê as alterações e não apresenta uma resposta da IA como verdade automática.
- **Verificação:** testa o caminho principal e pelo menos um caso de erro ou lista vazia.
- **Comunicação:** apresenta o projeto e explica uma decisão tomada pelo grupo.

### Rubrica simples para o projeto final

| Critério | Em desenvolvimento | Atingiu o esperado | Foi além |
| --- | --- | --- | --- |
| Funcionamento | A interação principal ainda apresenta erros | A interação principal funciona | Também trata casos de erro ou vazio |
| Componentes e tipos | Precisa de ajuda para localizar ou explicar | Identifica componentes, props, estado e tipos | Consegue justificar como organizou os dados |
| Uso da IA | Aceita sugestões sem revisar | Revisa, testa e explica a mudança | Questiona ou melhora uma sugestão inadequada |
| Apresentação | Mostra o projeto com muita ajuda | Explica a ideia e uma parte do código | Relata um problema, tentativa e solução |

Não é necessário aplicar uma prova teórica. Os projetos e as explicações dos próprios alunos oferecem evidências melhores de aprendizagem para essa faixa etária.
