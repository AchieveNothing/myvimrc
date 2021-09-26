### 安装vim-plug

```
镜像加速 curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://gitee.com/RaneChan/vim-plug/raw/master/plug.vim
更改 let fmt = get(g:, 'plug_url_format', 'https://git::@github.com/%s.git') 为
let fmt = get(g:, 'plug_url_format', 'https://git::@hub.fastgit.org/%s.git')
更改 \ '^https://git::@github\.com', 'https://github.com', '') 为
\ '^https://git::@hub.fastgit\.org', 'https://hub.fastgit.org', '')
```



### 安装ccls作为补全插件

```
sudo aptitude install ccls
sudo curl -sL install-node.now.sh/lts |sudo bash
```

  打开VIM，输入:CocInstall coc-ccls、:CocInstall coc-snippets，然后输入:CocConfig后回车可打开coc的配置文件，然后输入:

```
{
  "languageserver": {
    "ccls": {
      "command": "ccls",
      "filetypes": ["c", "cpp", "cuda", "objc", "objcpp"],
      "rootPatterns": [".ccls-root", "compile_commands.json"],
      "initializationOptions": {
        "cache": {
          "directory": ".ccls-cache"
        },
        "client": {
          "snippetSupport": true
        }
      }
    }
  }
}

```

```
cd ~/.config/coc/extensions/node_modules/coc-ccls
ln -s node_modules/ws/lib lib
sudo aptitude install python3-dev python2-dev
```

### 安装powerline字体

```
sudo pip install powerline-status
sudo aptitude install fonts-powerline
Plug 'powerline/powerline', {'rtp': 'powerline/bindings/vim'}
```

```
#/bin/bash
# install DroidSansMono Nerd Font --> u can choose another at: https://www.nerdfonts.com/font-downloads
echo "[-] Download fonts [-]"
echo "https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/DroidSansMono.zip"
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/DroidSansMono.zip
unzip DroidSansMono.zip -d ~/.fonts
fc-cache -fv
echo "done!"
```

