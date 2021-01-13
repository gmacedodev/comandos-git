# Aprendizados sobre Git
###### Estudos feitos no curso [Git e Github Essencial para o Desenvolvedor](https://www.udemy.com/course/curso-de-git-e-github-essencial/)
> Se tiver algo errado aqui, abra uma issue que vou corrigir :wink:

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

- **`.gitignore`** --> Bem auto explicativo, é um arquivo em que você coloca arquivos/diretórios/etc, que você quer que o git ignore. Normalmente usado pra banco de dados, lógica de negócios, autenticações, etc.
  - Para arquivos, coloque o arquivo e extensão, exemplo **`video.mp4`** **`db.sqlite`** etc
  - Para ignorar vários arquivos com a mesma extensão, use **\*** e a extensão, exemplo **`*.sqlite3`**
  - Para diretórios, coloque **\*\*** e o nome do diretório, exemplo **`**videos`** **`**database`**

- **`git config user.name ""`** --> configurar seu nome de usuário.

- **`git config user.email ""`** --> configurar email do usuário.
  - Se estiver numa máquina pessoal, de uso exclusivo, utilize **`--global`** depois do **`config`** para que todos projetos comecem com essa configuração padrão.

- **`git add`** seguido do nome e extensão do arquivo, para adicionar arquivos ao monitoramento do git. **Também** é usado quando você modifica um arquivo.

- **`git add .`** --> diz pro git tanto pra adicionar arquivos novos pro monitoramento, quanto pra monitorar os modificados.

- **`git mv arquivo1.extensao arquivo2.extensao`** --> renomeia arquivos
  > Por que fazer isso pelo git e não pelo terminal normal? Porque quando você faz isso, na verdade o arquivo anterior é apagado, e é criado um nome arquivo, com mesmo conteúdo mas nome diferente. Você tem que adicionar novamente o arquivo, com o novo nome, ao rastreio do Git, e também tem que adicionar o arquivo deletado (??wtf??) com o nome antigo.

  > Renomeando pelo próprio git, o arquivo só muda o nome mesmo, continua rastreado, pronto pro commit. Muito menos dor de cabeça.

- **`git rm arquivo.extensao`** --> deletar arquivo. **`git rm -rf pasta/`** --> deletar diretório
  > Mas preste atenção, só pode excluir um diretório ou arquivo que já esteja sendo tracked pelo Git, do contrário vai dar erro, pois pra ele "não existe". Ah, e diretórios vazios não são sequer enxergados pelo Git, ele nem dá algum aviso. E portanto não dá pra remover, são untracked.

- **`git diff`** vem de difference, mostra as diferenças de um estado pro outro, de um commit pro que virá.
  - Você tem que adicionar algo amais, exemplo **`git diff --staged`** para verificar diferença do anterior pro atual.
  - **`git diff hash`** --> verificar a diferença com um commit especifico.
  - **`git diff hash..hash`** para ver a diferença de um commit **até** o outro.

</details>
