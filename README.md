# Hisho Web - Estrutura V1.0

Projeto reorganizado a partir do `index(16).html`. O objetivo desta versão é manter as funções atuais e separar o código para facilitar publicação em servidor, manutenção e criação de novas features.

## Como publicar

1. Envie todo o conteúdo desta pasta para o servidor.
2. Configure o servidor para abrir `index.html` como página inicial.
3. Mantenha a estrutura de pastas, pois o HTML referencia arquivos em `assets/css` e `assets/js`.

## Estrutura

```txt
hisho-web-estrutura-v1/
├─ index.html
├─ pages/
│  └─ erro.html
├─ assets/
│  ├─ css/
│  │  ├─ app.css
│  │  └─ modules/
│  ├─ js/
│  │  ├─ core/
│  │  ├─ modules/
│  │  └─ patches/
│  ├─ img/
│  └─ vendor/
├─ config/
│  └─ endpoints.example.js
├─ components/
├─ data/mock/
└─ docs/
   ├─ ARCHITECTURE.md
   └─ js-modules-manifest.json
```

## O que foi feito

- CSS removido do HTML e reunido em `assets/css/app.css`.
- Scripts inline extraídos para arquivos em `assets/js`.
- Ordem original dos scripts preservada para evitar quebrar regras existentes.
- Patches/fixes mantidos em `assets/js/patches`.
- Página de erro criada em `pages/erro.html`.
- Documentação inicial criada em `docs/ARCHITECTURE.md`.
- Pasta de configuração criada para centralizar APIs em futuras refatorações.

## Observação importante

Como o Hisho Web já tinha muitas regras acopladas em um único HTML, esta entrega prioriza uma refatoração segura: organização por arquivos sem remover funcionalidades. A próxima etapa ideal é transformar os módulos globais em serviços menores, começando por APIs, filtros, autenticação, gráficos e renderização da carteira.

## Instalação como aplicativo (PWA)

O Hisho Web agora possui favicon, manifesto, Service Worker, ícones e botão de instalação.

A instalação funciona em HTTPS ou localhost. Abrir o HTML diretamente por `file://` não habilita o Service Worker. Após publicar, abra no Chrome ou Edge e use o botão **Instalar Hisho** no cabeçalho.
