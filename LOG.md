# Log

## Decisiones

| Fecha | Quién | Decisión | Motivo |
|---|---|---|---|
| 2026-11-22 | Grupo | Juego base: clon de Ansh Singh (MIT) en `GD_Clon/` | Acceso al estado interno, simple, niveles en `.json` |
| 2026-11-22 | Dani | `pygame-ce` en lugar de `pygame` | `pygame` 2.6.1 no compila en Python reciente |
| 2026-11-22 | Dani | Incluir clustering de estados (aprendizaje no supervisado) | Cubrir el apartado no supervisado de la propuesta; método concreto por decidir (k-means y jerárquico están en el temario); se comparará con la discretización simple |
| 2026-11-22 | Grupo | Descartar de momento redes neuronales y visión por computador | El estado interno ya está disponible; se retomarán solo si sobra tiempo |

## Datos del entorno (juego original)

- Ventana 1000×520, 60 FPS, suelo en y=420. Jugador 40×40 en x=120.
- Gravedad 1.0 y velocidad de salto −18. Velocidad del nivel fija: 5 px/frame.
- Salto: altura máxima ≈153 px, ≈35 frames en el aire, ≈175 px recorridos.
- Margen de timing para un obstáculo 40×40: ≈14 frames (≈70 px).
- Bloques y pinchos colisionan igual (rectángulo completo).
- Nivel 1: 10 obstáculos 40×40 separados 300–400 px, ≈800 frames. Hay 2 niveles, muy parecidos.
- Tras el último obstáculo del `.json` se generan obstáculos aleatorios sin semilla.
- No existe condición de victoria en el código original.

## Cambios en el código

| Fecha | Quién | Archivo | Cambio |
|---|---|---|---|
| 2026-11-22 | Dani | `GD_Clon/requirements.txt` | `pygame-ce`, `numpy`, `matplotlib` |
| 2026-11-22 | Dani | `LOG.md` | Añadido LOG para guardar cambios y decisiones |
| 2026-11-22 | Dani | `SETUP.md` | Añadido SETUP con instrucciones para empezar |

## Experimentos

| Fecha | Quién | Nivel | α | γ | λ | ε | Episodios | Semilla | Representación del estado | Resultado |
|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | |

## Problemas y soluciones

| Problema | Solución |
|---|---|
| PowerShell bloquea `activate` | `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` |
| `pip install pygame` falla al compilar | Usar `pygame-ce` |

## Pendiente

- Decidir método de trabajo del grupo (ramas y pull requests).
- Decidir variante de SARSA(λ) y representación del estado.