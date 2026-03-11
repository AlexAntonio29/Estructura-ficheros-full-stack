FROM nginx:alpine

# Carpeta donde Nginx sirve archivos estáticos por defecto
WORKDIR /usr/share/nginx/html

# Copia tus archivos estáticos (HTML, CSS, JS) ya construidos
COPY src ./ 

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
