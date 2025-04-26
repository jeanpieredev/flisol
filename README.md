
# 🚀 Guía Básica para Empezar con Ubuntu

Este tutorial te guiará paso a paso en tareas esenciales que todo usuario de Ubuntu debe dominar.

---

## 1. Información básica del sistema

Verifica en qué sistema operativo estás trabajando:

```bash
cat /etc/os-release
```

Verifica la versión del kernel:

```bash
uname -r
```

---

## 2. Comandos básicos de navegación en la terminal

Ver tu ubicación actual:

```bash
pwd
```

Listar archivos y carpetas:

```bash
ls
```

Entrar en una carpeta:

```bash
cd nombre_de_la_carpeta
```

Crear una nueva carpeta:

```bash
mkdir nueva_carpeta
```

Crear un archivo vacío:

```bash
touch archivo.txt
```

Copiar un archivo:

```bash
cp archivo.txt copia_archivo.txt
```

Mover o renombrar un archivo:

```bash
mv copia_archivo.txt archivo_nuevo.txt
```

Eliminar un archivo:

```bash
rm archivo_nuevo.txt
```

---

## 3. Gestión de permisos

Ver los permisos de archivos:

```bash
ls -l
```

Cambiar permisos de un archivo:

```bash
chmod 755 archivo.txt
```

Dar permiso de ejecución a un archivo:

```bash
chmod +x script.sh
```

Cambiar el grupo propietario de un archivo:

```bash
sudo chgrp nombre_grupo archivo.txt
```

---

## 4. Gestión de usuarios y grupos

⚠️ Estas acciones requieren permisos de administrador (sudo).

Ver tu usuario actual:

```bash
whoami
```

Ver los grupos a los que perteneces:

```bash
groups
```

Crear un nuevo usuario:

```bash
sudo adduser nuevo_usuario
```

Crear un nuevo grupo:

```bash
sudo groupadd nuevo_grupo
```

Agregar un usuario a un grupo:

```bash
sudo usermod -aG nuevo_grupo nuevo_usuario
```

---

## 5. Instalación de software

Actualizar la lista de paquetes:

```bash
sudo apt update
```

Actualizar los paquetes instalados:

```bash
sudo apt upgrade
```

Instalar nuevas herramientas:

```bash
sudo apt install git curl docker.io
```

---

## 6. Comandos de monitoreo del sistema

Ver uso de la memoria RAM:

```bash
free -h
```

Ver uso del disco:

```bash
df -h
```

Ver procesos activos (si tienes instalado `htop`):

```bash
htop
```

*(Si no tienes `htop`, puedes instalarlo con:)*

```bash
sudo apt install htop
```

---

## 7. Alias útiles

Crear un alias para listar archivos de forma detallada:

```bash
alias ll='ls -lah'
```

Hacer el alias permanente agregándolo a `.bashrc`:

```bash
echo "alias ll='ls -lah'" >> ~/.bashrc
source ~/.bashrc
```

---

# 🎯 ¡Listo!

Ahora ya tienes las bases para trabajar con comodidad en Ubuntu.
