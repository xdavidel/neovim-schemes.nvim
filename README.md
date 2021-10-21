# Neovim Schemes

A collection of color schemes for neovim.

**Included Themes**

- code (basically just vscode dark+)
- onedark
- nord
- aurora (more colorful nord)
- gruvbox
- palenight
- dracula
- snazzy
- xoria

### Credit

The generate script comes from this repo: https://github.com/felipec/vim-felipec
Most of the colorscheme came from [ChristianChiarulli](https://github.com/ChristianChiarulli/nvcode-color-schemes.vim)

### Requirements 

This color scheme requires [treesitter](https://github.com/nvim-treesitter/nvim-treesitter) and [Neovim](https://neovim.io/) > 0.5.

## Installing

With `Vim-plug`

```viml
Plug 'christianchiarulli/nvcode-color-schemes.vim'
Plug 'nvim-treesitter/nvim-treesitter'
```

With `Packer`
```lua
  use {
    'xdavidel/neovim-schemes.nvim',
    config = function()
      vim.g.colors_name = <selected theme>
      vim.cmd[[colorscheme <selected theme>]]
    end
  }
```

## Contributing

- Create a YAML file
- Modify the highlight groups with custom colors 
- Run the generate script and save the output to the colors directory 
	- `generate colorscheme_name.yml >  ./colors/colorscheme_name.vim`
- Create a PR

Below are the treesitter highlight groups; modify these to take advantage of treesitter highlighting.

```viml
" Misc
highlight TSError guifg=#F44747
highlight TSPunctDelimiter guifg=#ABB2BF
highlight TSPunctBracket guifg=#ABB2BF
highlight TSPunctSpecial guifg=#ABB2BF

" Constants
highlight TSConstant guifg=#DCDCAA
highlight TSConstBuiltin guifg=#569CD6
" Not sure about this guy
highlight TSConstMacro guifg=#4EC9B0
highlight TSString guifg=#CE9178
highlight TSStringRegex guifg=#CE9178
highlight TSStringEscape guifg=#D7BA7D
highlight TSCharacter guifg=#CE9178
highlight TSNumber guifg=#B5CEA8
highlight TSBoolean guifg=#569CD6
highlight TSFloat guifg=#B5CEA8
highlight TSAnnotation guifg=#DCDCAA
highlight TSAttribute guifg=#FF00FF
highlight TSNamespace guifg=#FF00FF


" Functions
" highlight TSFuncBuiltin guifg=#4EC9B0
highlight TSFuncBuiltin guifg=#DCDCAA
highlight TSFunction guifg=#DCDCAA
highlight TSFuncMacro guifg=#DCDCAA
highlight TSParameter guifg=#9CDCFE
highlight TSParameterReference guifg=#9CDCFE
highlight TSMethod guifg=#DCDCAA
highlight TSField guifg=#9CDCFE
highlight TSProperty guifg=#9CDCFE
highlight TSConstructor guifg=#4EC9B0

" Keywords
highlight TSConditional guifg=#C586C0
highlight TSRepeat guifg=#C586C0
highlight TSLabel guifg=#FF00FF
" Does not work for yield and return they should be diff then class and def
highlight TSKeyword guifg=#569CD6
highlight TSKeywordFunction guifg=#FF00FF
highlight TSKeywordOperator guifg=#569CD6
highlight TSOperator guifg=#ABB2BF
highlight TSException guifg=#C586C0
highlight TSType guifg=#4EC9B0
highlight TSTypeBuiltin guifg=#FF00FF
highlight TSStructure guifg=#FF00FF
highlight TSInclude guifg=#C586C0

" Variable
highlight TSVariable guifg=#9CDCFE
highlight TSVariableBuiltin guifg=#9CDCFE

" Text
highlight TSText guifg=#FF00FF
highlight TSStrong guifg=#FF00FF
highlight TSEmphasis guifg=#FF00FF
highlight TSUnderline guifg=#FF00FF
highlight TSTitle guifg=#FF00FF
highlight TSLiteral guifg=#FF00FF
highlight TSURI guifg=#FF00FF

" Tags
highlight TSTag guifg=#569CD6
highlight TSTagDelimiter guifg=#5C6370
```
