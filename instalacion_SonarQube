# Tranformarnos en root (superusuario)
sudo su -

# Una vez somos root, configuramos algunas variables que hacen falta en la maquina
sysctl -w vm.max_map_count=262144
sysctl -w fs.file-max=65536
ulimit -n 65536
ulimit -u 4096

# Dejo de ser root
exit

# Descargar la imagen llamada                                                          SONARQUBE
#                                                                                         VVVV
# Crear un contenedor llamado MISONARQUBE
#                      VVVV                                        
# Cambiar el puerto en que se ejecuta sonarQUBE
#                                                                             VVVV                                        
docker run -d --name misonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 8080:9000 sonarqube:latest

# NOTA: El cmabio que hemos hecho en el puerto, es una restricción de AMAZON.
# AMAZON solo me deja ejecutar cosas en los puertos ++ 8080 ++ , 8081, 8082