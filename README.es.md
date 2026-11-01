<p align="right">Idioma:&emsp;<a href="README.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

# Privacidad (`plugin-privacy`)

Registra una actividad de tratamiento: las categorías, la finalidad, quién decide y cuánto se conserva. No elige una base legal.

Las instrucciones están en inglés. El archivo que guarda el plugin sigue el idioma del pedido. Los archivos van en `adrenaline/privacy/`.

## /priv-processing

Las categorías y la finalidad. Un identificador que señale a una persona se queda afuera.

## /priv-roles

Quién decide la finalidad y quién trata para ellos, solo cuando la persona nombró a las partes.

## /priv-retention

Cuánto se conserva cada categoría. Un plazo que nadie dio queda en hueco.

## Ayuda

## /priv-help

El catálogo de este plugin. No escribe un archivo.

## Para quién es

Quien necesita el registro de una actividad que la persona describió. El control técnico queda en `plugin-security`. Este plugin no da asesoría legal y no copia el skill de seguridad.

## Qué incluye

Portable, para cualquier agente que siga [Agent Skills](https://agentskills.io/specification):

- `record-processing` registra la actividad, los roles y la conservación.

Cursor y Claude Code: los commands de arriba. En Cursor, `/priv-processing`. En Claude Code, `/plugin-privacy:priv-processing`.

Solo Cursor: las rules `output-folder`, `no-legal-basis`. Claude Code no carga rules. Las mismas restricciones están en los skills.

## Instalar

En Cursor, instala el plugin desde este repositorio en Customize.

En Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-privacy
claude plugin install plugin-privacy@plugin-privacy
```

Para probar una copia local, arranca Claude Code con `claude --plugin-dir <ruta de este repositorio>`.

## Ejemplo

Pide `/priv-processing` y describe la actividad. El archivo lista solo las categorías que nombraste. El título de base legal queda en hueco.

## Configuración

Los archivos van en `adrenaline/privacy/`. Una actividad nombrada va en `<subject>/`.

## Licencia

MIT. Copyright (c) 2026 Ricardo Plascencia.

