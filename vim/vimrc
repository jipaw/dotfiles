call plug#begin('~/.config/vim/plugged')

" colorschemes
Plug 'chriskempson/base16-vim'
Plug 'crusoexia/vim-monokai'


" utilities
Plug 'bling/vim-airline'
Plug 'Raimondi/delimitMate'
Plug 'ctrlpvim/ctrlp.vim'
Plug 'scrooloose/nerdtree'

call plug#end()


set nocompatible " not compatible with vi
set autoread " detect when a file is changed


" set syntax
syntax on

set backspace=2		" make backspace behave in a sane manner
set ruler 		" show the cursor positon all the time
set showcmd		" display incomplete command
set laststatus=2 	" show the satus line all the time
set autowrite		" Automatically : write before running command
set autoread		" Reload files changed outside vim
" Trigger autoread when changing buffers or coming back to vim in terminal
au FocusGained,Bufenter * :silent! !


 "" => Mappings""""""""""""""""""""""""""""""""""""""""""""""""""
"^""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" General mappings/shortcuts for functionality
" Additional, plugin-specific mappings are located under
" the plugins section

" set a map leader for more key combos
let mapleader = " " 
let g:mapleader = " " 

" remap esc
inoremap jj <esc>

" show line numbers
" set relativenumber " show relative line numbers
set number " show the current line number"


" shortcut to save
nmap <leader>w :w<cr>
nmap <leader>q :q<cr>
nmap <leader>wq :q<cr>

" Seraching
nnoremap / /\v
vnoremap / /\v
set gdefault	" Never have to tupe /g at the end of search / replace
set ignorecase		" case insensitive searching (unless specified)
set smartcase
set hlsearch

" clear highlighted search
" noremap <space> :set hlsearch! hlsearch?<cr>
set incsearch
set showmatch

" toggle invisible characters
set invlist
set listchars=tab:?\ ,eol:¬,trail:·,extends:?,precedes:?
highlight SpecialKey ctermbg=none " make the highlighting of tabs less annoying
set showbreak=?
nmap <leader>l :set list!<cr>

" Softtabs, 4 spaces
set tabstop=4
set shiftwidth=4
set shiftround
set expandtab

" set paste toggle
set pastetoggle=<F6>

" toggle paste mode
map <leader>v :set paste!<cr>

" Windows & Panes 
" Open new split panes to right and bottom
set splitbelow
set splitright

"Auto resize Vim splits to active split
set winwidth=84
set winheight=5
set winminheight=5
set winheight=999

"HTML Editing
set matchpairs+=<:>

"Treat <li> and <p> tags like the block tags they are
let g:html_indent_tags = 'li\|p'

" ============== Scrolling ===================

set scrolloff=8
set sidescrolloff=15
set sidescroll=1

"toggle relative numbering, and set to absolute on loss off focus or insert
"Mode
set number
set numberwidth=7

set rnu
" Set relative line number
function! NumberToggle()
    if(&relativenumber == 1)
        set norelativenumber
    else
        set relativenumber
    endif
endfunction

nnoremap nn :call NumberToggle()<cr>

function! ToggleNumbersOn()
	set nu!
	set rnu
endfunction
function! ToggleRelativeOn()
	set rnu!
	set nu
endfunction
autocmd FocusLost * call ToggleRelativeOn()
autocmd FocusGained * call ToggleRelativeOn()
autocmd InsertEnter * call ToggleRelativeOn()
autocmd InsertLeave * call ToggleRelativeOn()


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Functions
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Plugins

"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

" airline options
let g:airline_powerline_fonts=1
let g:airline_left_sep=''
let g:airline_right_sep=''
let g:airline_theme='base16'
