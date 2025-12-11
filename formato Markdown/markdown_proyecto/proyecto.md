# Documento de Soporte del Proyecto de Grado – ADSO
## Plataforma de Seguimiento de Instructores a Aprendices del SENA

# 1. Introducción

El presente documento describe el proyecto de grado del programa ADSO (Análisis y Desarrollo de Software) cuyo objetivo principal es diseñar e implementar una plataforma digital de seguimiento académico y formativo, permitiendo que los instructores del SENA realicen un control más eficiente sobre los avances, entregas, desempeño y alertas de los aprendices.

La solución busca optimizar el proceso actual, el cual suele ser manual, disperso y poco estandarizado. Mediante esta plataforma, el seguimiento será centralizado, rápido y accesible desde cualquier dispositivo.

#2. Descripción General del Proyecto

La plataforma se concibe como un sistema web responsivo, escalable y seguro. Estará orientado a mejorar la comunicación entre instructores y aprendices, así como a automatizar el registro de actividades formativas, evidencias, notas y alertas tempranas.

## 2.1 Problema a Resolver

Actualmente, los instructores realizan seguimiento usando herramientas distintas (Excel, WhatsApp, correos, Classroom, papel), lo que provoca:

Pérdida de información.

Procesos lentos y desorganizados.

Dificultad para centralizar evidencias.

Bajo control sobre actividades pendientes.

Falta de reportes automatizados.

## 2.2 Objetivo General

Desarrollar una plataforma web que permita el seguimiento integral del proceso formativo de los aprendices del SENA, facilitando el registro, monitoreo y retroalimentación de actividades por parte de los instructores.

## 2.3 Objetivos Específicos

Permitir que el instructor registre avances, notas y observaciones.

Facilitar al aprendiz visualizar en tiempo real su estado académico.

Centralizar evidencias y actividades formativas.

Automatizar reportes de desempeño y alertas tempranas.

Implementar roles diferenciados (Administrador, Instructor, Aprendiz).

# 3. Alcance del Proyecto

La primera versión del sistema incluye:

Módulo de autenticación por roles.

Gestión de fichas, programas e instructores.

Gestión de aprendices.

Registro de actividades formativas.

Subida de evidencias.

Seguimiento individual y grupal.

Reportes por trimestre, competencia y resultado de aprendizaje.

Notificaciones internas.

No incluye en esta versión:

Integración con SOFIAPlus.

Integración con correo institucional.

App móvil nativa (aunque será responsiva).

# 4. Actores del Sistema
## 4.1 Administrador

Gestiona usuarios.

Habilita fichas y programas.

Supervisa métricas generales.

## 4.2 Instructor

Gestiona actividades formativas.

Registra calificaciones.

Aprueba o rechaza evidencias.

Emite alertas y observaciones.

Genera reportes.

## 4.3 Aprendiz

Consulta actividades asignadas.

Carga evidencias.

Revisa notas y retroalimentación.

Ve su progreso por trimestre.

# 5. Requerimientos del Sistema
## 5.1 Requerimientos Funcionales

El sistema debe permitir el registro e inicio de sesión según rol.

El instructor debe poder crear actividades para su ficha.

El aprendiz debe poder cargar evidencias en distintos formatos.

El sistema debe guardar calificaciones y retroalimentación.

El administrador debe gestionar la información de usuarios.

Debe permitir generar reportes exportables.

Debe mostrar alertas y notificaciones.

## 5.2 Requerimientos No Funcionales

Seguridad: Cifrado de contraseñas y control por roles.

Rendimiento: Las vistas deben cargar en menos de 3 segundos.

Usabilidad: Interfaz intuitiva para usuarios no técnicos.

Escalabilidad: Capacidad para manejar múltiples fichas.

Disponibilidad: Operatividad 24/7.

# 6. Arquitectura Propuesta

Frontend: HTML, CSS, JavaScript, Vue.js / React.

Backend: Node.js o Java Spring Boot.

Base de Datos: MySQL o PostgreSQL.

Servicios Adicionales: API interna para módulos de reportes.

Infraestructura: Servidor cloud o contenedor Docker.

# 7. Modelo del Dominio
## 7.1 Entidades Principales

Usuario (ID, nombre, rol, correo, ficha asignada).

Ficha (número, programa, estado, trimestre).

Actividad (descripción, RA asociado, fecha límite, instructor).

Evidencia (archivo, aprendiz, actividad, estado).

Calificación (nota, observación, fecha).

Reporte (trimestre, aprendiz, desempeño).

# 8. Flujo Principal del Sistema (Resumen BPMN)
## 8.1 Proceso de Seguimiento del Instructor

Instructor inicia sesión.

Selecciona ficha.

Crea actividad.

Aprendiz entrega evidencia.

Instructor revisa.

Instructor califica.

Aprendiz visualiza su estado.

El sistema genera reportes automáticos.

## 8.2 Proceso del Aprendiz

Inicia sesión.

Consulta actividades.

Sube evidencia.

Revisa observaciones.

Monitorea su progreso.

# 9. Beneficios de la Plataforma

Mayor organización para instructores.

Reducción del uso de herramientas externas.

Mayor control y trazabilidad.

Transparencia del proceso formativo.

Acceso a información en tiempo real.

Mejor respuesta ante dificultades académicas.

# 10. Conclusión

La plataforma propuesta representa una solución moderna y eficiente para los desafíos actuales del seguimiento formativo en el SENA. Mediante su implementación, se logrará una experiencia más ordenada, rápida y estandarizada, fortaleciendo el proceso educativo y mejorando la comunicación entre instructores y aprendices.

