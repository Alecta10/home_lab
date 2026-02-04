# 🚀 home_lab
Configuración de DNS recursivo y bloqueo de publicidad en Raspberry Pi.

---

### 🛠️ Instalación y Configuración

Sigue estos pasos para desplegar **Pi-hole** y **Unbound** en tu red local.

#### 1. Preparar el sistema
Clona este repositorio en tu Raspberry Pi:
```Bash
git clone https://github.com/Alecta10/home_lab.git
cd TU_REPO
```
### 2. Descargar Root Hints
Unbound necesita conocer los servidores raíz del mundo para ser recursivo:
```Bash
wget https://www.internic.net/domain/named.root https://www.internic.net/domain/named.root -O ./docker-compose/unbound/root.hints
```
### 3. Configurar Variables
Copia el archivo de ejemplo y edita tu contraseña de administrador:

```Bash
cp .env.example .env
nano .env
```
### 4. Desplegar
Levanta los contenedores con Docker Compose:

```Bash
docker compose up -d
```
