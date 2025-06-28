
# 📘 Documentación técnica - IA Narrativa Libre

## 🧠 Descripción general

Este documento expande la idea original del sistema de IA narrativa adaptativa publicada como "prior art". Su objetivo es impedir que cualquier corporación o entidad registre una patente sobre este enfoque. Toda la información aquí contenida es de dominio público y puede ser utilizada, modificada o implementada libremente.

---

## ⚙️ Componentes del sistema

### 1. Entidad IA Compañera

* Puede tomar cualquier forma: robot, animal, dron, voz, etc.
* Recuerda eventos importantes de la historia del jugador.
* Evalúa las decisiones morales (acciones buenas o malas) y las consecuencias físicas (heridas, pérdidas).

### 2. Memoria dinámica del jugador

* Estado físico: pérdida de extremidades, heridas, fatiga, enfermedades.
* Estado moral: robos, asesinatos, decisiones diplomáticas.
* Estas memorias alteran el comportamiento de la IA y de los NPCs.

### 3. Análisis de terreno y entorno

* La IA analiza en tiempo real:

  * Coberturas disponibles.
  * Enemigos visibles.
  * Rutas de escape.
  * Obstáculos físicos.

### 4. Generación de sugerencias

* Basado en análisis de entorno y estado del jugador.
* Frases como:

  * “Estás sangrando mucho. No resistas más, déjame ayudarte.”
  * “Podríamos flanquearlos por la izquierda.”
  * “Con tu brazo roto, no puedes escalar. Debemos encontrar otra ruta.”

### 5. Transferencia narrativa

* Si el jugador está gravemente herido, la IA o un NPC puede ofrecerse a continuar la misión.
* La historia se adapta al cambio:

  * “Luis cayó en combate. Ahora tú lideras.”

### 6. Reacciones sociales adaptativas

* NPCs ofrecen ayuda si el jugador está débil.
* Algunos personajes desconfían si el jugador ha hecho daño antes.
* Otros se sienten inspirados si el jugador ha sido valiente o justo.

---

## 💬 Ejemplo de estructura de datos (JSON simplificado)

```json
{
  "player_state": {
    "health": 45,
    "left_arm": "missing",
    "reputation": "neutral",
    "decisions": ["helped_child", "stole_weapon"]
  },
  "environment": {
    "enemy_count": 3,
    "cover_available": true,
    "escape_route": "rooftop"
  },
  "ai_suggestion": "Luis, estás herido. Si subimos al tejado, podrías descansar mientras yo cubro la salida."
}
```

---

## 🔁 Pseudocódigo base para IA

```python
def generate_ai_response(player, environment):
    if player.health < 30 and 'left_arm' in player.lost_limbs:
        if environment.escape_route:
            return "No estás en condiciones, sube al escape y yo te cubro."
        else:
            return "Aguanta como puedas, buscaré una ruta alternativa."
    elif 'killed_villager' in player.decisions:
        return "No confío del todo en ti, pero no tenemos otra opción."
    else:
        return "Avancemos juntos, flanqueemos por la izquierda."
```

---

## 📜 Licencia y uso libre

Este proyecto se encuentra en **dominio público** bajo licencia **CC0** y **MIT**. Puedes copiar, adaptar, comercializar o incluirlo en tus proyectos, pero **no puedes registrarlo como patente** ni reclamar propiedad exclusiva sobre estos conceptos.

---

## 📅 Fecha de publicación como Prior Art

28 de junio de 2025

## 👥 Creado por

**juan alexander medina** y desarrolladores libres.

---

