Docker Compose en Docker Desktop para el repositorio: https://github.com/alexcayoja-sys/finance

Este paquete añade Dockerfiles y un archivo docker-compose.yml para ejecutar el backend de Django (Postgres) y el frontend de React existentes mediante Docker Desktop. - Postgres se ejecuta como servicio de base de datos
- El backend se ejecuta con Gunicorn en el puerto 8000
- El frontend se compila y se sirve mediante nginx en el puerto 3000 (host)

Cómo usar:
1. Copiar el contenido de esta carpeta en la raíz del repositorio clonado (junto a backend/ y frontend/)
2. Editar backend/.env con la clave SECRET_KEY real y la configuración si es necesario
3. Desde Docker Desktop o la terminal, ejecutar: docker compose up -d --build
4. Acceder al frontend en http://localhost:3000 y a la API del backend en http://localhost:8000

Notas:
- Los volúmenes están configurados para la persistencia de Postgres
- Ajustar el número de trabajadores y la configuración de producción según sea necesario
