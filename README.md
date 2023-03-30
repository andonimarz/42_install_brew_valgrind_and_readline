# Instalar valgrind en 42 Urduliz

Crear nuestra carpeta personal en la red e instalar valgrind

## Pasos para instalar valgrind

*Es recomendable cerrar la terminal en cada paso para que se añadan los comandos nuevos.

1 En 42urduliz_global_announcements vamos al 3 de agosto al mensaje de Steamo sobre “sgoinfre”. Se explica como crear el espacio en red. Creamos en la ruta “/sgoinfre/goinfre/Perso/“ nuestra carpeta haciendo “mkdir (nuestro login)” y cambiamos los permisos -> chmod 700.

---- Añadimos el canal tools_bots---- 

2 Para instalar brew.
Copiamos el código 

      rm -rf $HOME/.brew && git clone --depth=1 https://github.com/Homebrew/brew $HOME/.brew && echo 'export PATH=$HOME/.brew/bin:$PATH' >> $HOME/.zshrc && source $HOME/.zshrc && brew update


3 Una vez instalado, volvemos al mensaje de Steamo y vamos al enlace de Github 

      https://github.com/docgloucester/42homebrew_sgoinfre

Ejecutamos el comando 

      curl -fsSL https://raw.githubusercontent.com/docgloucester/42homebrew_sgoinfre/master/install.sh | zsh

Esto mueve home-brew de tu usuario local a la carpeta de sgoinfre.

4 Usamos estos 2 comandos juntos para instalar valgrind:

      brew tap LouisBrunner/valgrind
      brew install --HEAD LouisBrunner/valgrind/valgrind

Para revisar los memory leaks de programas donde utilizamos malloc, usaremos el siguiente comando:

      $\valgrind ./ejecutable “argumentos si hubiera”


5 Instalar readline para la minishell

      brew install readline

Para limpiar el usuario
Nos ponemos en la carpeta raíz del usuario y creamos el archivo: "touch .reset"
Reiniciamos el ordenador y empezará de 0.

# Instalar coreutils

Para la corrección de cpp9 se necesita 'shuf'. Para instalarlo usar el siguiente comando:

    brew install coreutils
    
Después de instalarse hay que cerrar el terminal y volver a abrirlo.
