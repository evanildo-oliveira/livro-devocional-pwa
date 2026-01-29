# 📖 Livro Devocional para Crianças - PWA

Versão Progressive Web App (PWA) do Livro Devocional baseado no Catecismo para Crianças Pequenas.

## ✨ Características do PWA

- **📱 Instalável**: Pode ser instalado na tela inicial do celular/tablet/computador
- **🌐 Funciona Offline**: Cache de recursos para uso sem internet
- **🔔 Atualizações Automáticas**: Service Worker gerencia atualizações
- **📲 Splash Screen**: Tela de carregamento ao abrir o app
- **🎨 Ícone Próprio**: Aparece como aplicativo nativo no dispositivo
- **📊 Barra de Status**: Integração com tema do sistema (iOS/Android)

## 📁 Estrutura de Arquivos

```
Livro_Devocional_PWA/
├── index.html              # Página principal (modificada para PWA)
├── manifest.json           # Configuração do PWA
├── service-worker.js       # Cache e funcionalidade offline
├── icons/                  # Ícones do aplicativo
│   ├── icon-base.svg       # SVG base para geração dos ícones
│   ├── icon-72x72.png      # Ícone pequeno
│   ├── icon-96x96.png      # Ícone médio
│   ├── icon-128x128.png    # Chrome Web Store
│   ├── icon-144x144.png    # Ícone grande
│   ├── icon-152x152.png    # iPad
│   ├── icon-192x192.png    # Tela inicial Android/iOS
│   ├── icon-384x384.png    # Alta resolução
│   ├── icon-512x512.png    # Splash screen/Play Store
│   └── README.md           # Instruções para ícones
└── README.md               # Este arquivo
```

## 🚀 Como Usar

### 1. Instalação Local (Teste)

```bash
# Navegue até a pasta
cd Livro_Devocional_PWA

# Inicie um servidor local (requer Python 3)
python -m http.server 8000

# Ou com Node.js
npx serve .

# Ou com PHP
php -S localhost:8000
```

Acesse `http://localhost:8000` no navegador.

### 2. Instalação no Dispositivo

#### Android (Chrome):
1. Abra o site no Chrome
2. Toque no menu (⋮) → "Adicionar à tela inicial"
3. Confirme a instalação

#### iOS (Safari):
1. Abra o site no Safari
2. Toque no botão Compartilhar (□↑)
3. Role e toque em "Adicionar à Tela de Início"

#### Desktop (Chrome/Edge):
1. Abra o site
2. Clique no ícone de instalação na barra de endereço
3. Ou use Menu → "Instalar Livro Devocional..."

## 🧪 Testando o PWA

### Lighthouse (Chrome DevTools)
1. Abra o DevTools (F12)
2. Vá para a aba "Lighthouse"
3. Selecione "Progressive Web App"
4. Clique em "Analyze page load"

### Verificação Offline
1. Abra o aplicativo
2. Desligue a internet
3. Recarregue a página
4. O app deve continuar funcionando!

### Verificação de Instalação
- No Chrome: DevTools → Application → Manifest
- Verifique se todos os ícones estão carregando
- Confira se o Service Worker está registrado

## 📝 O que foi adicionado ao HTML original

### No `<head>`:
```html
<!-- PWA Manifest -->
<link rel="manifest" href="manifest.json">

<!-- iOS Support -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Devocional Kids">
<link rel="apple-touch-icon" href="icons/icon-192x192.png">
```

### No final do `<body>`:
```javascript
// Registro do Service Worker
if ('serviceWorker' in navigator) {
    navigator.serviceWorker.register('service-worker.js')
        .then(registration => console.log('SW registrado'))
        .catch(error => console.error('Erro SW:', error));
}
```

## 🔧 Personalização

### Cores
Edite `manifest.json` para mudar as cores:
- `theme_color`: Cor da barra de endereço/status
- `background_color`: Cor da splash screen

### Ícones
Substitua os arquivos em `icons/` mantendo os mesmos nomes e tamanhos.

### Nome do App
Edite em `manifest.json`:
- `name`: Nome completo
- `short_name`: Nome curto (para tela inicial)

## 📋 Requisitos para Publicação

Para publicar em uma loja de aplicativos (como PWA):

1. **Servidor HTTPS**: O PWA requer conexão segura
2. **Ícones Completos**: Todos os 8 tamanhos de ícones
3. **Screenshots**: Adicione em `screenshots/` para o manifesto
4. **Teste**: Verifique com Lighthouse (pontuação >90)

## 🐛 Solução de Problemas

### Service Worker não registra
- Verifique se está em HTTPS ou localhost
- Limpe o cache do navegador
- Verifique o console por erros

### Ícones não aparecem
- Verifique se todos os arquivos PNG estão em `icons/`
- Confira se os nomes correspondem ao `manifest.json`

### App não instala
- Verifique se o manifesto é válido (DevTools → Application → Manifest)
- Confira se o Service Worker está ativo
- Use o Lighthouse para diagnóstico

## 📚 Recursos Adicionais

- [Web App Manifest](https://developer.mozilla.org/pt-BR/docs/Web/Manifest)
- [Service Workers](https://developer.mozilla.org/pt-BR/docs/Web/API/Service_Worker_API)
- [PWA Checklist](https://web.dev/pwa-checklist/)

---

**Nota**: Este é um aplicativo para fins educacionais e devocionais.
