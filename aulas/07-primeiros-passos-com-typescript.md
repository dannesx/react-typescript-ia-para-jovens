# Aula 7 — Novo projeto e primeiros passos com TypeScript

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** tipos básicos como pistas oferecidas pela IDE
- **Produto do encontro:** primeira tela estática do Todo List em um projeto TypeScript
- **Pré-requisito:** componentes, importações, props, estado, eventos e `map`
- **OpenCode:** ainda não será usado
- **Interface:** DaisyUI já configurado e conhecido pela turma
- **Organização sugerida:** duplas, com troca de piloto na metade da prática

## Ideia central

Esta aula começa um projeto completamente novo. O Todo List fornece um contexto simples e familiar para apresentar TypeScript sem transformar o encontro em uma aula abstrata sobre linguagem.

O objetivo não é decorar sintaxe nem configurar TypeScript. O objetivo é perceber que cada informação possui um formato e que a IDE consegue avisar quando o código recebe algo diferente do esperado.

## O que entra e o que não entra nesta aula

### Entra

- Arquivos `.tsx`.
- `string`, `number` e `boolean`.
- Anotações simples de tipo.
- Inferência apresentada brevemente.
- Leitura de mensagens da IDE.
- Criação e importação de um componente estático.
- Estrutura visual inicial do Todo List.

### Fica para depois

- Props tipadas: aula 8.
- Objetos, arrays e tipo `Tarefa`: aula 9.
- `useState<Tarefa[]>`: aula 10.
- Formulário funcional: aula 11.
- Concluir, excluir e filtrar tarefas: aulas 12 e 13.
- OpenCode: a partir da aula 10.

## Objetivos de aprendizagem

Ao final da aula, o aluno deve conseguir:

1. Explicar que TypeScript verifica se os dados possuem o formato esperado.
2. Reconhecer exemplos de `string`, `number` e `boolean`.
3. Localizar arquivo, linha e trecho destacados pela IDE.
4. Traduzir uma mensagem simples de incompatibilidade de tipos.
5. Corrigir um erro alterando apenas o valor incompatível.
6. Criar, exportar e importar um componente estático no novo projeto.

## Critérios de sucesso

A aula atingiu o resultado esperado quando a maioria da turma consegue:

- Abrir o novo projeto sem depender dos arquivos do projeto anterior.
- Exibir a tela inicial do Todo List.
- Classificar corretamente pelo menos cinco de seis valores.
- Corrigir pelo menos um erro de tipo preparado pelo professor.
- Explicar a correção usando a frase “esperava, recebeu, corrigi”.

## Resultado visual esperado

A tela final deve apresentar:

- Cabeçalho com o nome “Minhas tarefas”.
- Frase curta explicando a aplicação.
- Campo e botão ainda sem comportamento.
- Área informando quantas tarefas existem.
- Mensagem indicando se há pendências.
- Espaço visual reservado à futura lista.

Não é necessário adicionar tarefas nesta aula.

---

## Preparação do professor

### Projeto-base

Antes da aula:

- Criar um projeto React com TypeScript.
- Confirmar que o servidor inicia sem erros.
- Remover conteúdo de demonstração desnecessário.
- Manter apenas `App.tsx`, `App.css`, `main.tsx` e os arquivos básicos da ferramenta utilizada.
- Criar a pasta `src/components`.
- Instalar e configurar Tailwind CSS e DaisyUI antes de entregar o projeto.
- Escolher um único tema DaisyUI para toda a turma.
- Preparar uma cópia limpa para recuperação.
- Abrir o projeto uma vez em cada computador da sala.

Os alunos não precisam criar ou configurar o projeto. Problemas de instalação desviariam o foco pedagógico dos tipos e das mensagens da IDE.

### Organização da IDE

- Deixar explorador de arquivos, editor e painel de problemas visíveis.
- Aumentar o tamanho da fonte.
- Confirmar que os erros do TypeScript aparecem sublinhados.
- Projetar IDE e navegador lado a lado.
- Fechar extensões ou painéis que gerem distração.

### Materiais

- Uma captura ou desenho simples do Todo List esperado.
- Cartões físicos ou digitais com valores para classificação.
- Três versões de erro preparadas.
- Arquivo final funcional para recuperação.
- Cronômetro visível.

### Cartões para a dinâmica

Prepare estes valores:

| Valor | Tipo esperado |
| --- | --- |
| `"Fazer atividade de matemática"` | `string` |
| `4` | `number` |
| `false` | `boolean` |
| `"4"` | `string` |
| `true` | `boolean` |
| `"false"` | `string` |

Os dois últimos pares ajudam a mostrar que aspas mudam o tipo do valor.

---

## Vocabulário da aula

| Palavra | Explicação para a turma | Exemplo |
| --- | --- | --- |
| Tipo | Formato esperado para uma informação | texto, número ou verdadeiro/falso |
| `string` | Texto escrito entre aspas | `"Estudar React"` |
| `number` | Número sem aspas | `3` |
| `boolean` | Valor que só pode ser verdadeiro ou falso | `true` |
| Erro de tipo | Valor diferente do formato esperado | guardar `"três"` onde era esperado um número |
| IDE | Aplicativo em que escrevemos e investigamos o código | VS Code |
| `.tsx` | Arquivo TypeScript que também pode conter JSX | `App.tsx` |
| Inferência | Quando o TypeScript descobre o tipo pelo próprio valor | entender que `3` é um número |

## Frase-chave

> TypeScript é um revisor que observa os formatos dos dados antes de a página ser usada.

Evite dizer que TypeScript “impede todos os bugs”. Ele encontra muitos erros de formato, mas não garante que toda a lógica esteja correta.

---

## Roteiro detalhado de 80 minutos

### 0–8 min — Apresentação do novo desafio

Mostre a referência visual do Todo List e pergunte:

- Para que serve uma lista de tarefas?
- Que informações aparecem em uma tarefa?
- O que pode mudar enquanto usamos essa aplicação?

Registre respostas como título, quantidade e situação de conclusão. Não transforme as respostas em código ainda.

**Fala sugerida:**

> Hoje começamos uma aplicação nova. Ela será construída durante várias aulas. Nesta primeira etapa, vamos montar a tela e conhecer uma ferramenta que avisa quando colocamos uma informação no formato errado.

### 8–18 min — Planejamento visual

Desenhe quatro regiões:

1. Cabeçalho.
2. Formulário.
3. Resumo.
4. Lista.

Explique que apenas o cabeçalho e a estrutura estática serão implementados hoje. O formulário ainda não adicionará tarefas.

Peça que cada dupla desenhe a tela em uma folha durante três minutos. O desenho deve conter somente as quatro regiões.

### 18–30 min — Tipos do cotidiano

Apresente os seis cartões, um por vez. Os alunos levantam uma indicação de texto, número ou verdadeiro/falso.

Depois de cada escolha, pergunte:

- Há aspas?
- O valor representa uma contagem ou um texto?
- Ele só pode ter duas respostas?

Destaque especialmente:

```ts
const quantidadeComoNumero: number = 4;
const quantidadeComoTexto: string = "4";
```

Os valores parecem parecidos para uma pessoa, mas possuem tipos diferentes para o código.

### 30–40 min — Primeira leitura da IDE

Digite coletivamente:

```ts
const nomeDaLista: string = "Minhas tarefas";
const quantidade: number = 0;
const possuiPendencias: boolean = false;
```

Explique cada linha:

- `const`: cria um nome para guardar um valor.
- `nomeDaLista`: nome escolhido para a informação.
- `: string`: formato esperado.
- `=`: recebe o valor.
- `"Minhas tarefas"`: valor guardado.

Em seguida, crie este erro intencional:

```ts
const quantidade: number = "zero";
```

Use sempre a sequência:

1. Localizar o sublinhado.
2. Passar o mouse sobre o erro.
3. Ler somente a primeira mensagem útil.
4. Identificar o tipo esperado.
5. Identificar o tipo recebido.
6. Corrigir uma linha.
7. Confirmar que o aviso desapareceu.

**Tradução sugerida:**

> O código esperava um número, mas recebeu um texto.

### 40–58 min — Prática guiada: componente de cabeçalho

Crie `src/components/CabecalhoLista.tsx` com a turma. Reforce exportação e importação, pois esse é um ponto de dificuldade já observado.

Depois, altere `App.tsx` para usar o novo componente e declarar os três valores tipados.

Faça pausas depois de:

1. Criar o arquivo.
2. Exportar o componente.
3. Digitar o caminho do import.
4. Exibir o componente.
5. Salvar e verificar o navegador.

### 58–68 min — Troca de piloto e personalização

Troque quem está digitando em cada dupla.

O novo piloto deve:

- Alterar `nomeDaLista`.
- Alterar `quantidade` para outro número.
- Alterar `possuiPendencias` para `true`.
- Confirmar as mudanças na página.

Não adicionar novas funcionalidades.

### 68–76 min — Caça aos três erros

Entregue ou projete um erro por vez. A dupla só recebe o próximo depois de explicar o anterior.

Para cada erro, preencher:

```text
Esperava:
Recebeu:
Correção:
```

### 76–80 min — Bilhete de saída

Cada aluno responde individualmente:

1. Qual é o tipo de `"5"`?
2. Qual é o tipo de `5`?
3. O que você observa primeiro quando a IDE sublinha um erro?
4. Complete: “O TypeScript esperava ___, recebeu ___ e eu corrigi ___”.

Recolha as respostas para decidir quanto revisar no início da aula 8.

---

## Implementação completa da aula

### `src/components/CabecalhoLista.tsx`

```tsx
export default function CabecalhoLista() {
  return (
    <header className="cabecalho-lista">
      <span className="badge badge-outline cabecalho-lista__marcador">
        ORGANIZAÇÃO
      </span>
      <h1>Meu Todo List</h1>
      <p>Um lugar simples para acompanhar o que preciso fazer.</p>
    </header>
  );
}
```

### `src/App.tsx`

```tsx
import "./App.css";
import CabecalhoLista from "./components/CabecalhoLista";

export default function App() {
  const nomeDaLista: string = "Minhas tarefas";
  const quantidade: number = 0;
  const possuiPendencias: boolean = false;

  return (
    <main className="aplicacao min-h-screen bg-base-200 text-base-content">
      <CabecalhoLista />

      <section
        className="painel card border border-base-300 bg-base-100 shadow-xl"
        aria-labelledby="titulo-lista"
      >
        <div className="painel__titulo">
          <div>
            <span>LISTA ATUAL</span>
            <h2 id="titulo-lista">{nomeDaLista}</h2>
          </div>
          <strong className="badge badge-primary">{quantidade} tarefas</strong>
        </div>

        <form className="formulario-tarefa">
          <fieldset className="fieldset">
            <label className="label font-bold" htmlFor="nova-tarefa">
              Nova tarefa
            </label>
            <div className="formulario-tarefa__linha">
            <input
              id="nova-tarefa"
              name="nova-tarefa"
              placeholder="Ex.: revisar a matéria"
              type="text"
              className="input w-full"
            />
            <button className="btn btn-primary" type="button">
              Adicionar
            </button>
            </div>
          </fieldset>
        </form>

        <section className="resumo stats shadow" aria-label="Resumo das tarefas">
          <div className="stat">
            <div className="stat-title">Tarefas cadastradas</div>
            <div className="stat-value text-primary">{quantidade}</div>
          </div>
          <div className="stat">
            <div className="stat-title">Situação</div>
            <div className="stat-desc text-base-content">
              {possuiPendencias ? "Existem pendências" : "Nenhuma pendência"}
            </div>
          </div>
        </section>

        <section
          className="lista-vazia alert alert-info"
          aria-label="Lista de tarefas"
        >
          <span>✓</span>
          <h3>A lista começará aqui</h3>
          <p>Na próxima etapa, cada tarefa terá seu próprio componente.</p>
        </section>
      </section>
    </main>
  );
}
```

O botão utiliza `type="button"` porque o formulário ainda não terá comportamento. O envio será implementado somente na aula 11.

### `src/App.css`

```css
@import "tailwindcss";
@plugin "daisyui";

:root {
  color: #20231f;
  background: #f2f0e9;
  font-family: Inter, system-ui, sans-serif;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
}

* {
  box-sizing: border-box;
}

body {
  min-width: 320px;
  min-height: 100vh;
  margin: 0;
}

button,
input {
  font: inherit;
}

button {
  cursor: pointer;
}

.aplicacao {
  width: min(100% - 32px, 760px);
  margin: 0 auto;
  padding: 56px 0;
}

.cabecalho-lista {
  margin-bottom: 32px;
}

.cabecalho-lista__marcador,
.painel__titulo span {
  color: #596156;
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 0.12em;
}

.cabecalho-lista h1 {
  margin: 8px 0;
  font-size: clamp(2rem, 7vw, 4.5rem);
  letter-spacing: -0.06em;
  line-height: 0.95;
}

.cabecalho-lista p {
  max-width: 520px;
  margin: 0;
  color: #596156;
  line-height: 1.6;
}

.painel {
  padding: 24px;
  border: 1px solid #c9c9bf;
  border-radius: 20px;
  background: #fffef9;
}

.painel__titulo {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 16px;
}

.painel__titulo h2 {
  margin: 4px 0 0;
  font-size: 1.5rem;
}

.painel__titulo strong {
  padding: 8px 12px;
  border-radius: 999px;
  background: #e4eadf;
  font-size: 0.875rem;
}

.formulario-tarefa {
  margin-top: 28px;
}

.formulario-tarefa label {
  display: block;
  margin-bottom: 8px;
  font-weight: 700;
}

.formulario-tarefa__linha {
  display: flex;
  gap: 8px;
}

.formulario-tarefa input {
  min-width: 0;
  flex: 1;
  padding: 12px 14px;
  border: 1px solid #a8ada5;
  border-radius: 10px;
  background: #fff;
}

.formulario-tarefa input:focus-visible,
.formulario-tarefa button:focus-visible {
  outline: 3px solid #f3b83f;
  outline-offset: 2px;
}

.formulario-tarefa button {
  padding: 12px 18px;
  border: 0;
  border-radius: 10px;
  color: #fff;
  background: #2f5135;
  font-weight: 700;
}

.resumo {
  display: flex;
  justify-content: space-between;
  gap: 16px;
  margin: 24px 0;
  padding: 12px 0;
  border-top: 1px solid #deded5;
  border-bottom: 1px solid #deded5;
  color: #596156;
}

.resumo p {
  margin: 0;
}

.lista-vazia {
  padding: 36px 16px;
  text-align: center;
}

.lista-vazia span {
  display: inline-grid;
  width: 44px;
  height: 44px;
  place-items: center;
  border-radius: 50%;
  color: #2f5135;
  background: #e4eadf;
  font-weight: 800;
}

.lista-vazia h3 {
  margin: 14px 0 6px;
}

.lista-vazia p {
  margin: 0;
  color: #6b7168;
}

@media (max-width: 560px) {
  .aplicacao {
    width: min(100% - 24px, 760px);
    padding: 32px 0;
  }

  .painel {
    padding: 18px;
  }

  .painel__titulo,
  .formulario-tarefa__linha,
  .resumo {
    flex-direction: column;
  }

  .formulario-tarefa button {
    width: 100%;
  }
}
```

Tailwind CSS e DaisyUI devem chegar instalados. O CSS complementar pode ser entregue pronto: ele organiza o layout, enquanto classes como `card`, `badge`, `input`, `btn`, `stats` e `alert` comunicam os componentes visuais. A aula não deve virar um encontro de configuração ou estilização.

## Uso de DaisyUI na aula

Peça que os alunos identifiquem cada classe pelo papel que desempenha:

| Classe | Papel na interface |
| --- | --- |
| `card` | Agrupa o painel principal |
| `badge` | Destaca marcador e quantidade |
| `input` | Apresenta o campo de tarefa |
| `btn btn-primary` | Apresenta a ação principal |
| `stats` | Agrupa o resumo |
| `alert alert-info` | Comunica que a lista ainda está vazia |

Trocar uma classe visual não deve mudar `string`, `number` ou `boolean`. Essa comparação ajuda a separar responsabilidades: TypeScript verifica dados; DaisyUI oferece a base visual.

---

## Caça aos erros preparada

Apresente um erro por vez. Não coloque os três simultaneamente no projeto.

### Erro 1 — número recebido onde era esperado texto

```ts
const nomeDaLista: string = 7;
```

**Leitura esperada:**

- Esperava: `string`.
- Recebeu: `number`.
- Correção possível: `const nomeDaLista: string = "Minhas tarefas";`.

### Erro 2 — texto recebido onde era esperado número

```ts
const quantidade: number = "3";
```

**Leitura esperada:**

- Esperava: `number`.
- Recebeu: `string`.
- Correção possível: remover as aspas.

### Erro 3 — texto recebido onde era esperado booleano

```ts
const possuiPendencias: boolean = "sim";
```

**Leitura esperada:**

- Esperava: `boolean`.
- Recebeu: `string`.
- Correção possível: usar `true` ou `false` sem aspas.

## Ordem de ajuda do professor

Quando um aluno pedir a solução, responda em camadas:

1. “Qual linha está sublinhada?”
2. “Qual tipo aparece depois de ‘esperava’?”
3. “O valor possui aspas?”
4. “Qual dos três tipos estudados combina com esse valor?”
5. Mostre a correção somente se as pistas não forem suficientes.

Essa ordem ajuda o aluno a aprender um método de investigação em vez de esperar a resposta pronta.

---

## Inferência sem complicação

Depois que os exemplos explícitos funcionarem, mostre rapidamente:

```ts
const quantidade = 0;
```

Explique:

> Mesmo sem escrever `: number`, o TypeScript percebe que zero é um número. Isso se chama inferência. Hoje escrevemos os tipos para enxergar o contrato; em outros momentos, a própria ferramenta poderá descobri-los.

Não peça que os alunos removam todas as anotações. O objetivo é apenas evitar a ideia de que TypeScript exige escrever o tipo de toda variável.

---

## Prática individual essencial

Depois da prática guiada, cada aluno deve realizar estas quatro ações:

1. Alterar o nome da lista para um texto próprio.
2. Colocar uma quantidade numérica diferente de zero.
3. Escolher `true` ou `false` para pendências.
4. Criar e corrigir um erro de tipo intencional.

O aluno conclui a prática quando a página abre e a IDE não apresenta erro de tipo nos três valores.

## Extensão para quem terminar cedo

Criar `src/components/RodapeLista.tsx`:

```tsx
export default function RodapeLista() {
  return (
    <footer>
      <p>Projeto Todo List — Aula 7</p>
    </footer>
  );
}
```

Depois:

- Exportar o componente.
- Importá-lo em `App.tsx`.
- Exibi-lo depois do painel.
- Explicar o caminho utilizado no import.

Não adicionar props ao rodapé; esse conteúdo pertence à aula 8.

---

## Avaliação formativa

### Checklist durante a aula

| Habilidade observada | Ainda precisa de ajuda | Conseguiu com pista | Conseguiu sozinho |
| --- | --- | --- | --- |
| Localiza o arquivo indicado |  |  |  |
| Diferencia valor com e sem aspas |  |  |  |
| Reconhece `string`, `number` e `boolean` |  |  |  |
| Lê a primeira mensagem do erro |  |  |  |
| Corrige somente a linha necessária |  |  |  |
| Cria, exporta e importa um componente |  |  |  |

### Respostas esperadas do bilhete de saída

1. `"5"` é `string` porque possui aspas.
2. `5` é `number` porque é um número sem aspas.
3. Resposta esperada: arquivo, linha, sublinhado ou primeira mensagem do erro.
4. A frase deve identificar corretamente o tipo esperado, o recebido e a alteração realizada.

## Decisão para a aula 8

- Se pelo menos 70% acertarem as duas primeiras perguntas e explicarem uma correção, avance para props tipadas.
- Se a turma confundir valores com aspas, reserve 10 minutos da aula 8 para nova classificação.
- Se a maior dificuldade for importação, comece a aula 8 recriando o percurso `arquivo → export → import → JSX`.
- Se muitos alunos não abrirem o projeto, resolva primeiro a infraestrutura e preserve o conteúdo pedagógico.

---

## Erros esperados e intervenções

| Situação | Intervenção sugerida |
| --- | --- |
| Aluno chama `"3"` de número | Perguntar se as aspas fazem parte do valor |
| Aluno altera várias linhas | Restaurar a cópia e corrigir um erro por vez |
| Componente não aparece | Seguir arquivo, export, import e uso no JSX |
| Import está vermelho | Comparar pasta atual, destino, `./` e `../` |
| Aluno lê toda a mensagem e se perde | Cobrir o restante e ler apenas a primeira frase |
| Página abre, mas IDE mostra erro | Explicar que o navegador abrir não torna o contrato correto |
| IDE não mostra erros | Reiniciar o servidor TypeScript ou usar a captura preparada |

## Plano de recuperação

Se a turma avançar mais devagar:

1. Entregue `CabecalhoLista.tsx` pronto.
2. Faça a importação coletivamente.
3. Trabalhe apenas `nomeDaLista` e `quantidade`.
4. Introduza `boolean` no fechamento.
5. Realize somente um erro intencional.

O mínimo inegociável é que cada aluno relacione valor, tipo e mensagem da IDE.

## Plano para turma avançada

Se a turma concluir cedo:

1. Criar o rodapé como segundo componente.
2. Comparar anotação explícita e inferência.
3. Criar três erros intencionais para outra dupla investigar.
4. Registrar as mensagens em linguagem técnica e em linguagem comum.

Não antecipar props tipadas, arrays ou estado tipado. A extensão deve aprofundar a investigação, não aumentar o número de conceitos.

## Tarefa opcional

Encontrar em casa três informações de um aplicativo e classificá-las como `string`, `number` ou `boolean`.

Exemplo de formato:

| Informação | Valor de exemplo | Tipo |
| --- | --- | --- |
| Nome do usuário | `"Ana"` | `string` |
| Quantidade de mensagens | `8` | `number` |
| Notificação ativada | `true` | `boolean` |

Não solicitar dados pessoais reais. Os exemplos devem ser inventados.

## Evidências produzidas

Ao final da aula, cada aluno ou dupla terá:

- Projeto Todo List abrindo no navegador.
- `CabecalhoLista.tsx` criado e importado.
- Três valores tipados em `App.tsx`.
- Pelo menos um erro corrigido com ajuda da IDE.
- Bilhete de saída preenchido.
- Registro “esperava, recebeu, corrigi”.
