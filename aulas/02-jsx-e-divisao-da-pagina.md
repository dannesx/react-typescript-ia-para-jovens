# Aula 2 — JSX e divisão da página

> Aula realizada. Este registro serve para revisão e alinhamento com as aulas seguintes.

## Ficha da aula

- **Duração:** 80 minutos
- **Conceito principal:** JSX
- **Produto do encontro:** estrutura inicial da página inspirada no YouTube
- **Pré-requisito:** reconhecer um componente
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Reconhecer JSX como a forma de descrever a interface dentro do JavaScript.
- Aplicar regras básicas de fechamento de tags e agrupamento de elementos.
- Dividir visualmente a página em regiões menores.

## Preparação do professor

- Disponibilizar uma captura simples de uma página de vídeo.
- Marcar na imagem cabeçalho, vídeo, informações e comentários.
- Manter o CSS inicial pronto para evitar que estilo seja o assunto principal.

## Roteiro de 80 minutos

1. **10 min — Revisão:** localizar o componente criado na aula 1.
2. **15 min — JSX:** comparar um pequeno trecho HTML com JSX.
3. **15 min — Leitura visual:** desenhar caixas sobre as regiões da página.
4. **30 min — Prática guiada:** montar a estrutura com elementos semânticos simples.
5. **10 min — Fechamento:** identificar qual trecho gera cada região da tela.

## Desafio essencial

Montar uma página contendo:

- Cabeçalho.
- Área do vídeo.
- Título e informações do vídeo.
- Área reservada aos comentários.

## Uso de DaisyUI

Construa a região superior com `navbar`, a área principal com `card` e as separações com `divider`. Use as classes para tornar visível a divisão da página, mas peça que os alunos identifiquem primeiro os elementos JSX e suas relações de abertura e fechamento.

**Verificação:** remover temporariamente `card` deve alterar o visual, mas não a estrutura semântica do conteúdo.

## Extensão

Adicionar uma descrição curta abaixo do título do vídeo.

## Verificação rápida

- O JSX possui um elemento principal?
- Todas as tags foram fechadas?
- O aluno associa cada região visual a um trecho do JSX?

## Erros esperados

- Usar `class` em vez de `className`.
- Retornar elementos irmãos sem agrupá-los.
- Fechar tags na ordem errada.

## Plano de recuperação

Oferecer a estrutura com quatro regiões vazias e pedir que o aluno apenas adicione os textos correspondentes.
