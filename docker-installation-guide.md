
# Guía de Instalación de Docker en Ubuntu Server (usuario: osboxes)

## 1. Actualizar el sistema

```bash
sudo apt update
sudo apt upgrade -y
```

## 2. Instalar paquetes necesarios para repositorios HTTPS

```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
```

## 3. Agregar la clave GPG oficial de Docker

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

## 4. Agregar el repositorio de Docker

```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

## 5. Actualizar la lista de paquetes

```bash
sudo apt update
```

## 6. Instalar Docker Engine y containerd

```bash
sudo apt install docker-ce docker-ce-cli containerd.io -y
```

## 7. Habilitar y arrancar el servicio Docker

```bash
sudo systemctl enable docker
sudo systemctl start docker
```

## 8. (Opcional) Usar Docker sin necesidad de sudo

Agregar el usuario `osboxes` al grupo `docker`:

```bash
sudo usermod -aG docker osboxes
```

> Luego debes cerrar sesión y volver a iniciar sesión para aplicar los cambios de grupo.

## 9. Verificar que Docker está instalado correctamente

Mostrar la versión de Docker:

```bash
docker --version
```

Probar que Docker corre correctamente:

```bash
docker run hello-world
```

## 10. Verificar que el usuario pertenece al grupo docker

```bash
groups
```

Deberías ver `docker` listado entre tus grupos.

---

**¡Docker estará listo para usar en tu servidor Ubuntu!**
