# Aprendizados sobre Git
###### Estudos feitos no curso [Git e Github Essencial para o Desenvolvedor](https://www.udemy.com/course/curso-de-git-e-github-essencial/)
#####Por favor, se tiver algo errado aqui, abra uma issue que vou corrigir :wink:

<details><summary>Ciclo de vida dos arquivos</summary>

- **Untracked:** estados em que todos arquivos iniciam. Quando não está rastreado, sincronizado no repo local, no Git.
- **Tracked:** quando o arquivo está rastreado pelo Git, está sob o controle de versionamento.
- **Modified:** quando modifica um arquivo já rastreado. O Git te avisa que precisa atualizar o rastreamento.
- **Staged:** quando o arquivo está pronto pro commit.

</details>

<details><summary>Comandos Básicos</summary>

- **`history -c`** --> Apagar histórico do terminal git/linux.
  - Apagar de forma mais completa: **`cat /dev/null > ~/.bash_history && history -c`**
- **`git init`** --> Inicializar um repositório.
- **`git status`** --> Checar o estado dos arquivos do repo.
- **`.gitignore`** - Bem auto explicativo, é um arquivo em que você coloca arquivos/diretórios/etc, que você quer que o git ignore. Normalmente usado pra banco de dados, lógica de negócios, autenticações, etc.
  - Para arquivos, coloque o arquivo e extensão, exemplo **`video.mp4`** **`db.sqlite`** etc
  - Para ignorar vários arquivos com a mesma extensão, use **\*** e a extensão, exemplo **`*.sqlite3`**
  - Para diretórios, coloque **\*\*** e o nome do diretório, exemplo **`**videos`** **`**database`**
- **`git config user.name ""`** - para configurar seu nome de usuário. 
- **`git config user.email ""`** - para configurar email do usuário.
  - Se estiver numa máquina pessoal, de uso exclusivo, utilize **`--global`** depois do **`config`** para que todos projetos comecem com essa configuração padrão.
- **`git add`** seguido do nome e extensão do arquivo, para adicionar arquivos ao monitoramento do git. **Também** é usado quando você modifica um arquivo.
- **`git add .`** isso diz pro git tanto pra adicionar arquivos novos pro monitoramento, quanto pra monitorar os modificados.

</details>
