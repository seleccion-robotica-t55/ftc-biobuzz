# Zero-Ohms E13 · Código FTC BIOBUZZ 2026-2027

Este repo es un fork del SDK oficial de FIRST (v12.0). **Solo se edita `TeamCode/`.**
El `README.md` de la raíz es el de FIRST: no lo modificamos para poder actualizar el SDK sin conflictos.

> Este repo es **público** (los forks de un repo público no pueden ser privados). No subas datos de alumnos, contraseñas ni información privada.

## Cómo abrirlo

1. `git clone https://github.com/zero-ohms-e13/ftc-biobuzz.git`
2. Ábrelo en Android Studio **Narwhal 3 Feature Drop o más nuevo** y espera el **Gradle Sync**.
3. Conecta el Control Hub → **Run 'TeamCode'**.

## Estructura de TeamCode

```
TeamCode/src/main/java/org/firstinspires/ftc/teamcode/
├── teleop/        ← OpModes @TeleOp           (package ...teamcode.teleop)
├── autonomo/      ← OpModes @Autonomous       (package ...teamcode.autonomo)
├── subsistemas/   ← clases de mecanismos: Drivetrain, Intake, ... (sin @TeleOp)
└── util/          ← utilidades: filtros, PID, constantes
```

Cada archivo `.java` debe declarar el `package` de su carpeta. Por ejemplo, en `teleop/`:
`package org.firstinspires.ftc.teamcode.teleop;`

## Reglas del equipo

**Ramas**

- `master` es el código que **compila y funciona** en el robot.
- Para trabajar, crea una rama temporal: `hiram/drivetrain`, `ana/auton-azul`.
- Teleop y autónomo **no** van en ramas separadas: van en carpetas distintas dentro de la misma rama.
- Cuando funcione, abre un **Pull Request** a `master`. El capitán de programación lo revisa y lo une.

**Commits**

- Mensaje en español y descriptivo: `Agrega TeleOp de campeonato`, `Ajusta velocidad del intake`.
- No se aceptan mensajes como `jkkjj` o `Descripción de los cambios`.
- Nombres de clases con sentido y en PascalCase: `TeleOpPrincipal`, `AutoAzulIzquierda`. Nada de `csdcscs`.
- Antes de hacer commit: el proyecto compila (**Build → Make Project**).

**Actualizar el SDK**

Cuando FIRST publique una versión nueva: en GitHub, **Sync fork** en la página del repo. Como solo tocamos `TeamCode/`, no debe haber conflictos.
