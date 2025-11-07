ARG BUILD_FROM
FROM $BUILD_FROM

# Instala Node.js y npm
RUN apk add --no-cache nodejs npm

# Copia tu script de arranque y dale permisos
COPY run.sh /run.sh
RUN chmod a+x /run.sh

# Copia todos los archivos de tu carpeta scripts al contenedor
COPY scripts/ /data/scripts/
RUN ls -R /data/scripts

# Establece /data como directorio de trabajo
WORKDIR /data/scripts

# Comando de inicio
CMD [ "/run.sh" ]
