# Ícones do PWA

Para completar o PWA, você precisa gerar ícones PNG nos seguintes tamanhos:

## Tamanhos necessários

- `icon-72x72.png` - Para notificações e dispositivos antigos
- `icon-96x96.png` - Para dispositivos de densidade média
- `icon-128x128.png` - Para Chrome Web Store
- `icon-144x144.png` - Para dispositivos de alta densidade
- `icon-152x152.png` - Para iPad
- `icon-192x192.png` - Para tela inicial Android e iOS
- `icon-384x384.png` - Para telas de alta resolução
- `icon-512x512.png` - Para splash screens e Play Store

## Como gerar os ícones

### Opção 1: Usar o arquivo SVG base (recomendado)

1. Use o arquivo `icon-base.svg` nesta pasta
2. Converta para PNG nos tamanhos acima usando ferramentas como:
   - [SVG to PNG](https://svgtopng.com/)
   - [CloudConvert](https://cloudconvert.com/svg-to-png)
   - Inkscape ou Adobe Illustrator

### Opção 2: Usar geradores de ícones PWA

1. Acesse [PWA Asset Generator](https://pwa-asset-generator.nicepkg.cn/)
2. Ou use o [Favicon.io](https://favicon.io/favicon-converter/)
3. Faça upload do SVG e baixe os ícones gerados

### Opção 3: Criar ícones personalizados

Você pode criar ícones personalizados seguindo estas diretrizes:
- Formato: PNG
- Fundo: cor sólida #4CAF50 (verde)
- Ícone central: 📖 (livro) ou ✝️ (cruz) ou ❤️ (coração)
- Bordas arredondadas (opcional mas recomendado)

## Verificação

Após gerar os ícones, verifique se:
1. Todos os 8 arquivos estão na pasta `icons/`
2. Os nomes estão exatamente como listado acima
3. Os tamanhos correspondem aos nomes dos arquivos
4. O formato é PNG (não JPEG ou outros)

## Nota importante

Os ícones são essenciais para:
- A instalação do PWA funcionar corretamente
- O ícone aparecer na tela inicial do dispositivo
- A splash screen ser exibida ao abrir o app
- O app ser reconhecido pelas lojas de aplicativos
