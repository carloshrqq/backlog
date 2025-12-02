#markdown/guide #mega/download #obsidian/guide #obsidian/plugins #youtube/tutorial #youtube/profile/lucasbadico #pkm
# Prefácio

Conteúdo iniciante de nível fácil para quebrar o gelo inicial do obsidian. Segue o link de referência para criação deste documento (adaptado por [Carlos Henrique](https://github.com/carlos7z))

Link do vídeo Youtube [Obsidian para devs: configurando daily notes, calendar, git backup excalidraw](https://www.youtube.com/watch?v=ofy5N6Ef8ks)
Link do canal Youtube [Lucas Badico](https://www.youtube.com/@lucas_badico)
Link MEGA para [download](https://mega.nz/file/jUwmTQRB#9jrDpWVeEPr9xF-0g19iM4rCaA1gWh_rNVW7TUqghrw) (criado em 2025-01-23 verificar expiração)

# Títulos e Subtítulos

Para utilizar títulos e subtítulos (e subtítulos dos subtítulos dos subtítulos) utilizar `# título`. Entrada: hashtag>espaço>título.

```markdown
# título 1
## subtítulo 1.1
### subtítulo 1.1.1
#### subtítulo 1.1.1.1
##### subtítulo 1.1.1.1.1
###### subtítulo 1.1.1.1.1.1
```

Utilizar títulos e subtítulos estrutura o documento. A estrutura é útil para visualização em ordem dentro e fora do obsidian. 

# Listas

Para criar uma lista simples `- item`. Entrada traço (ou menos)>espaço. Para adicionar um subitem pressionar TAB antes de começar a digitar o conteudo do subitem. 

```markdown
- item
	- subitem
```

# Checklist

Para criar um checklist simples `- [ ]` (traço > espaço > abre colchetes > espaço > fecha colchetes).
```markdown
- [x] exemplo checklist 1 (marcação)
- [ ] exemplo checklist 2 (sem marcação)
	- [ ] subitem cheklist 2.1
```

A saída cria uma caixa retangular de bordas circulares que pode ser marcada com um 'v' azul.
# Citações para outras notas (notas existentes ou inexistentes)

Para transformar uma palavra em um link para uma nota existente ou inexistente (se não existir basta clicar para criar depois que o link estiver pronto) basta utilizar `[[palavra que deve se tornar um link para uma nota existente ou não]]` por exemplo `[[tarefas]]` ou `[[evento importante]]`. Entrada abre colchete>abre colchete>texto>fecha colchete>fecha colchete.

Se o texto linkado ainda não existir como nota (esperado em casos de inicio de estudo de contexto) basta clicar no link para criar a nota com o título do link.

# Nomes ou textos customizados para links internos e externos

Para customizar o texto exibido para um link externo, em markdown, temos:
```markdown
[Texto customizado aqui](https://linkdapaginahtml.com)
```

Para customizar o texto exibido em um link interno, em markdown, temos:
Importante: não utilizar espaços entre o caractere"|"
```markdown
[[nomedanota|Texto customizado aqui]]
```

Também é possível utilizar javascript no lugar do "nomedanota" para determinar o nome de um arquivo.
```js
<< [[<% fileDateYesterday =  tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|voltar]] | [[<% fileDateTomorrow = tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|avançar]] >>
```

Nomes customizados podem tornar o contexto claro e amigável para a navegação. 

A combinação de nomes de links customizados possibilitam a criação de sistemas de navegação entre notas com base em cabeçalhos (mkd) e data (js). 

# Plugins

[Plugins da comunidade](/c/community-plugins.md) para acessar a minha nota referente aos plugins da comunidade.