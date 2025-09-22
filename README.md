# AstroNvim Template

**NOTE:** This is for AstroNvim v5+

A template for getting started with [AstroNvim](https://github.com/AstroNvim/AstroNvim)

## 🛠️ Installation

#### Make a backup of your current nvim and shared folder

```shell
mv ~/.config/nvim ~/.config/nvim.bak
rm -rf ~/.local/share/nvim
rm -rf ~/.local/state/nvim
rm -rf ~/.cache/nvim
```

#### Create a new user repository from this template

Press the "Use this template" button above to create a new repository to store your user configuration.

You can also just clone this repository directly if you do not want to track your user configuration in GitHub.

#### Clone the repository

```shell
git clone https://github.com/keer2345/nvim-AstroNvim ~/.config/nvim
```

#### Start Neovim

```shell
nvim
```

## Setup
- [Community Plugins](https://github.com/AstroNvim/astrocommunity)

### colorscheme (Theme)
Edit `~/.config/nvim/lua/community.lua`:
```lua
return {
  -- ...

  { import = "astrocommunity.colorscheme.catppuccin" },
}
```

Copy the contents of [init.lua](https://github.com/AstroNvim/astrocommunity/blob/main/lua/astrocommunity/colorscheme/catppuccin/init.lua) to new file `./lua/plugins/catppuccin.lua`.

Restart Neovim and it download catppuccin colorscheme auto.

Then edit `./lua/plugins/astroui.lua`:
- Comment out the first line.
- add `colorscheme = "catppuccin",` and comment old colorscheme .

```lua
-- if true then return {} end -- WARN: REMOVE THIS LINE TO ACTIVATE THIS FILE

-- ...

---@type LazySpec
return {
  "AstroNvim/astroui",
  ---@type AstroUIOpts
  opts = {
    -- change colorscheme
    -- colorscheme = "astrodark",
    colorscheme = "catppuccin",

    -- ...
    
  },
}
```
