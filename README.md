# Simple-Shell

## Descripcion
Este proyecto consiste en la creacion de una shell simple, capaz de leer entradas de usuario, interpretar comandos y ejecutarlos en un entorno UNIX. El objetivo es replicar algunas de las funcionalidades basicas de una shell utilizando llamadas al sistema de C estandar.

-----------------------------

## Característics

- Modo interactivo y no interactivo
- Ejecución de comandos con argumento
- Comandos internos (built-ins):
  - `exit`: Cierra la shell
  - `env`: Muestra las variables de entorno
  - `cd`: Cambia el directorio de trabajo
- Manejo de rutas con la variable `PATH`
- Manejo básico de errore
- Cumple con la norma **Betty**

-----------------------------

##  Conceptos aprendidos

- Cómo funciona una shel
- Manejo de procesos con `fork`, `execve`, `wait`
- Lectura de entrada con `getline`
- Manejo de cadenas y arrays en C
- Manejo de memoria dinámia
- Manejo de errores y señals
- Programación modular enC

-----------------------------

## Requisitos

- Compilar con: `gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh`
- Ejecutable: `./hsh`
- Sistema operativo: Ubuntu LTS (Linux)

-----------------------------

## Estructura del proyecto

_strcmp.c
#funcion personalizada para comparar cadenas

shell.h
# Header principal

shell_loop.c
# Bucle principal de la shell
# Comando interno "exit"

prompt.c
# Muestra el prompt al usuario

tokenize.c
# Separa el input en comandos

execute.c
# Ejecuta los comandos

print_env.c
# Comando interno "env"

print_cd.c
# Comando interno "cd"

find_command_in_path.c
# Busca el comando en el PATH

README.md
# Este archivo

man_1_simple_shell
# Pagina de manual para la shell

-----------------------------

###Uso

## Modo interactivo

$ ./hsh
$ ls -l
$ pwd
$ cd ..
$ env
$ exit

-----------------------------

Modo no interactivo
$ echo "ls -l" | ./hsh

-----------------------------

Compilacion

Compila todos los archivos .c con:
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

------------------------------

###Author [Ezequiel Juvencio]� - GitHub EzequielH

------------------------------

##Recursos

UNIX Programming Concepts

- man execve

- man fork

- man getline

- man strtok

-----------------------------

###Proyecto desarrollado como parte del programa Holberton School.
