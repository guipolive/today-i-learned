# arquivos

# biblioteca [os](https://docs.python.org/3/library/os.html#module-os): Miscellaneous operating system interfaces

- `os.listdir(path)`
    - lista todos os arquivos e pastas de um diretório
    - pode ser usado para percorrer depois e fazer algo com cada elemento encontrado
- `os.remove(path)`
    - remove um arquivo único
    - não pode ser usado para remover pastas
- `os.path(path)`
    - traz alguns recursos que podemos usar com um pathname
        - .: os.path.isfile(path)
            - retorna True se o elemento for um file
        - .: os.path.isdir(path)
            - retorna True se o elemento for um diretório

# biblioteca [shutil](https://docs.python.org/3/library/shutil.html#module-shutil): High-level file operations

- `shutil.rmtree(path)`
    - nos permite remover um diretório inteiro, podendo ignorar o fato de ele não estar vazio ( possuir elementos dentro )
- `shutil.move(from, to)`
    - nos permite mover um elemento de um lugar from para outro lugar to
- `shutil.unpack_archive(from, to)`
    - nos permite extrair elementos de um arquivo zip (ou outro formato) para um local específico

```python
## exemplo que fiz. Esse trecho de código deve excluir tudo de dentro da pasta
# 'til_dir', com exceção dos arquivos 'README.md' e '.git'

# deleting previous files
old_files = listdir(til_dir)

for f in old_files:
    if re.search('^README\.md$', f) == None and re.search('^\.git$', f) == None: # searching for 'README.md' or '.git' files
        if path.isfile(til_dir + '\\' + f):
            remove(til_dir + '\\' + f)
        elif path.isdir(til_dir + '\\' + f):
            shutil.rmtree(til_dir + '\\' + f)
```