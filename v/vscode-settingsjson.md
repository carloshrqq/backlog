---
created: 2025-02-10 06:51
tags:
  - "#new"
  - "#new/tags"
  - "#new/pkm"
  - "#review"
---

# Localização do arquivo de configuração

De acordo com a documentação
`%APPDATA%\Code\User\settings.json`

Localização
`C:\Users\USER\AppData\Roaming\Code\User`


https://gist.github.com/carlos7z/8729842e65dcda6974392ddbde0e3389
# Tutorial completo APC UI++ e VSCode Version Control

Nome do pinned gist: VSCode settings.json (Uptaded feb. 12th)
	Nome do subpin: LEIA-ME (extensão APC UI e versão do VSCode )
	Nome do subpin: README (APC UI extension and VSCode version)
	Nome do subpin: enabled-extensions 


LEIA-ME

(Atualizado em 12 de Fevereiro de 2025)

A partir da versão 1.94 o plugin APC Customize UI++ quebrou e até a data atual não há conserto.

Para evitar o problema é necessário instalar a versão 1.93.

Seguir o passo a passo sem pular nenhuma etapa:

1. [Download](https://update.code.visualstudio.com/1.93.1/win32-x64-user/stable) (win) da [versão 1.93](https://code.visualstudio.com/updates/v1_93)

2. **IMPORTANTE**: Ao **ABRIR A PRIMEIRA VEZ** configure o seguinte:

	Arquivo > Preferências > Configurações > Aplicação > *Update*
	
	**DESMARQUE A OPÇÃO**: [ ] Habilitar update em segundo plano  
	
	**MODO**: Escolha a opção NENHUM.

3. Para conferir a versão feche o obsidian e acesse o endereço do executável code.exe em

%USERPROFILE%\AppData\Roaming\VSCode.exe

ou no diretório em que escolheu durante a instalação.

Clique com o botão direito sobre o arquivo > Propriedades > Detalhes >

Em versão do arquivo deve constar 1.93.1.0.
# Desabilitar update do vscode

ATENÇÃO: Assim que o VSCode abrir desabilite o "update em segundo plano" e o modo de atualização "nenhum".

Se este passo não for realizado o apc não irá funcionar (próximo passo)

**Em detalhes deve constar 1.93.1**

"File > Preferences > Settings > Application > Update"
**uncheck** Enable windows background updates
Mode **none** ou **manual**
# Versão com a extensão APC Customize AI estável
**Em detalhes do aquivo code.exe deve constar 1.93.1**

Versão 1.93
https://code.visualstudio.com/updates/v1_93

Consultar [[vscode-plugins|plugins do vscode]]


# Versão atual estendida e adaptada (diego 3g)

[VSCode Settings (Updated)](https://gist.github.com/diego3g/b1b189063d21b96d6144ca896755be64)

**Em detalhes deve constar 1.93.1 na versão do vscode**


```json
/*
[ptBR]

LEIA-ME

(Atualizado em 10 de Fevereiro de 2025)

A partir da versão 1.94 o plugin APC Customize UI++ quebrou e até a data atual

não há conserto.

Para evitar o problema é necessário instalar a versão 1.93.

Seguir o passo a passo sem pular nenhuma etapa:

4. Link para download da versão 1.93

https://code.visualstudio.com/updates/v1_93

5. IMPORTANTE: Ao ABRIR A PRIMEIRA VEZ configure o seguinte:

Arquivo > Preferências > Configurações > Aplicação > Update 

DESMARQUE A OPÇÃO: [ ] Habilitar update em segundo plano

MODO: Escolha a opção NENHUM.

Para conferir feche o obsidian e acesse o endereço do executável code.exe em

%USERPROFILE%\AppData\Roaming\VSCode.exe

ou no diretório em que escolheu durante a instalação.

Clique com o botão direito sobre o arquivo > Propriedades > Detalhes >

Em versão do arquivo deve constar 1.93.1.0

********************************************************************************
[engUS]

README

(Last update February 10th, 2025)

Starting with version 1.94, the APC Customize UI++ plugin broke and there is no

fix until this day.

To avoid the problem, you need to install version 1.93.

Follow the step-by-step instructions without skipping any steps:

6. Download link for version 1.93

https://code.visualstudio.com/updates/v1_93

7. IMPORTANT: When OPENING FOR THE FIRST TIME, configure the following:

File > Preferences > Settings > Application > Update

UNCHECK THE OPTION: [ ] Enable background updates

MODE: Choose the NONE option.

To check, close Obsidian and access the code.exe executable address in

%USERPROFILE%\AppData\Roaming\VSCode.exe

or another custom directory of your choice during install


Right-click on the file > Properties > Details >

The file version should be 1.93.1.0

********************************************************************************
VSCode plugins in that config (some plugins maybe repeated or double marked)

Apc Customize UI++
Auto close Tag
Auto Rename Tag
Laravel Artisan (out of settings/personal use)
Laravel Blade Formatter (out of settings/personal use)
Laravel Extra Intellisense (out of settings/personal use)
C/C++
C/C++ Extension Pack
C/C++ Themes
CMake
CMake Tools
Code Spell Checker
Composer
Console Ninja
fish
GitLens - Git supercharged
ESLint
Fluent Icons
Intelli PHP
Min Theme
PHP
PHP Profiler
poimandres
Prettier - Code Formatter
Prettier ESLint
Prettier SQL VSCode
Prisma
Tailwind CSS IntelliSense
*/

{
  "workbench.startupEditor": "newUntitledFile",
  "editor.fontSize": 20,
  "editor.lineHeight": 1.8,
  "javascript.suggest.autoImports": true,
  "javascript.updateImportsOnFileMove.enabled": "always",
  "editor.rulers": [
    80,
    120
  ],
  "extensions.ignoreRecommendations": true,
  "typescript.tsserver.log": "off",
  "editor.stickyScroll.enabled": false,
  "workbench.tree.enableStickyScroll": false,
  "files.associations": {
    ".env.*": "dotenv",
    ".prettierrc": "json",
    "*.css": "css",
    ".dev.vars": "dotenv"
  },
  "symbols.files.associations": {
    "*.module.ts": "nest",
    "*.guard.ts": "typescript",
    "*.spec.ts": "ts-test",
    "*.e2e-spec.ts": "ts-test",
    "*.mock.ts": "ts-test",
    "vitest.config.e2e.ts": "vite",
    ".env.development.local": "gear",
    ".env.test.local": "gear",
    ".env.local": "gear",
    ".env.example": "gear"
  },
  "tailwindCSS.experimental.classRegex": [
    [
      "tv\\(([^)]*)\\)",
      "[\"'`]([^\"'`]*).*?[\"'`]"
    ],
    "class:\\s*?[\"'`]([^\"'`]*).*?,"
  ],
  "editor.parameterHints.enabled": false,
  "editor.renderLineHighlight": "gutter",
  "cSpell.language": "en,pt",
  "typescript.updateImportsOnFileMove.enabled": "always",
  "editor.suggestSelection": "first",
  "explorer.confirmDelete": false,
  "gitlens.codeLens.recentChange.enabled": false,
  "terminal.integrated.showExitAlert": false,
  "[prisma]": {
    "editor.formatOnSave": true,
    "editor.formatOnPaste": true,
    "files.autoSave": "afterDelay",
    "files.autoSaveDelay": 1000
  },
  "typescript.suggest.autoImports": true,
  "typescript.preferences.preferTypeOnlyAutoImports": true,
  "terminal.integrated.env.osx": {
    "FIG_NEW_SESSION": "1"
  },
  "workbench.editor.labelFormat": "short",
  "workbench.sideBar.location": "right",
  "editor.fontLigatures": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "mdx": "javascriptreact"
  },
  "emmet.syntaxProfiles": {
    "javascript": "jsx",
    "mdx": "jsx"
  },
  "cSpell.enableFiletypes": [
    "!asciidoc",
    "!c",
    "!cpp",
    "!csharp",
    "!go",
    "!handlebars",
    "!haskell",
    "!jade",
    "!java",
    "!latex",
    "!php",
    "!pug",
    "!python",
    "!restructuredtext",
    "!rust",
    "!scala",
    "!scss"
  ],
  "editor.acceptSuggestionOnCommitCharacter": false,
  "explorer.compactFolders": false,
  "git.enableSmartCommit": true,
  "editor.accessibilitySupport": "off",
  "explorer.confirmDragAndDrop": false,
  "terminal.integrated.fontSize": 20,
  "terminal.integrated.fontFamily": "JetBrainsMono Nerd Font",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit"
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "graphql"
  ],
  "editor.semanticHighlighting.enabled": false,
  "breadcrumbs.enabled": false,
  "workbench.productIconTheme": "fluent-icons",
  "editor.fontFamily": "JetBrains Mono",
  "gitlens.codeLens.authors.enabled": false,
  "editor.tabSize": 2,
  "security.workspace.trust.untrustedFiles": "newWindow",
  "files.exclude": {
    "**\/CVS": true,
    "**\/.DS_Store": true,
    "**\/.hg": true,
    "**\/.svn": true,
    "**\/.git": true,
    ".vscode": true,
  },
  "workbench.iconTheme": "symbols",
  "update.mode": "none",
  "terminal.integrated.gpuAcceleration": "on",
  "terminal.integrated.defaultProfile.osx": "fish",
  "[jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[json]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "window.commandCenter": false,
  "git.openRepositoryInParentFolders": "always",
  "symbols.hidesExplorerArrows": false,
  "[javascript]": {
    "editor.defaultFormatter": "vscode.typescript-language-features"
  },
  "console-ninja.featureSet": "Community",
  "workbench.editor.empty.hint": "hidden",
  "update.showReleaseNotes": false,
  "security.promptForLocalFileProtocolHandling": false,
  "workbench.activityBar.location": "hidden",
  "apc.activityBar": {
    "position": "bottom",
    "hideSettings": true,
    "size": 48,
    "itemMargin": 8,
    "itemSize": 32
  },
  "editor.hideCursorInOverviewRuler": true,
  "editor.minimap.enabled": false,
  "window.titleBarStyle": "native",
  "apc.electron": {
    "titleBarStyle": "hiddenInset",
    "trafficLightPosition": {
      "x": 11,
      "y": 10
    },
    "opacity": 1,
    "vibrancy": "dark",
    "frame": false
  },
  "apc.header": {
    "height": 40
  },
  "apc.listRow": {
    "height": 25
  },
  "apc.font.family": "Inter",
  "apc.stylesheet": {
    ".title-label > h2": "display: none",
    ".editor-actions": "display: none",
    ".nosidebar div.inline-tabs-placeholder": "width: 75px",
    ".pane-header": "padding: 0 8px",
    ".pane-body": "padding: 8px",
    ".split-view-view:first-child .pane-header": "display: none !important;",
    ".monaco-list-row": "border-radius: 4px;",
    ".monaco-workbench .monaco-list:not(.element-focused):focus:before": "display: none;"
  },
  "editor.scrollbar.vertical": "hidden",
  "explorer.sortOrder": "foldersNestsFiles",
  "explorer.fileNesting.patterns": {
    "package.json": ".eslint*, prettier*, tsconfig*, vite*, pnpm-*, bun.lockb, nest*, package-lock*",
    "tailwind.config.*": "tailwind.config*, postcss.config*",
    ".env.local": ".env*",
    ".env": ".env*"
  },
  "explorer.fileNesting.enabled": true,
  "cSpell.userWords": [
    "automations",
    "bootcamp",
    "chakra",
    "checkin",
    "checkins",
    "cloudflare",
    "clsx",
    "Codegen",
    "datadog",
    "Datetime",
    "dayjs",
    "Dotenv",
    "Elysia",
    "esbuild",
    "fastify",
    "Fastify",
    "feedbackwidget",
    "ffprobe",
    "gamificada",
    "Hasher",
    "hono",
    "Hono",
    "ilike",
    "IUGU",
    "jamjuree",
    "jupiter",
    "ksuid",
    "liveblocks",
    "LIVEBLOCKS",
    "Marguerita",
    "middlewares",
    "mixpanel",
    "monaco",
    "nestjs",
    "nivo",
    "omni",
    "Omni",
    "Onboarded",
    "pallas",
    "postgres",
    "postgresql",
    "prefetch",
    "reactflow",
    "retriable",
    "roboto",
    "rocketseat",
    "rotion",
    "rsxp",
    "Sandpack",
    "shiki",
    "skylab",
    "sqlite",
    "supergraph",
    "svgr",
    "sympla",
    "tailwindcss",
    "textblock",
    "tiptap",
    "trpc",
    "TRPC",
    "tsup",
    "unfollow",
    "Unfollow",
    "unform",
    "Unform",
    "unmark",
    "upsert",
    "Usuario",
    "webm",
    "WEBPUSH"
  ],
  "workbench.statusBar.visible": false,
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": "keyword.other.dotenv",
        "settings": {
          "foreground": "#FF000000"
        }
      }
    ]
  },
  "workbench.layoutControl.enabled": false,
  "window.autoDetectColorScheme": true,
  "workbench.preferredDarkColorTheme": "poimandres",
  "workbench.preferredLightColorTheme": "Min Dark",
  "gitlens.advanced.messages": {
    "suppressIntegrationRequestTimedOutWarning": true
  },
  "liveServer.settings.donotShowInfoMsg": true,
  "update.enableWindowsBackgroundUpdates": false,
  "terminal.integrated.env.windows": {},
  "workbench.editor.tabSizing": "shrink",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "window.customTitleBarVisibility": "never",
  "window.newWindowDimensions": "maximized",
  "window.restoreFullscreen": true,
  "window.menuBarVisibility": "hidden"
}
```
# Versão Laranja com Vesper++ (alternativo)

[Meu vscode minimalista](https://www.youtube.com/watch?v=TW3KoPkuWEA)

```json
{
  "window.zoomLevel": 1,
  "workbench.colorTheme": "Vesper ++",
  "symbols.hidesExplorerArrows": false,
  "workbench.iconTheme": "symbols",
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontSize": 18,
  "editor.lineHeight": 1.8,
  "editor.rulers": [80, 120]
  "workbench.startupEditor": "newUntitledFile",
  "editor.renderLineHighlight": "gutter",
  "editor.fontLigatures": true,
  "workbench.editor.labelFormat": "short",
  
  /*configurações importantes*/
  "explorer.compactFolders": false,
  "editor.semanticHighlighting.enabled": false,
  "breadcrumbs.enabled": false,
  "editor.scrollbar.vertical": "hidden",
  "editor.scrollbar.horizontal": "hidden",
  /*controle da barra de menu superior (File, edition, menu)*/

  "window.titleBarStyle": "custom",
  "workbench.statusBar.visible": false,
  "window.customTitleBarVisibility": "windowed",
  "window.newWindowDimensions": "maximized",
  "window.restoreFullscreen": true,
  "workbench.layoutControl.enabled": false,
  "window.menuBarVisibility": "compact",

  /*apc customs*/
  "apc.header": {
    "height": 36
  },
  "apc.listRow": {
    "height": 24
  },

  "apc.font.family": "Inter",
  "apc.stylesheet": {
    ".title-label > h2": "display: none",
    ".editor-actions:": "display: none",
    ".pane-header": "padding: 0 8px",
    ".pane-body": "padding: 8px",
    ".split-view-view:first-child .pane-header": "display: none !important;",
    ".monaco-list-row": "border-radius: 4px;",
    ".monaco-workbeench .monaco-list:not(.element-focused):focus:before": "display: none;"
  },

  "window.commandCenter": false,
  "explorer.fileNesting.enabled": true,
  "explorer.fileNesting.patterns": {
    "package.json": ".eslint*, prettier*, tsconfig*, vite*, pnpm-lock*, package-lock*, bun.lockb",
    "tailwind.config*": "tailwind.config*, postcss.config*",
    ".env.local": ".env*",
    ".env": ".env*"
  },
  "terminal.integrated.fontSize": 14,
  "terminal.integrated.fontFamily": "JetBrainsMono Nerd Font",
  "workbench.editor.empty.hint": "hidden",

  /*prettier*/
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "prettier.enable": true,
  "prettier.singleQuote": false,
  "prettier.tabWidth": 2,
  "prettier.semi": false,
  
  /*terminal*/
  "terminal.integrated.profiles.windows": {
    "Git Bash": {
      "source": "Git Bash"
    }
  },
  "terminal.integrated.defaultProfile.windows": "Git Bash",
  /*a linha acima somente funciona com a instalação do git e registro do git nas variáveis do sistema*/

  /*editor*/
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "files.autoSave": "afterDelay",
  "workbench.sideBar.location": "right",
  "workbench.editor.autoLockGroups": {
    "default": true,
    "workbench.editor.chatSession": true,
    "workbench.editorinputs.searchEditorInput": true,
    "jupyter-notebook": true,
    "imagePreview.previewEditor": true,
    "vscode.audioPreview": true,
    "vscode.videoPreview": true,
    "jsProfileVisualizer.cpuprofile.table": true,
    "jsProfileVisualizer.heapsnapshot.table": true,
    "workbench.editors.gettingStartedInput": true,
    "workbench.input.interactive": true,
    "mainThreadWebview-markdown.preview": true
  },

  "git.terminalGitEditor": true,
  "editor.minimap.enabled": false,
  "security.workspace.trust.untrustedFiles": "open",
  "php.validate.executablePath": ""
}
```
