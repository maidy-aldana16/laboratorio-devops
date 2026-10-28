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

## Publicación

1. Subir estos archivos a la rama `main`.
2. En GitHub: **Settings > Pages > Build and deployment > Source > GitHub Actions**.
3. Revisar la pestaña **Actions**, workflow **Laboratorio CI-CD**, trabajos `validar` y `publicar`.
4. Cuando el despliegue se complete, acceder a: `https://maidy-aldana16.github.io/laboratorio-devops/`.

**Nota:** el enlace anterior es la ruta prevista de Pages y solo funcionará cuando GitHub confirme la publicación.

## Prueba de fallo y recuperación

En `site/index.html`, cambia temporalmente el único `<h1>` que contiene la frase `Laboratorio DevOps` por `Sitio de prueba`, realiza un commit y observa el fallo de `validar`. Devuelve el texto original, confirma un nuevo commit y verifica la recuperación del workflow. Mantén capturas auténticas del fallo y de la ejecución exitosa para el informe.

## Diferencia entre Docker y Pages

Docker construye y comprueba una imagen Nginx dentro de GitHub Actions. **GitHub Pages sirve los archivos de `site/` como sitio estático**, no mantiene ejecutándose el contenedor.
