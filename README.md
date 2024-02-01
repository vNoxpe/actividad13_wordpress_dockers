# 1º.- DESINSTALACIÓN DE PAQUETES QUE PUEDEN ENTRAR EN CONFLICTO:

$ for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done


# 2º.- INSTALACIÓN USANDO UN REPOSITORIO
Existen diferentes maneras de instalación de docker. Vamos a utilizar la instalación utilizando el repositorio apt.

sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/92029c91-101a-4a2c-b4ae-5881cfa6febf)


sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/6f9c0806-8ffc-49e0-a736-7c40a1057df5)


echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/0f67b627-4ffd-4d27-b932-e275af635bcb)

# 3º.- INSTALACIÓN DEL MOTOR DE DOCKER

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/bf379e13-ba05-4304-a2a8-f5d1e5f40d5c)


## COMPROBACIÓN INSTALACIÓN DOCKER
docker version

- ![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/e308afa5-9c32-4072-a2aa-f100c61ffc1b)

docker run hello-world
- ![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/27d8d766-82e0-4cdf-a731-6b57444e50c9)


## INSTALACIÓN DOCKER-COMPOSE:
sudo apt install docker-compose-plugin
- ![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/3b99589f-5d43-4559-b61c-031872d9002b)

## COMPROBACIÓN INSTALACIÓN DOCKER-COMPOSE
docker compose version
-![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/38f2081c-7d4d-406c-98cf-86e47b305f5c)

# Clonamos el repositorio de gihub de la tarea:
![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/5c09c954-858c-495e-b21d-bf38021a1b98)

# Añdimos los ficheros config-compose.yml y .env y los modificamos:
fichero config-compose.yml
![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/bca85172-4a90-446b-adb7-3eff60def41e)
fichero .env
![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/90b05737-6e93-468e-ae3f-c7ca04898cb1)

# Ahora arracncamos DOCKER con:

![image](https://github.com/vNoxpe/actividad13_wordpress_dockers/assets/144890599/7cc4b7b9-077d-4bfb-b2ce-2d44e6f4e28f)
