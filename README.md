# Implementación de una Arquitectura Web de 3 Capas en AWS Academy

Proyecto desarrollado para la Evaluación Final Transversal de la asignatura **Soluciones Cloud**, cuyo objetivo fue diseñar e implementar una arquitectura web de tres capas utilizando servicios de Amazon Web Services (AWS Academy).

## Arquitectura Implementada

La solución fue construida utilizando los siguientes servicios:

- Amazon VPC
- Subredes públicas y privadas
- Internet Gateway
- Route Tables
- Security Groups
- Amazon EC2 (Amazon Linux 2023)
- Apache HTTP Server
- Launch Template
- Target Group
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)

La infraestructura fue distribuida en **dos Availability Zones**, permitiendo una mayor disponibilidad y tolerancia a fallos.

## Tecnologías Utilizadas

- AWS Academy Learner Lab
- Amazon EC2
- Amazon VPC
- Elastic Load Balancing (ALB)
- Auto Scaling
- Apache HTTP Server
- HTML5
- CSS3

## Estructura del Proyecto

```
ProyectoAWS/
│── index.html
│── README.md
```

## Funcionamiento

La aplicación consiste en un sitio web estático alojado en una instancia Amazon EC2 con Apache HTTP Server.

El tráfico HTTP es distribuido mediante un **Application Load Balancer**, mientras que el **Auto Scaling Group** administra automáticamente las instancias EC2 para mantener la disponibilidad del servicio.

## Arquitectura

La infraestructura implementada sigue el siguiente esquema:

```
                    Internet
                        │
                        ▼
          Application Load Balancer
                        │
                        ▼
                Auto Scaling Group
                 │              │
             EC2 (AZ1)      EC2 (AZ2)
                 │              │
          VPC con Subredes Públicas
                 │
     Subredes Privadas (Diseñadas para RDS)
```

## Mejoras Propuestas

Como parte del proyecto se propuso incorporar:

- Amazon RDS Multi-AZ para la capa de datos.
- Amazon S3 para almacenamiento de archivos estáticos.
- Amazon CloudFront (CDN) para optimizar la entrega de contenido y reducir la latencia.

Estas mejoras fueron documentadas en el informe técnico, aunque no fueron implementadas debido a las limitaciones del entorno AWS Academy Learner Lab.

## Autor

**Matias Vargas Bozza**

Ingeniería en Informática – Duoc UC

## Licencia

Proyecto desarrollado con fines exclusivamente académicos.
