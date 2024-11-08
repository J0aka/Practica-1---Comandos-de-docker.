# Práctica 1: Comandos de Docker e Git

## Introdución
Nesta práctica traballaremos con Docker e Git dende o terminal, clonando un repositorio, creando ficheiros
## Procedemento
### 1. Crear e clonar o repositorio
1. **Crear o repositorio** en GitHub co nome `Practica 1 - Comandos de docker`.
2. **Clonar o repositorio** no equipo:
```bash
git clone https://github.com/J0aka/Practica-1-Comandos-de-docker.git
cd Practica-1-Comandos-de-docker
```
### 2. Crear o ficheiro `readme2.md`
1. Crear `readme2.md` cunha mensaxe:
```bash
echo "Esta é unha proba de creación de ficheiro readme2.md." > readme2.md
```
### 3. Crear o ficheiro `readme.md` con comandos Docker
1. Crear e editar `readme.md` cos pasos:
```bash
nano readme.md
```
2. Engadir contido para os comandos de Docker:
```markdown
### Comandos para Docker
1. Descargar imaxe Ubuntu
```bash
docker pull ubuntu
docker images
```
2. Crear contedor sen nome
```bash
docker run -d ubuntu
docker ps -a
```
3. Crear contedor co nome `u1`
```bash
docker run -d --name u1 ubuntu
docker exec -it u1 bash
```
4. IP e ping a google.com
```bash
docker exec u1 ip a
docker exec u1 ping google.com
```
5. Crear contedor `bono` e facer ping entre contedores
```bash
docker run -d --name bono ubuntu
docker exec -it bono ping u1
```
6. Ver contedores en segundo plano:
```bash
docker ps
```
7. Espazo en disco usado
```bash
docker system df
```
8. Ver RAM dos contedores
```bash
docker stats
```
### 4. Subir ficheiros ao repositorio
1. Engadir e confirmar ficheiros:
```bash
git add readme.md readme2.md
git commit -m "Engadir readme.md e readme2.md"
```
2. Subir os cambios:
```bash
git push origin main
```
3. Verificar diferenzas co remoto:
```bash
git fetch
git diff origin/main
```
---
