``m̀arkdown
    ___    ________  ___   ____  ____  ______   ____________    ___________
   / | / / |  / /  _/  |/  /  / __ \/ __ \/_  __/  / ____/  _/ /   / ____/ ___/
  /  |/ /| | / // // /|_/ /  / / / / / / / / /    / /_   / // /   / __/  \__ \ 
 / /|  / | |/ // // /  / /  / /_/ / /_/ / / /    / __/ _/ // /___/ /___ ___/ / 
/_/ |_/  |___/___/_/  /_/  /_____/\____/ /_/    /_/   /___/_____/_____//____/

<div align="center">
    
**NVIM setup tailored my own coding style and needs**

[![Lua](https://img.shields.io/badge/Lua-2C2D72?style=for-the-badge&logo=lua&logoColor=white)](https://www.lua.org)
[![NeoVim](https://img.shields.io/badge/NeoVim-57A143?style=for-the-badge&logo=neovim&logoColor=white)](https://neovim.io)

</div>

---

## 📋 Overview

This repository contains my personal **NeoVim configuration**, crafted for my own dev experience. It features several plugins, intuitive keybindings, and a modern aesthetic that enhances productivity and code readability.

<div align="center">
  <img src="https://via.placeholder.com/800x400?text=NeoVim+Config+Screenshot" alt="NeoVim Config" />
</div>

---

## ✨ Features

| Feature | Details |
|---------|---------|
| **Plugin Manager** | [Lazy.nvim](https://github.com/folke/lazy.nvim) - Fast and efficient plugin management |
| **Language Support** | LSP integration with Mason for multiple languages |
| **Fuzzy Finder** | [Telescope](https://github.com/nvim-telescope/telescope.nvim) for file and text searching |
| **Syntax Highlighting** | [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter) for improved syntax awareness |
| **Code Completion** | [nvim-cmp](https://github.com/hrsh7th/nvim-cmp) with multiple snippet sources |
| **Git Integration** | [Fugitive](https://github.com/tpope/vim-fugitive) + [Gitsigns](https://github.com/lewis6991/gitsigns.nvim) |
| **Status Line** | [Lualine](https://github.com/nvim-lualine/lualine.nvim) for custom status display |
| **File Explorer** | [Nvim-tree](https://github.com/nvim-tree/nvim-tree.lua) for easy file navigation |
| **Theme** | [TokyoNight](https://github.com/folke/tokyonight.nvim) beautiful color scheme |

---

## 📁 Directory Structure

```
~/.config/nvim/
├── init.lua                 # Main configuration entry point
├── lua/
│   ├── config/             # Configuration modules
│   │   ├── options.lua     # Editor options
│   │   ├── keymaps.lua     # Keybindings
│   │   └── autocmds.lua    # Autocommands
│   └── plugins/            # Plugin specifications
│       ├── completion.lua  # Completion plugins
│       ├── lsp.lua         # LSP configuration
│       ├── telescope.lua   # Fuzzy finder
│       └── ...
├── plugin/                 # Plugin-specific configs
└── README.md               # This file
```

---

### LSP Setup

Language servers are managed through Mason. Install additional servers:

```vim
:Mason
```

Then configure them in `lua/plugins/lsp.lua`.

---

## 📦 Plugin List

<details>
<summary><b>Core Plugins</b> (Click to expand)</summary>

- **lazy.nvim** - Plugin manager
- **nvim-lspconfig** - LSP client configuration
- **mason.nvim** - LSP installer
- **nvim-treesitter** - Syntax parsing
- **telescope.nvim** - Fuzzy finder
- **nvim-cmp** - Completion engine

</details>

<details>
<summary><b>UI & Navigation</b> (Click to expand)</summary>

- **nvim-tree.lua** - File explorer
- **lualine.nvim** - Status line
- **bufferline.nvim** - Buffer tabs
- **which-key.nvim** - Keybinding helper
- **indent-blankline.nvim** - Indentation guides

</details>

<details>
<summary><b>Editing & Productivity</b> (Click to expand)</summary>

- **vim-surround** - Surround operations
- **vim-commentary** - Easy commenting
- **nvim-autopairs** - Auto bracket pairing
- **gitsigns.nvim** - Git integration
- **vim-fugitive** - Git commands

</details>

---

## 🎨 Customization

### Change Theme

Edit `lua/plugins/ui.lua`:

```lua
return {
  {
    "folke/tokyonight.nvim",
    lazy = false,
    priority = 1000,
    config = function()
      vim.cmd.colorscheme("tokyonight-night")
    end,
  },
}
```
---

## 🤝 Contributing

Feel free to fork this repository and customize it to your needs. If you have suggestions feel free to submit a pull request or message me directly!
