# Sistema de Control de Personal - Skinet Internet

Plataforma web para control de asistencia, gestión de personal y registro de ventas.
Proyecto de residencia profesional, Instituto Tecnológico de Aguascalientes.

## Stack
- Frontend: React + Vite
- Backend: Node.js + Express
- Base de datos: MySQL 8.4 LTS
- ORM: Prisma 7

## Requisitos
- Node.js 26
- Git
- MySQL Server 8.4 LTS

## Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/TU_USUARIO/skinet-personal.git
   cd skinet-personal
   ```

2. Crear la base de datos en MySQL:
   ```sql
   CREATE DATABASE skinet_personal CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   CREATE USER 'skinet_user'@'localhost' IDENTIFIED BY 'TU_CONTRASEÑA';
   GRANT ALL PRIVILEGES ON skinet_personal.* TO 'skinet_user'@'localhost';
   FLUSH PRIVILEGES;
   ```

3. Backend:
   ```bash
   cd server
   npm install
   cp .env.example .env
   ```
   Edita `.env` con tus credenciales y luego:
   ```bash
   npx prisma generate
   npm run dev
   ```
   Verifica en `http://localhost:3000/api/health`

4. Frontend (en otra terminal):
   ```bash
   cd client
   npm install
   npm run dev
   ```

## Flujo de trabajo con Git
- `main`: versiones estables
- `develop`: integración
- `feature/nombre-de-la-tarea`: una rama por actividad, con Pull Request a `develop`
- Nunca subir `.env`

## Estructura
- `client/`: aplicación React
- `server/`: API REST y Prisma
- `docs/`: documentación y diagramas

## Equipo
- Estefania Sherlin González Jiménez
- Yessica Amairani Duran de Loera
- Jesús Alejandro Luna Delgado

Asesor interno: Yomira del Carmen Rosales Martínez
Asesor externo: Lic. Francisco Fermín Cruz López