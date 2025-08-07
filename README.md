# Proyecto Ansible - Instalación de JDK, Apache Tomcat y MySQL

Este proyecto tiene como objetivo demostrar la automatización de la instalación y configuración de tres componentes clave en un entorno Linux (Debian/Ubuntu) utilizando Ansible:

- OpenJDK 17
- Apache Tomcat 10
- MySQL Server 5.7 o superior

## 📁 Estructura del proyecto

├── ansible.cfg
├── inventory/
│ └── hosts.yml
├── group_vars/
│ └── all.yml
├── playbooks/
│ ├── site.yml
│ ├── install-jdk.yml
│ ├── install-tomcat.yml
│ └── install-mysql.yml
└── templates/
└── tomcat.service.j2

Las variables necesarias se definen en `group_vars/all.yml`:

```yaml
tomcat_user: tomcat
tomcat_version: "10.1.24"
tomcat_install_dir: /opt/tomcat
jdk_package: openjdk-17-jdk
mysql_root_password: "Password123"
