# Aula 14 — Escolha do tema, API e planejamento

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** aplicação final com API e IA
- **Conceito principal:** transformar dados externos em uma ideia de produto pequena
- **Produto do encontro:** tema, API, tipo principal e desenho aprovados
- **Organização:** duplas ou trios
- **OpenCode:** explica o JSON e critica o escopo; não edita código
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Explicar API como um serviço que entrega dados.
- Reconhecer arrays, objetos e propriedades em JSON.
- Escolher até quatro campos necessários à interface.
- Definir uma pergunta simples que o projeto responderá.
- Planejar componentes, estados e uma interação principal.

## Opções de projeto

O professor deve oferecer poucas opções já testadas, por exemplo:

- Catálogo de personagens.
- Explorador de criaturas ou monstros de jogos.
- Consulta de países e bandeiras.
- Galeria de imagens espaciais.
- Catálogo de livros.

Cada opção precisa de API sem autenticação, conteúdo apropriado e resposta JSON local de contingência.

## Requisitos do projeto final

- Consumir uma API aprovada.
- Criar um tipo TypeScript para os campos utilizados.
- Exibir carregamento, erro, vazio e sucesso.
- Renderizar dados com `map` e `key` estável.
- Possuir pelo menos três componentes.
- Possuir uma interação principal: busca, filtro ou categoria.
- Usar o OpenCode com plano, aprovação e testes.
- Registrar o prompt principal e a forma de verificação.

## Preparação do professor

- Testar todas as APIs na rede da escola.
- Salvar uma amostra JSON de cada opção.
- Preparar um projeto React com TypeScript vazio para cada grupo.
- Definir limites de requisição e conteúdo.
- Preparar cartões ou uma ficha de planejamento.

## Roteiro de 80 minutos

1. **10 min — Apresentação:** explicar API, pedido, resposta e JSON.
2. **15 min — Escolha:** cada grupo seleciona uma opção aprovada.
3. **15 min — Análise:** marcar array, objetos e até quatro propriedades.
4. **10 min — OpenCode:** pedir explicação do JSON e sugestão de tipo.
5. **20 min — Planejamento:** desenhar a tela, componentes, estados e interação.
6. **10 min — Revisão de escopo:** professor e IA verificam se cabe em cinco aulas.

## Ficha de planejamento

```text
Nome do projeto:
API escolhida:
Pergunta que a aplicação responde:
Campos do JSON usados:
Type principal:
Componentes:
Estados da tela:
Interação principal:
Três testes importantes:
```

## Prompt de análise

```text
Analise somente esta pequena amostra JSON.
Explique array, objeto e propriedades com palavras simples.
Sugira um type TypeScript com no máximo quatro campos úteis para a interface descrita.
Depois aponte um risco de escopo e uma simplificação possível.
Não altere arquivos, não escreva a aplicação e avise quando estiver fazendo uma suposição.
```

## Critérios de aprovação

- A API foi testada pelo professor?
- O projeto possui apenas uma tela?
- Há somente uma interação principal?
- O tipo usa no máximo quatro campos?
- O grupo consegue explicar o que cada campo representa?
- Existe JSON local como plano B?

## Uso de DaisyUI

Durante o planejamento, cada grupo escolhe no máximo quatro componentes visuais: `card` para itens, `select` para categoria, `input` para busca e `badge` para uma propriedade curta. Use `mockup-code` somente para apresentar a amostra JSON, não como parte obrigatória da aplicação.

**Verificação:** o desenho precisa ligar cada componente DaisyUI a uma função concreta. Remova qualquer componente meramente decorativo que aumente o escopo.

## Extensão

Criar, em papel, duas alternativas de organização visual usando os mesmos dados e escolher a mais simples.

## Erros esperados

- Escolher uma API desconhecida durante a aula.
- Querer exibir todos os campos da resposta.
- Planejar login, favoritos persistentes ou várias páginas.
- Aceitar o tipo da IA sem comparar com o JSON.

## Plano B

Se a internet falhar, trabalhar integralmente com as amostras locais. Se o grupo não escolher um tema, usar a opção padrão definida pelo professor.

## Evidência de aprendizagem

Cada grupo entrega a ficha preenchida, o tipo principal revisado e o desenho de uma tela.
