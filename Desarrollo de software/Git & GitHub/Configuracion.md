---
banner_icon: ⚙️
banner: "![[gemini-vi_31191744012_o.jpg]]"
banner_y: 0.444
---

# Configuración inicial de Git 

1. Configuración del nombre:
	```bash
	git config --global user.name "Jorge Juarez"
	```

2. Configuración del correo electrónico:
	```bash
	git config --global user.email jorgeang33@gmail.com
	```

3. Configuración del editor de código (VS Code):
	```bash
	git config --global core.editor "code --wait"
	```

##### 4. Configuración de autocrlf (el formato de fin de línea):
+ Configuración en Windows:
	```bash
	git config --global core.autocrlf true
	```

+ Configuración en MacOS y Linux:
	```bash
	git config --global core.autocrlf input
	```

5. Configurar la autenticación: Si se va a trabajar con repositorios remotos y se necesita de autenticación, se puede configurar Git para que recuerde las credenciales.
	```bash
	git config --global credential.helper store
	```

Confirmación de la configuración inicial:
```bash
git config --global -e
```

Ayuda con la configuración inicial de git:
```bash
git config -h
```

## Configuración opcional del Git

Configurar alias para comandos frecuentemente utilizados o para abreviar comandos largos.
```bash
git config --global alias.st status
```

Así, podrías usar `git st` en lugar de `git status`.

Tener un `.gitignore` global
```bash
git config --global core.excludesfile [file]
```

Se utiliza para especificar un archivo global de exclusión en Git. Este archivo contiene patrones de nombres de archivos que Git debe ignorar de manera predeterminada en todos los repositorios de tu sistema.

Es importante destacar que `[file]` en el comando representa la ruta y el nombre de archivo que deseas utilizar como archivo global de exclusión. Puedes reemplazar `[file]` con la ruta y el nombre de archivo que desees, por ejemplo: `~/.gitignore_global`.
Recuerda que una vez configurado el archivo global de exclusión, debes asegurarte de que los archivos y patrones que deseas excluir estén especificados correctamente en ese archivo.