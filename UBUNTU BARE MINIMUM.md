## UBUNTU RAW

sudo fallocate -l 4G /swapfile && sudo chmod 600 /swapfile && sudo mkswap /swapfile && sudo swapon /swapfile && sudo cp /etc/fstab /etc/fstab.bak && echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab && sudo apt update -y && sudo apt-get update -y && sudo apt-get upgrade -y && sudo apt dist-upgrade -y && sudo apt-get autoremove -y && sudo apt-get clean -y && sudo apt-get autoclean -y && sudo apt update -y && sudo apt-get update -y && sudo apt-get install mosh -y && sudo apt install python3-pip -y && sudo apt-get install postgresql -y && sudo snap install ngrok rclone && sudo snap install cmake --classic && sudo snap install node --edge --classic && sudo snap install google-cloud-sdk --classic && pip3 install cryptography==2.5 psycopg2-binary asyncio asyncpg joblib scrapy selenium scrapy-selenium unicodedata2 requests-html beautifulsoup4 multiprocess httplib2 numpy google-api-python-client google_auth_oauthlib oauth2client google_spreadsheet virtualenv django bottle flask Flask-SSLify gspread pandas gspread-dataframe aiogram python-telegram-bot --no-warn-script-location && && sudo npm i -g -S localtunnel

## VIM 
```
if empty(glob('~/.vim/autoload/plug.vim'))
  silent !curl -fLo ~/.vim/autoload/plug.vim --create-dirs
    \ https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
  autocmd VimEnter * PlugInstall --sync | source $MYVIMRC
endif

call plug#begin('~/.vim/plugged')
Plug 'terryma/vim-multiple-cursors'
Plug '907th/vim-auto-save'
Plug 'chrisbra/csv.vim'
Plug 'Townk/vim-autoclose'
Plug 'Quramy/tsuquyomi'
Plug 'Shougo/vimproc.vim'
Plug 'itchyny/lightline.vim'
Plug 'tomasiser/vim-code-dark'
call plug#end()

filetype plugin indent off
set number    
set expandtab    
set tabstop=2    
set softtabstop=2    
set shiftwidth=2    
set textwidth=80    
set cursorline    
set laststatus=2    
set omnifunc=syntaxcomplete#Complete    
set splitright 

nnoremap L <C-W><C-W>
nnoremap H <C-W><C-H>
tnoremap dk <C-W>w

inoremap ff <Esc>
inoremap ( ()<Left>
inoremap ' ''<Left>
inoremap " ""<Left> 

map ft :bprev<CR>
map fe :bnext<CR>
map fd :tabnew 

map Q :qa<CR>
map W :Vex<CR>
map E <C-d>
map R <C-u> 
map c <C-f>
map x <C-b> 
map B :vert term<CR>
map K :below term<CR>
map ss ZZ
map F :vert res 50<CR>
map M <C-z>
map S :s/\<\>//g<left><left><left><left><left>
map ee :s/^/# /g<CR>:let @/ = ""<CR>
map rr :s/^# //g<CR>:let @/ = ""<CR>
map vs :vs 

let g:netrw_banner = 0
let g:netrw_liststyle = 3
let g:netrw_browse_split = 4
let g:netrw_winsize = 25
let g:netrw_altv = 1
let g:auto_save = 1
let g:auto_save_silent = 1
let g:auto_save_events = ["InsertLeave","TextChanged","TextChangedI"]
let g:tsuquyomi_disable_quickfix = 1
let g:ycm_autoclose_preview_window_after_completion = 1

colorscheme codedark
hi Normal guibg=NONE ctermbg=NONE
hi LineNr guibg=NONE ctermbg=NONE
hi EndOfBuffer guibg=NONE ctermbg=NONE
hi NonText guibg=NONE ctermbg=NONE
hi CursorLine ctermbg=NONE
hi Pmenu guifg=NONE ctermbg=NONE

ru macros/justify.vim
set bs=2
set noshowmode

```