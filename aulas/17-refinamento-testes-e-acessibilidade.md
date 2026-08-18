# Aula 17 — Refinamento, testes e acessibilidade

## Ficha da aula

- **Duração:** 80 minutos
- **Projeto:** aplicação final com API e IA
- **Conceito principal:** melhorar uma versão funcional sem aumentar o escopo
- **Produto do encontro:** versão estável e pronta para demonstração
- **Pré-requisito:** API e interação principal funcionando
- **OpenCode:** revisão limitada; grupo escolhe e testa correções
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Priorizar bugs antes de melhorias visuais.
- Verificar carregamento, erro, vazio e sucesso.
- Testar a interação principal.
- Revisar labels, botões, foco e navegação por teclado.
- Ajustar a interface para uma tela estreita.

## Preparação do professor

- Preparar a rubrica e o checklist de testes.
- Confirmar que todos os grupos possuem uma cópia recuperável.
- Definir um tempo máximo para revisão da IA.
- Disponibilizar uma largura de referência para teste mobile.

## Ordem de prioridade

1. Página abre sem erro fatal.
2. API apresenta os quatro estados.
3. Interação principal funciona.
4. Textos e controles são compreensíveis.
5. Teclado alcança os controles.
6. Interface funciona em tela estreita.
7. Melhorias estéticas opcionais.

## Roteiro de 80 minutos

1. **10 min — Diagnóstico:** executar o checklist e listar problemas.
2. **10 min — Revisão com IA:** pedir análise limitada e priorizada.
3. **30 min — Correções:** aprovar uma mudança por vez e repetir testes.
4. **15 min — Acessibilidade:** revisar labels, botões, foco e teclado.
5. **10 min — Responsividade:** testar tela estreita e corrigir bloqueios.
6. **5 min — Checkpoint:** congelar escopo e preparar a apresentação.

## Prompt de revisão

```text
Revise este projeto React com TypeScript somente nestes critérios:
1. erros que impedem carregamento, erro, vazio ou sucesso;
2. falhas na interação principal;
3. controles sem texto ou label compreensível;
4. problemas que impedem uso por teclado.
Não instale bibliotecas, não troque a API, não crie funcionalidades e não redesenhe a página.
Liste os problemas por prioridade, informe os arquivos e espere aprovação antes de editar.
```

## Checklist de testes

- Carregamento aparece no momento correto.
- Erro oferece uma mensagem compreensível.
- Resposta vazia não parece uma página quebrada.
- Sucesso mostra os campos escolhidos.
- Interação neutra preserva todos os dados.
- Interação com resultado mostra os itens corretos.
- Interação sem resultado oferece orientação.
- Todos os botões funcionam por teclado.
- Campos possuem label visível ou acessível.
- Conteúdo principal cabe em tela estreita.

## Uso de DaisyUI

Faça uma auditoria dos modificadores de estado: `btn-disabled`, `alert-error`, `loading`, `tab-active` e variantes de tamanho. Confirme contraste no tema escolhido, labels reais, foco visível e nomes acessíveis. Componentes prontos não garantem acessibilidade quando usados com HTML inadequado.

Peça ao OpenCode para revisar sem substituir componentes DaisyUI nem alterar o tema. Toda sugestão visual deve estar ligada a um item do checklist.

## Regra de aprovação

Para cada sugestão da IA, o grupo escolhe:

- **Aceitar:** está dentro do escopo e sabemos testar.
- **Adiar:** pode ajudar, mas não é necessária.
- **Recusar:** muda algo fora do pedido ou não conseguimos explicar.

## Extensão

Adicionar uma pequena preferência visual, como alternar entre grade e lista, somente se todo o checklist estiver concluído.

## Erros esperados

- Acrescentar funcionalidades um dia antes da apresentação.
- Aceitar uma grande reorganização para corrigir um detalhe.
- Testar somente com mouse e caso de sucesso.
- Dedicar toda a aula a cores e imagens.

## Plano de recuperação

Se o projeto ainda estiver instável, remover recursos opcionais e manter API, estados e uma interação. Se a API falhar, apresentar com o JSON local e explicar a contingência.

## Evidência de aprendizagem

Cada grupo entrega o checklist marcado e registra uma sugestão aceita, adiada ou recusada com sua justificativa.
