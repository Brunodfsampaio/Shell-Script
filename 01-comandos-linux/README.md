# 📘 Aula 01 – Comandos Linux Básicos

> 🐧 Curso: Shell Script  
> 📅 Tema: Introdução aos comandos essenciais do terminal Linux  
> 🎯 Objetivo: Entender e praticar os comandos fundamentais para navegação, manipulação de arquivos e análise de conteúdo no terminal.

---

## 📂 Navegação no Sistema

### 🔸 `cd` – Mudar de diretório
```bash
cd /caminho/do/diretorio    # Vai para o diretório indicado
cd                          # Vai para o diretório pessoal (home)
```

# 🔸 ls – Listar conteúdo
```bash
ls                          # Lista arquivos e pastas
ls -l                       # Lista detalhada (permissões, tamanho, data)
ls -lts                     # Ordena do mais antigo ao mais recente
```

# 📁 Manipulação de Arquivos e Diretórios
### 🔸 touch – Criar arquivos
```bash
touch arquivo.txt           # Cria um novo arquivo vazio
touch --help                # Exibe ajuda sobre o comando
```

### 🔸 mkdir – Criar diretórios
```bash
mkdir nova_pasta                    # Cria um diretório
mkdir -p pasta1/pasta2/pasta3       # Cria estrutura de diretórios em sequência
```
### 🔸 rm – Remover arquivos e diretórios
```bash
rm arquivo.txt              # Remove arquivo
rm -r pasta/                # Remove diretório (recursivamente)
rm -f arquivo.txt           # Força a remoção sem mensagens de erro
```

# 🧾 Exibição de Conteúdo
### 🔸 echo – Mostrar mensagens
```bash
echo "Olá Mundo"            # Exibe a mensagem
echo -n "Olá"               # Exibe sem quebra de linha
man echo                   # Abre o manual do comando
```

### 🔸 cat – Mostrar conteúdo de arquivos
```bash
cat arquivo.txt             # Mostra todo o conteúdo
cat -b arquivo.txt          # Numera apenas linhas com texto
cat -n arquivo.txt          # Numera todas as linhas
cat -A arquivo.txt          # Mostra caracteres especiais (como tabulações)
```

### 🔸 tac – Mostrar conteúdo invertido
```bash
tac arquivo.txt             # Mostra as linhas de baixo para cima
```

###🔸 head – Primeiras linhas
```bash
head -n5 arquivo.txt        # Mostra as 5 primeiras linhas
head -c10 arquivo.txt       # Mostra os 10 primeiros caracteres
```

### 🔸 tail – Últimas linhas
```bash
tail -n5 arquivo.txt        # Mostra as 5 últimas linhas
tail -n10 arquivo.txt       # Mostra as 10 últimas linhas
```

# 🔢 Contagem de Elementos
###🔸 wc – Word Count
```bash
wc arquivo.txt              # Mostra linhas, palavras e bytes
wc -l arquivo.txt           # Mostra apenas número de linhas
wc -w arquivo.txt           # Mostra apenas número de palavras
wc -c arquivo.txt           # Mostra apenas número de bytes

# Exemplo:
wc -l alunos*               # Conta as linhas de todos os arquivos que começam com "alunos"
```

# 🗂️ Ordenação e Filtros
###🔸 sort – Ordenar linhas
```bash
sort arquivo.txt            # Ordena em ordem alfabética
sort -r arquivo.txt         # Ordem reversa
sort -k2 -t":" arquivo.txt  # Ordena pelo 2º campo, separando por “:”
sort -k3 -t":" -g           # Ordena pelo 3º campo, como número
```

###🔸 uniq – Remover duplicatas
```bash
sort arquivo.txt | uniq     # Remove linhas repetidas em sequência
uniq -u arquivo.txt         # Mostra apenas linhas únicas
uniq -d arquivo.txt         # Mostra apenas linhas duplicadas
uniq -c arquivo.txt         # Conta repetições das linhas
```

# 🛠️ Utilitários Extras
###🔸 whatis – Descrição rápida do comando
```bash
whatis ls                   # Mostra o que o comando faz
```

###🔸 tr – Substituir ou remover caracteres
```bash
echo "abc" | tr a-z A-Z         # Transforma em maiúsculas
cat arquivo.txt | tr -d aei     # Remove vogais específicas
echo "shell" | tr l L           # Substitui ‘l’ por ‘L’
echo "shell" | tr -s l          # Suprime letras repetidas
```

# ✂️ Seleção de Campos
###🔸 cut – Cortar partes de linhas
```bash
cut -c1-3 arquivo.txt           # Mostra os 3 primeiros caracteres de cada linha
cut -c6- arquivo.txt            # Mostra a partir do caractere 6
cut -d" " -f1,3 arquivo.txt     # Mostra os campos 1 e 3, separados por espaço
```

#🔍 Comparação de Conteúdo
###🔸 diff – Comparar arquivos ou diretórios
```bash
diff arq1.txt arq2.txt          # Compara dois arquivos
diff -r pasta1/ pasta2/         # Compara diretórios recursivamente
```

# ✅ Dicas Finais
- Sempre combine comandos com pipes | para criar soluções mais poderosas.
- Use --help e man comando para explorar mais opções.
- Pratique cada comando com arquivos reais para entender seu comportamento.
