# Aula 3 — Reutilização de componentes e importações

> Aula realizada. Este registro serve para revisão e alinhamento com as aulas seguintes.

## Ficha da aula

- **Duração:** 80 minutos
- **Conceito principal:** composição de componentes
- **Produto do encontro:** página montada com componentes separados
- **Pré-requisito:** JSX básico
- **Interface:** DaisyUI já configurado e conhecido pela turma

## Objetivos

- Separar uma região da página em outro arquivo.
- Entender `export` como oferecer algo e `import` como trazer esse item.
- Reutilizar o mesmo componente mais de uma vez.

## Modelo mental

```text
arquivo que oferece o componente -> export
arquivo que precisa do componente -> import
```

## Preparação do professor

- Manter todos os componentes inicialmente na mesma pasta.
- Usar apenas `export default` nesta etapa.
- Preparar cartões com nomes de arquivos para simular importações fisicamente.

## Roteiro de 80 minutos

1. **10 min — Revisão:** apontar as partes da página criada.
2. **15 min — Extração:** mover o cabeçalho para um componente próprio.
3. **15 min — Importação:** explicar origem, destino e caminho `./`.
4. **30 min — Prática:** separar vídeo e comentário em componentes.
5. **10 min — Fechamento:** remontar verbalmente o caminho de uma importação.

## Desafio essencial

- Criar um arquivo de componente.
- Exportar o componente.
- Importá-lo no arquivo principal.
- Exibi-lo na página.

## Uso de DaisyUI

Use `avatar` no componente de canal e `card` no componente de comentário. Reforce que as classes visuais podem se repetir, enquanto cada componente React continua sendo criado, exportado e importado pelo projeto.

**Verificação:** a dupla deve seguir o percurso `arquivo → export → import → JSX → classe DaisyUI` sem confundir importação React com classe CSS.

## Extensão

Exibir o componente de comentário duas vezes para observar a reutilização.

## Verificação rápida

- O nome do arquivo corresponde ao caminho importado?
- O aluno distingue `export` de `import`?
- O componente aparece no JSX do arquivo principal?

## Erros esperados

- Esquecer `./`.
- Digitar o nome do arquivo com maiúsculas ou minúsculas diferentes.
- Importar o componente sem utilizá-lo.

## Plano de recuperação

Deixar a linha de importação pronta com uma lacuna apenas no nome do arquivo. Repetir o percurso “sai de onde, entra onde”.
