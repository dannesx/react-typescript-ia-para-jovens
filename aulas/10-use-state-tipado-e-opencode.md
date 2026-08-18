# Aula 10 — Estado tipado e início do OpenCode

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** Todo List
- **Conceito principal:** lista tipada dentro do estado
- **Produto do encontro:** tarefas controladas por `useState<Tarefa[]>`
- **Pré-requisito:** tipo `Tarefa`, arrays, `map` e `useState`
- **OpenCode:** primeira utilização, somente para pistas e explicações
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Mover as tarefas iniciais para um estado tipado.
- Reconhecer erros ao inserir uma tarefa incompatível.
- Revisar caminhos simples de importação.
- Aplicar o protocolo PARE ao pedir ajuda à IA.

## Preparação do professor

- Instalar e configurar o OpenCode antes da aula.
- Manter aprovação manual e bloquear instalações desnecessárias.
- Criar uma cópia recuperável do Todo List.
- Preparar quatro erros independentes no projeto.
- Testar o prompt da aula com o modelo disponível.

## Protocolo PARE

1. **Pedir:** fazer uma pergunta pequena e proibir alterações.
2. **Analisar:** comparar a explicação com a IDE.
3. **Rodar:** corrigir manualmente e testar a página.
4. **Explicar:** contar qual era o erro e por que a correção funcionou.

## Exemplo-base

```tsx
const [tarefas, setTarefas] = useState<Tarefa[]>(tarefasIniciais);
```

Leia em voz alta: “O estado `tarefas` guarda uma lista de itens que seguem o tipo `Tarefa`”.

## Roteiro de 80 minutos

1. **10 min — Revisão:** ler `Tarefa[]` e relembrar `useState`.
2. **15 min — Estado tipado:** mover a lista para o estado.
3. **15 min — OpenCode e segurança:** apresentar PARE e as regras da turma.
4. **30 min — Caça aos erros:** corrigir quatro problemas, usando IA somente no último.
5. **10 min — Registro:** anotar pergunta, pista, correção e teste.

## Prompt da aula

```text
Explique o erro do TypeScript destacado neste Todo List como se eu tivesse 13 anos.
Não altere nenhum arquivo e não execute comandos.
Dê primeiro uma pista curta e diga qual tipo o código esperava receber.
```

## Prática essencial

- Criar `useState<Tarefa[]>`.
- Renderizar a lista a partir do estado.
- Corrigir uma tarefa incompatível.
- Corrigir um caminho `./` ou `../` observando a localização dos arquivos.
- Pedir uma pista ao OpenCode e realizar a correção manualmente.

## Uso de DaisyUI

Mantenha `card`, `checkbox` e `badge` das aulas anteriores. Mostre erros ou orientações dentro de `alert alert-warning`, deixando claro que o `alert` apresenta a mensagem, mas o TypeScript e a lógica determinam quando ela existe.

Inclua no prompt ao OpenCode: “Não troque componentes nem classes DaisyUI”. Isso mantém a investigação focada no estado tipado.

## Extensão

Criar intencionalmente uma tarefa sem `concluida`, prever o erro e confirmar a previsão na IDE.

## Verificação rápida

Cada aluno completa: “O TypeScript esperava ___, recebeu ___ e eu corrigi ___”.

## Erros esperados

- Aceitar edição da IA mesmo quando o pedido proíbe mudanças.
- Copiar a explicação sem localizar a linha correspondente.
- Alterar o array diretamente em vez de usar `setTarefas`.

## Plano de recuperação

Se o OpenCode falhar, usar uma captura de resposta preparada. Se a turma estiver insegura, resolver dois erros coletivamente e deixar apenas um para as duplas.

## Evidência de aprendizagem

Registrar em quatro linhas: pedido feito, pista recebida, correção realizada e teste executado.
