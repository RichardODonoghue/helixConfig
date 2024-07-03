# My personal config for the Helix text editor

This is set up with support for formatting with Prettier, linting with ESLint, emmet and LSP configuration for Typescript, TSX, JSX, Javascript, JSON, HTML, CSS, TailwindCSS and rainbow CSV formatting. 

This setup provides a good base for anyone wanting to try the editor for web development.

# Themes 
This configuration uses the stock key mappings and has the `monokai_pro` theme enabled by default. This can be configured to something else in config.toml. 
There is a folder called themes in the repo directory which contains a collection of additional themes

# Requirements

In order to have a fully functional configuration, you will need to install the following NPM packages globally 

Run the following commands in your terminal (assuming you are running a linux distribution). 

```
npm i -g vscode-lang-servers-extracted prettier emmet-ls  @tailwindcss/language-server typescript-language-server typescript
```

After this, check the health of your Helix setup by running `hx --health`

Your setup should look like the following 

```
Language                 LSP                      DAP                      Formatter                Highlight                Textobject               Indent                   
ada                      ✘ ada_language_server…   None                     None                     ✓                        ✓                        ✘                        
                         ✘ ada_language_server…   
agda                     None                     None                     None                     ✓                        ✘                        ✘                        
astro                    None                     None                     None                     ✓                        ✘                        ✘                        
awk                      ✘ awk-language-server…   None                     None                     ✓                        ✓                        ✘                        
bash                     ✘ bash-language-serve…   None                     None                     ✓                        ✓                        ✓                        
bass                     ✘ bass                   None                     None                     ✓                        ✘                        ✘                        
beancount                None                     None                     None                     ✓                        ✘                        ✘                        
bibtex                   ✘ texlab                 None                     ✘ bibtex-tidy            ✓                        ✘                        ✘                        
bicep                    ✘ bicep-langserver       None                     None                     ✓                        ✘                        ✘                        
blade                    None                     None                     None                     ✓                        ✘                        ✘                        
blueprint                ✘ blueprint-compiler     None                     None                     ✓                        ✘                        ✘                        
c                        ✘ clangd                 ✘ lldb-vscode            None                     ✓                        ✓                        ✓                        
c-sharp                  ✘ OmniSharp              ✘ netcoredbg             None                     ✓                        ✓                        ✘                        
cabal                    ✘ haskell-language-se…   None                     None                     ✘                        ✘                        ✘                        
cairo                    ✘ cairo-language-serv…   None                     None                     ✓                        ✓                        ✓                        
capnp                    None                     None                     None                     ✓                        ✘                        ✓                        
cel                      None                     None                     None                     ✓                        ✘                        ✘                        
clojure                  ✘ clojure-lsp            None                     None                     ✓                        ✘                        ✘                        
cmake                    ✘ cmake-language-serv…   None                     None                     ✓                        ✓                        ✓                        
comment                  None                     None                     None                     ✓                        ✘                        ✘                        
common-lisp              ✘ cl-lsp                 None                     None                     ✓                        ✘                        ✓                        
cpon                     None                     None                     None                     ✓                        ✘                        ✓                        
cpp                      ✘ clangd                 ✘ lldb-vscode            None                     ✓                        ✓                        ✓                        
crystal                  ✘ crystalline            None                     None                     ✓                        ✓                        ✘                        
css                      ✓ vscode-css-language…   None                     ✓ prettier               ✓                        ✘                        ✓                        
                         ✓ tailwindcss-languag…   
csv                      None                     None                     None                     ✘                        ✘                        ✘                        
cue                      ✘ cuelsp                 None                     ✘ cue                    ✓                        ✘                        ✘                        
d                        ✘ serve-d                None                     ✘ dfmt                   ✓                        ✓                        ✓                        
dart                     ✘ dart                   None                     None                     ✓                        ✓                        ✓                        
dbml                     None                     None                     None                     ✓                        ✘                        ✘                        
devicetree               None                     None                     None                     ✓                        ✘                        ✘                        
dhall                    ✘ dhall-lsp-server       None                     ✘ dhall                  ✓                        ✓                        ✘                        
diff                     None                     None                     None                     ✓                        ✘                        ✘                        
docker-compose           ✘ docker-compose-lang…   None                     None                     ✓                        ✘                        ✓                        
                         ✘ yaml-language-serve…   
dockerfile               ✘ docker-langserver      None                     None                     ✓                        ✘                        ✘                        
dot                      ✘ dot-language-server…   None                     None                     ✓                        ✘                        ✘                        
dtd                      None                     None                     None                     ✓                        ✘                        ✘                        
edoc                     None                     None                     None                     ✓                        ✘                        ✘                        
eex                      None                     None                     None                     ✓                        ✘                        ✘                        
ejs                      None                     None                     None                     ✓                        ✘                        ✘                        
elixir                   ✘ elixir-ls              None                     None                     ✓                        ✓                        ✓                        
elm                      ✘ elm-language-server…   None                     None                     ✓                        ✓                        ✘                        
elvish                   ✘ elvish                 None                     None                     ✓                        ✘                        ✘                        
env                      None                     None                     None                     ✓                        ✘                        ✘                        
erb                      None                     None                     None                     ✓                        ✘                        ✘                        
erlang                   ✘ erlang_ls              None                     None                     ✓                        ✓                        ✘                        
esdl                     None                     None                     None                     ✓                        ✘                        ✘                        
fidl                     None                     None                     None                     ✓                        ✘                        ✘                        
fish                     None                     None                     ✘ fish_indent            ✓                        ✓                        ✓                        
forth                    ✘ forth-lsp              None                     None                     ✓                        ✘                        ✘                        
fortran                  ✘ fortls                 None                     None                     ✓                        ✘                        ✓                        
fsharp                   ✘ fsautocomplete         None                     None                     ✓                        ✘                        ✘                        
gas                      None                     None                     None                     ✓                        ✓                        ✘                        
gdscript                 None                     None                     ✘ gdformat               ✓                        ✓                        ✓                        
gemini                   None                     None                     None                     ✓                        ✘                        ✘                        
git-attributes           None                     None                     None                     ✓                        ✘                        ✘                        
git-commit               None                     None                     None                     ✓                        ✓                        ✘                        
git-config               None                     None                     None                     ✓                        ✘                        ✘                        
git-ignore               None                     None                     None                     ✓                        ✘                        ✘                        
git-rebase               None                     None                     None                     ✓                        ✘                        ✘                        
gleam                    ✘ gleam                  None                     None                     ✓                        ✓                        ✘                        
glimmer                  ✘ ember-language-serv…   None                     ✓ prettier               ✓                        ✘                        ✘                        
glsl                     None                     None                     None                     ✓                        ✓                        ✓                        
gn                       None                     None                     ✘ gn                     ✓                        ✘                        ✘                        
go                       ✘ gopls                  ✘ dlv                    None                     ✓                        ✓                        ✓                        
                         ✘ golangci-lint-langs…   
godot-resource           None                     None                     None                     ✓                        ✘                        ✘                        
gomod                    ✘ gopls                  None                     None                     ✓                        ✘                        ✘                        
gotmpl                   ✘ gopls                  None                     None                     ✓                        ✘                        ✘                        
gowork                   ✘ gopls                  None                     None                     ✓                        ✘                        ✘                        
graphql                  ✘ graphql-lsp            None                     None                     ✓                        ✘                        ✘                        
groovy                   None                     None                     None                     ✓                        ✘                        ✘                        
hare                     None                     None                     None                     ✓                        ✘                        ✘                        
haskell                  ✘ haskell-language-se…   None                     None                     ✓                        ✓                        ✘                        
haskell-persistent       None                     None                     None                     ✓                        ✘                        ✘                        
hcl                      ✘ terraform-ls           None                     None                     ✓                        ✓                        ✓                        
heex                     ✘ elixir-ls              None                     None                     ✓                        ✓                        ✘                        
helm                     ✘ helm_ls                None                     None                     ✓                        ✘                        ✘                        
hocon                    None                     None                     None                     ✓                        ✘                        ✓                        
hoon                     None                     None                     None                     ✓                        ✘                        ✘                        
hosts                    None                     None                     None                     ✓                        ✘                        ✘                        
html                     ✓ vscode-html-languag…   None                     ✓ prettier               ✓                        ✘                        ✘                        
hurl                     None                     None                     ✘ hurlfmt                ✓                        ✘                        ✓                        
hyprlang                 None                     None                     None                     ✓                        ✘                        ✓                        
idris                    ✘ idris2-lsp             None                     None                     ✘                        ✘                        ✘                        
iex                      None                     None                     None                     ✓                        ✘                        ✘                        
ini                      None                     None                     None                     ✓                        ✘                        ✘                        
janet                    None                     None                     ✘ janet-format           ✓                        ✘                        ✘                        
java                     ✘ jdtls                  None                     None                     ✓                        ✓                        ✓                        
javascript               ✓ typescript-language…   ✘                        ✓ prettier               ✓                        ✓                        ✓                        
                         ✓ vscode-eslint-langu…   
jinja                    None                     None                     None                     ✓                        ✘                        ✘                        
jsdoc                    None                     None                     None                     ✓                        ✘                        ✘                        
json                     ✓ vscode-json-languag…   None                     ✓ prettier               ✓                        ✘                        ✓                        
json5                    None                     None                     None                     ✓                        ✘                        ✘                        
jsonc                    ✓ vscode-json-languag…   None                     None                     ✓                        ✘                        ✓                        
jsonnet                  ✘ jsonnet-language-se…   None                     None                     ✓                        ✘                        ✘                        
jsx                      ✓ typescript-language…   None                     ✓ prettier               ✓                        ✓                        ✓                        
                         ✓ vscode-eslint-langu…   
                         ✓ tailwindcss-languag…   
julia                    ✘ julia                  None                     None                     ✓                        ✓                        ✓                        
just                     None                     None                     None                     ✓                        ✓                        ✓                        
kdl                      None                     None                     None                     ✓                        ✓                        ✓                        
koka                     None                     None                     None                     ✓                        ✘                        ✓                        
kotlin                   ✘ kotlin-language-ser…   None                     None                     ✓                        ✘                        ✘                        
latex                    ✘ texlab                 None                     None                     ✓                        ✓                        ✘                        
ld                       None                     None                     None                     ✓                        ✘                        ✓                        
lean                     ✘ lean                   None                     None                     ✓                        ✘                        ✘                        
ledger                   None                     None                     None                     ✓                        ✘                        ✘                        
llvm                     None                     None                     None                     ✓                        ✓                        ✓                        
llvm-mir                 None                     None                     None                     ✓                        ✓                        ✓                        
llvm-mir-yaml            None                     None                     None                     ✓                        ✘                        ✓                        
log                      None                     None                     None                     ✓                        ✘                        ✘                        
lpf                      None                     None                     None                     ✓                        ✘                        ✘                        
lua                      ✘ lua-language-server…   None                     None                     ✓                        ✓                        ✓                        
make                     None                     None                     None                     ✓                        ✘                        ✓                        
markdoc                  ✘ markdoc-ls             None                     None                     ✓                        ✘                        ✘                        
markdown                 ✘ marksman               None                     None                     ✓                        ✘                        ✘                        
                         ✘ markdown-oxide         
markdown.inline          None                     None                     None                     ✓                        ✘                        ✘                        
matlab                   None                     None                     None                     ✓                        ✓                        ✓                        
mermaid                  None                     None                     None                     ✓                        ✘                        ✘                        
meson                    None                     None                     None                     ✓                        ✘                        ✓                        
mint                     ✘ mint                   None                     None                     ✘                        ✘                        ✘                        
msbuild                  None                     None                     None                     ✓                        ✘                        ✓                        
nasm                     None                     None                     None                     ✓                        ✓                        ✘                        
nickel                   ✘ nls                    None                     None                     ✓                        ✘                        ✓                        
nim                      ✘ nimlangserver          None                     None                     ✓                        ✓                        ✓                        
nix                      ✘ nil                    None                     None                     ✓                        ✓                        ✘                        
nu                       ✘ nu                     None                     None                     ✓                        ✘                        ✘                        
nunjucks                 None                     None                     None                     ✓                        ✘                        ✘                        
ocaml                    ✘ ocamllsp               None                     None                     ✓                        ✘                        ✓                        
ocaml-interface          ✘ ocamllsp               None                     None                     ✓                        ✘                        ✘                        
odin                     ✘ ols                    None                     ✘ odinfmt                ✓                        ✘                        ✓                        
ohm                      None                     None                     None                     ✓                        ✓                        ✓                        
opencl                   ✘ clangd                 None                     None                     ✓                        ✓                        ✓                        
openscad                 ✘ openscad-lsp           None                     None                     ✓                        ✘                        ✘                        
org                      None                     None                     None                     ✓                        ✘                        ✘                        
pascal                   ✘ pasls                  None                     None                     ✓                        ✓                        ✘                        
passwd                   None                     None                     None                     ✓                        ✘                        ✘                        
pem                      None                     None                     None                     ✓                        ✘                        ✘                        
perl                     ✘ perlnavigator          None                     None                     ✓                        ✓                        ✓                        
php                      ✘ intelephense           None                     None                     ✓                        ✓                        ✓                        
php-only                 None                     None                     None                     ✓                        ✘                        ✘                        
pkgbuild                 ✘ pkgbuild-language-s…   None                     None                     ✓                        ✓                        ✓                        
                         ✘ bash-language-serve…   
pkl                      None                     None                     None                     ✓                        ✘                        ✓                        
po                       None                     None                     None                     ✓                        ✓                        ✘                        
pod                      None                     None                     None                     ✓                        ✘                        ✘                        
ponylang                 None                     None                     None                     ✓                        ✓                        ✓                        
powershell               None                     None                     None                     ✓                        ✘                        ✘                        
prisma                   ✘ prisma-language-ser…   None                     None                     ✓                        ✘                        ✘                        
prolog                   ✘ swipl                  None                     None                     ✘                        ✘                        ✘                        
protobuf                 ✘ bufls                  None                     None                     ✓                        ✓                        ✓                        
                         ✘ pb                     
prql                     None                     None                     None                     ✓                        ✘                        ✘                        
purescript               ✘ purescript-language…   None                     ✘ purs-tidy              ✓                        ✓                        ✘                        
python                   ✘ pylsp                  None                     None                     ✓                        ✓                        ✓                        
qml                      ✘ qmlls                  None                     None                     ✓                        ✘                        ✓                        
r                        ✘ R                      None                     None                     ✓                        ✘                        ✘                        
racket                   ✘ racket                 None                     None                     ✓                        ✘                        ✓                        
regex                    None                     None                     None                     ✓                        ✘                        ✘                        
rego                     ✘ regols                 None                     None                     ✓                        ✘                        ✘                        
rescript                 ✘ rescript-language-s…   None                     None                     ✓                        ✓                        ✘                        
rmarkdown                ✘ R                      None                     None                     ✓                        ✘                        ✓                        
robot                    ✘ robotframework_ls      None                     None                     ✓                        ✘                        ✘                        
ron                      None                     None                     None                     ✓                        ✘                        ✓                        
rst                      None                     None                     None                     ✓                        ✘                        ✘                        
ruby                     ✘ solargraph             None                     None                     ✓                        ✓                        ✓                        
rust                     ✘ rust-analyzer          ✘ lldb-vscode            None                     ✓                        ✓                        ✓                        
sage                     None                     None                     None                     ✓                        ✓                        ✘                        
scala                    ✘ metals                 None                     None                     ✓                        ✓                        ✓                        
scheme                   None                     None                     None                     ✓                        ✘                        ✓                        
scss                     ✓ vscode-css-language…   None                     None                     ✓                        ✘                        ✘                        
slint                    ✘ slint-lsp              None                     None                     ✓                        ✓                        ✓                        
smali                    None                     None                     None                     ✓                        ✘                        ✓                        
smithy                   ✘ cs                     None                     None                     ✓                        ✘                        ✘                        
sml                      None                     None                     None                     ✓                        ✘                        ✘                        
solidity                 ✘ solc                   None                     None                     ✓                        ✘                        ✘                        
spicedb                  None                     None                     None                     ✓                        ✘                        ✘                        
sql                      None                     None                     None                     ✓                        ✘                        ✘                        
sshclientconfig          None                     None                     None                     ✓                        ✘                        ✘                        
starlark                 None                     None                     None                     ✓                        ✓                        ✘                        
strace                   None                     None                     None                     ✓                        ✘                        ✘                        
supercollider            None                     None                     None                     ✓                        ✘                        ✘                        
svelte                   ✘ svelteserver           None                     None                     ✓                        ✘                        ✓                        
sway                     ✘ forc                   None                     None                     ✓                        ✓                        ✓                        
swift                    ✘ sourcekit-lsp          None                     None                     ✓                        ✘                        ✘                        
t32                      None                     None                     None                     ✓                        ✘                        ✘                        
tablegen                 None                     None                     None                     ✓                        ✓                        ✓                        
tact                     None                     None                     None                     ✓                        ✓                        ✓                        
task                     None                     None                     None                     ✓                        ✘                        ✘                        
templ                    ✘ templ                  None                     None                     ✓                        ✘                        ✘                        
tfvars                   ✘ terraform-ls           None                     None                     ✓                        ✘                        ✓                        
todotxt                  None                     None                     ✓ sort                   ✓                        ✘                        ✘                        
toml                     ✘ taplo                  None                     None                     ✓                        ✘                        ✘                        
tsq                      None                     None                     None                     ✓                        ✘                        ✘                        
tsx                      ✓ typescript-language…   None                     ✓ prettier               ✓                        ✓                        ✓                        
                         ✓ vscode-eslint-langu…   
                         ✓ tailwindcss-languag…   
twig                     None                     None                     None                     ✓                        ✘                        ✘                        
typescript               ✓ typescript-language…   None                     ✓ prettier               ✓                        ✓                        ✓                        
                         ✓ vscode-eslint-langu…   
typst                    ✘ typst-lsp              None                     None                     ✓                        ✘                        ✘                        
ungrammar                None                     None                     None                     ✓                        ✘                        ✘                        
unison                   None                     None                     None                     ✓                        ✘                        ✓                        
uxntal                   None                     None                     None                     ✓                        ✘                        ✘                        
v                        ✘ v-analyzer             None                     None                     ✓                        ✓                        ✓                        
vala                     ✘ vala-language-serve…   None                     None                     ✓                        ✓                        ✘                        
verilog                  ✘ svlangserver           None                     None                     ✓                        ✓                        ✘                        
vhdl                     ✘ vhdl_ls                None                     None                     ✓                        ✘                        ✘                        
vhs                      None                     None                     None                     ✓                        ✘                        ✘                        
vue                      ✘ vue-language-server…   None                     None                     ✓                        ✘                        ✘                        
wast                     None                     None                     None                     ✓                        ✘                        ✘                        
wat                      None                     None                     None                     ✓                        ✘                        ✘                        
webc                     None                     None                     None                     ✓                        ✘                        ✘                        
wgsl                     ✘ wgsl_analyzer          None                     None                     ✓                        ✘                        ✘                        
wit                      None                     None                     None                     ✓                        ✘                        ✓                        
wren                     None                     None                     None                     ✓                        ✓                        ✓                        
xit                      None                     None                     None                     ✓                        ✘                        ✘                        
xml                      None                     None                     None                     ✓                        ✘                        ✓                        
yaml                     ✘ yaml-language-serve…   None                     None                     ✓                        ✘                        ✓                        
                         ✘ ansible-language-se…   
yuck                     None                     None                     None                     ✓                        ✘                        ✘                        
zig                      ✘ zls                    ✘ lldb-vscode            ✘ zig                    ✓                        ✓                        ✓    
```
