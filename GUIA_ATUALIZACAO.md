# Guia rapido de atualizacao

Este projeto usa arquivos HTML simples. A pagina principal e `index.html`.

## Para adicionar uma nova publicacao semanal

1. Crie ou copie o novo arquivo HTML para `C:\Vem_e_Segue`.
   Exemplo: `pagina-vem-e-segue-me-2026-05-25.html`.

2. Abra `index.html` e procure por:

   `ATUALIZACAO RAPIDA`

3. Copie um bloco:

   `<article class="publication-item"> ... </article>`

4. Cole abaixo da ultima publicacao e altere:

   - dia e mes;
   - titulo;
   - resumo;
   - nome do arquivo no link `href`.

5. Na guia lateral, dentro de:

   `<div class="guide-links">`

   adicione mais um link no formato:

   `<a href="NOME-DO-ARQUIVO.html">data - titulo curto</a>`

6. Copie a pagina principal para a copia descritiva:

   `Copy-Item .\index.html .\onde-cristo-habita-index.html -Force`

7. Atualize o repositorio:

   ```powershell
   git add .
   git commit -m "adiciona publicacao semanal"
   git push
   ```

## Arquivos principais

- `index.html`: pagina inicial publicada.
- `onde-cristo-habita-index.html`: copia da pagina inicial.
- `pagina-vem-e-segue-me-2026-*.html`: publicacoes semanais.
