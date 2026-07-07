# Contratos de Locação Residencial (Goiânia/Trindade – GO)

Site estático, sem servidor: tudo roda no navegador de quem abrir o link.
Agora funciona como um pequeno "app":

- **Lista de contratos**: cada contrato preenchido fica salvo no navegador (usando IndexedDB).
- **Editar**: reabra qualquer contrato salvo e altere os dados.
- **Gerar PDF**: gera o PDF do contrato a qualquer momento a partir dos dados salvos.
- **Anexar assinado**: depois de assinado (digitalizado ou assinatura digital via GOV.BR), anexe o arquivo (PDF ou imagem) ao contrato correspondente — ele fica guardado junto com o registro e pode ser baixado depois.
- **Backup**: botão para exportar todos os contratos em um `.json` (não inclui os arquivos assinados anexados) e reimportar depois, útil se quiser levar os dados para outro navegador/computador.

## Importante sobre onde os dados ficam salvos

Este é um site 100% estático — **não existe um servidor guardando os dados**.
Tudo (contratos, arquivos assinados anexados) fica salvo **apenas no navegador
do computador/celular usado para preencher**, através do IndexedDB do navegador.

Isso significa:
- Se sua mãe preencher no Chrome do computador dela, os contratos ficam só ali.
- Limpar o histórico/dados de navegação do navegador pode apagar os contratos salvos.
- Para ver os mesmos contratos em outro navegador ou dispositivo, use o botão
  **"Exportar backup"** em um dispositivo e **"Importar backup"** no outro
  (isso não leva os arquivos assinados anexados, só os dados do formulário).

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (pode ser privado ou público).
2. Suba o arquivo `index.html` (e este `README.md`, se quiser) para a raiz do repositório.
3. Vá em **Settings → Pages**.
4. Em "Source", selecione a branch `main` e a pasta `/ (root)`. Salve.
5. Em alguns minutos o GitHub mostrará o link do site, algo como:
   `https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO/`
6. Envie esse link para sua mãe preencher o formulário e gerar o PDF.

## Como testar antes de publicar

Basta abrir o arquivo `index.html` diretamente no navegador (duplo clique).
É necessário estar conectado à internet apenas porque o site usa uma
biblioteca (html2pdf.js) carregada de um CDN para montar o PDF.

## Observações jurídicas

- O modelo de contrato segue a Lei do Inquilinato (Lei nº 8.245/1991) e inclui cláusulas específicas para Goiânia/Trindade (GO), como a transferência de titularidade das contas de água (SANEAGO) e energia (Equatorial Goiás).
- A opção "Não se aplica" em Garantia Locatícia insere uma cláusula dispensando expressamente a exigência de garantia.
- Este é um modelo de referência. Recomenda-se revisão por um advogado antes da assinatura definitiva.
