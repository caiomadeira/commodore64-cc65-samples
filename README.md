<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/2/2c/Commodore_64_logo.png" width="400"></a></p>

<p align="center">
<a href="https://www.retroarch.com">Download Retroarch</a>
</p>

## Screenshots

<p align="center"><img src="https://raw.githubusercontent.com/caiomadeira/c64-c/main/assets/main-240213-144418.png" width="400" alt="Laravel Logo"></a></p>

<p align="center"><img src="https://raw.githubusercontent.com/caiomadeira/c64-c/main/assets/main.c-240213-144341.png" width="400" alt="Laravel Logo"></a></p>

<p align="center"><img src="https://raw.githubusercontent.com/caiomadeira/c64-c/main/assets/main.c-240213-144553.png" width="400" alt="Laravel Logo"></a></p>

## Sobre c64-C

Esse é um repositório de estudo com o intuito de explorar e demonstrar uma programação de baixo nível referente, primoridialmente, ao Commodore 64, mas válido para outros sistemas retros.

Usando a coletânia de header files cc65 ("/usr/share/cc65/include")

- [Referencia de funções(cc65.github.io)](https://cc65.github.io/doc/funcref.html).
- [c64 - Controle de Caracteres](https://www.c64-wiki.com/wiki/control_character).
- [Commodore 64 memory map](https://sta.c64.org/cbm64mem.html).


## Configuração de ambiente

Utilizando o VSCODE + extensão de C/C++ da Microsoft + WSL(Terminal Ubuntu), no arquivo de configuração: *c_cpp_properties.json*

```
{
    "configurations": [
        {
            "name": "Linux",
            "includePath": [
                "${workspaceFolder}/**",
                "/usr/share/cc65/include"
            ],
            "defines": [],
            "compilerPath": "/usr/bin/clang",
            "cStandard": "c17",
            "cppStandard": "c++14",
            "intelliSenseMode": "linux-clang-x64"
        }
    ],
    "version": 4
}

```

## Compilando e executando o código

Para compilar o código .c rode o comando

```
cl65 nome_do_arquivo.c -o nome_do_arquivo.c.prg
```

Você pode usar um emulador (como o Retroarch com o núcleo do C64 Vice) para rodar o arquivo ```.prg```

## Gerando cc65 assembly language file
Gerar um arquivo assembly a partir do código em C ajuda a entender como converte-lo. O codigo original em C permanece comentado junto com o em assembly.

```
cl65 -S -T nome_do_arquivo.c -o nome_do_arquivo.prg
```

## Lista de plataformas suportadas pelo cc65

```
cl65 --list-targets
```

```

atari
atari2600
atari5200
atarixl
vic20
c16
c64
c128
plus4
cbm510
cbm610
osic1p
pet
bbc
apple2
apple2enh
geos-cbm
creativision
geos-apple
lunix
atmos
telestrat
nes
supervision
lynx
sim6502
sim65c02
pce
gamate
c65
cx16
```


### Autor

- **[Caio Madeira](https://caiomaidera.dev)**