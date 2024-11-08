# Seguridad-y-Autenticacion-con-JWT

Como en prácticas pasadas, iniciamos el contenedor de docker de nginx y entramos a su terminal interactiva

Vamos al directorio de nuestro proyecto y activamos el venv
```bash
cd home/fire/
source firesenv/bin/activate
```

Instalar el paquete flask-jwt-extended para el manejo de JWT:
```bash
pip install flask-jwt-extended
```
Instalar bcrypt para el manejo seguro de contraseñas:
```bash
pip install bcrypt
```
Creamos un nuevo archivo python
```bash
vim app.py
```
Agregamos el codigo de: https://flask-jwt-extended.readthedocs.io/en/stable/refreshing_tokens.html


Vamos a
```bash
cd /etc/nginx/conf.d/
```
Y editamos
```bash
vim default.conf
```
Agregamos las rutas proxy_pass para las nuevas rutas: /register, /login, /protected, /refresh


Guardamos los cambios y luego reiniciamos nginx
```bash
nginx -s reload
```

Corremos la app con flask


<img width="801" alt="Screenshot 2024-11-07 at 7 13 03 PM" src="https://github.com/user-attachments/assets/9206a1e2-06d7-40a6-ab37-2b451684dd0a">



Vamos a postman


/register
![Screenshot 2024-11-07 at 7 08 27 PM](https://github.com/user-attachments/assets/4ec27c02-9e72-43e7-bc10-ce087b2dcf07)


/login
![Screenshot 2024-11-07 at 7 09 37 PM](https://github.com/user-attachments/assets/6875a7c7-d8ff-4e6c-b877-e7e4302dd33b)


/protected
![Screenshot 2024-11-07 at 7 10 46 PM](https://github.com/user-attachments/assets/2503e821-9d69-45e1-8353-e8a12d5e891f)


/refresh
![Screenshot 2024-11-07 at 7 11 44 PM](https://github.com/user-attachments/assets/4c22e3f2-3c94-483c-bc9f-332ce536fe38)

