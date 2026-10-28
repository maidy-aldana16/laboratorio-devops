# Laboratorio DevOps — Desarrollo Web

Universidad Mariano Gálvez de Guatemala · Ingeniería en Sistemas y Ciencias de la Computación

**Estudiante:** Maidy Obed Aldana Saquic  
**Carné:** 5090-23-10241  
**Fecha del laboratorio:** 26 de octubre de 2026

## Descripción

Práctica integrada de Docker, Kubernetes, GitHub Actions y CI/CD. Incluye una página web estática profesional, un Dockerfile basado en Nginx y un workflow que comprueba el contenido, construye y ejecuta una imagen Docker, realiza una prueba HTTP y despliega el sitio en GitHub Pages.

## Estructura

```text
laboratorio-devops/
├── README.md
├── Dockerfile
├── site/
│   └── index.html
└── .github/
    └── workflows/
        └── ci-cd.yml
```

## Diferencia entre Docker y Pages

Docker construye y comprueba una imagen Nginx dentro de GitHub Actions. **GitHub Pages sirve los archivos de `site/` como sitio estático**, no mantiene ejecutándose el contenedor.
