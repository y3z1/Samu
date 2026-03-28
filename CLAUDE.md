# S.A.M.U. "The Comeback"
> Sistema de Apoyo y Misiones para Un objetivo

## Contexto del proyecto

App web personalizada para acompañar a Samuel Adarme Ramírez (15-16 años, 4º ESO, Reus) en la recta final del curso. Desarrollada por su padre Yezid en el marco del framework B.R.I.D.G.E.

**URL producción:** https://y3z1.github.io/Samu
**Repositorio:** https://github.com/y3z1/Samu
**Rama principal:** main

---

## Stack técnico

- **Frontend:** HTML + CSS + JS vanilla — un solo archivo `index.html`
- **Guía de estudio:** `guide.html` — archivo separado enlazado desde index
- **Base de datos:** Firebase Firestore (plan Spark gratuito, sincronización en tiempo real)
- **Hosting:** GitHub Pages
- **Notificaciones:** Telegram Bot API
- **Control de versiones:** Git + GitHub

---

## Credenciales Firebase

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyBlWN60XJPkiS4RlbXM8FKtZDsB1IuhAjs",
  authDomain: "samuel-missions.firebaseapp.com",
  projectId: "samuel-missions",
  storageBucket: "samuel-missions.firebasestorage.app",
  messagingSenderId: "17487135398",
  appId: "1:17487135398:web:543fdd0c25f8fdb5036a67"
};
```

**Colección Firestore:** `missions`
**Campos por documento:** id, title, desc, cat, xp, completed, completedBy, completedAt, order

---

## Credenciales Telegram

```
Bot token: 8561570694:AAGzbrAhBuhZBdcU62LuEH_BZcUxvtaa8ds
Chat ID grupo: -5254474979
Grupo: S.A.M.U "The Comeback"
```

**Notificaciones activas:**
- Misión completada (quién, XP, progreso)
- Nueva misión añadida
- Misión desmarcada
- Resumen semanal

**Pendiente añadir al grupo:** madre, Felipe, Samuel

---

## Estructura de archivos

```
S.A.M.U/
├── index.html        ← App principal con misiones y Firebase
├── guide.html        ← Intel Guide — guía de estudio por asignatura
├── CLAUDE.md         ← Este archivo
└── BRIDGE_system_prompt.md  ← Framework para otras familias
```

---

## Categorías de misiones

| Valor | Etiqueta | Color |
|-------|----------|-------|
| `profe` | Reto Profesores | Rojo |
| `general` | General | Gris |
| `mates` | Matemáticas | Naranja |
| `socials` | Ciencias Sociales | Cyan |
| `lengua` | Lengua | Amarillo |
| `ingles` | Inglés | Verde |
| `efisica` | Ed. Física | Púrpura |
| `social` | Desarrollo Social | Dorado |

---

## Perfil de Samuel (contexto para decisiones de diseño)

- TEA grado mínimo — prefiere claridad, estructura y sin ambigüedad
- Intereses: GTA V, Call of Duty, Rocket League
- Fortalezas: Inglés (AN), Música (AN), Latín (AS)
- Dificultades: Matemáticas, Ciencias Sociales, Ed. Física, Lengua (todas NA)
- Vida social principalmente online
- Comunicación verbal escasa — la app no debe ser intrusiva ni condescendiente
- El tono del contenido tiene que sonar a algo que él elegiría, nunca a programa de ayuda

---

## Estética visual

- Fondo: `#080a0f` (negro azulado profundo)
- Acento principal: `#00e5ff` (cyan)
- Acento secundario: `#39ff8a` (verde neón)
- Advertencia: `#ff6b35` (naranja)
- XP: `#ffd600` (amarillo dorado)
- Tipografías: Bebas Neue (títulos) + Share Tech Mono (etiquetas) + Rajdhani (cuerpo)
- Efecto de fondo: scanlines sutiles, radial gradients
- Referencia visual: gaming UI, terminal militar, HUD de videojuego

---

## Principios de desarrollo

1. **Un solo archivo** para index.html y guide.html — no separar CSS ni JS
2. **Sin frameworks** — vanilla JS únicamente
3. **Firebase primero** — toda modificación de misiones pasa por Firestore, nunca localStorage
4. **Telegram en cada acción** — completar, añadir y desmarcar misiones siempre notifica
5. **Mobile first** — Samuel puede usarlo desde el móvil
6. **Tono del contenido** — nunca condescendiente, siempre desde las fortalezas

---

## Comandos git habituales

```bash
# Ver estado
git status

# Subir cambios
git add .
git commit -m "descripción del cambio"
git push origin main

# GitHub Pages se actualiza automáticamente en 1-2 minutos tras el push
```

---

## Historial de versiones

| Versión | Fecha | Descripción |
|---------|-------|-------------|
| v1.0 | Marzo 2026 | Versión inicial — 26 misiones, Firebase, Telegram, Intel Guide |

---

## Pendientes conocidos

- [ ] Añadir madre, Felipe y Samuel al grupo de Telegram
- [ ] Presentar el proyecto a Samuel
- [ ] Seguimiento consulta psicóloga
- [ ] Seguimiento medicación (Fluoxetina abandonada desde dic 2025)
- [ ] Posible futura mejora: sincronización entre dispositivos del progreso de la Intel Guide

---

*Desarrollado con Claude Code v2.1.86 · Marzo 2026*
*Parte del framework B.R.I.D.G.E. — Building Real Interest-Driven Growth Experiences*
