# ZequeOptimizador — Releases oficiales

Repositorio público de descargas de **ZequeOptimizador**. Acá se publican únicamente los binarios y las notas de versión; el código fuente se mantiene en un repositorio privado.

## Descargar

Andá a **[Releases](../../releases/latest)** y bajá `ZequeOptimizador.exe`.

No hace falta instalar nada más: es un ejecutable **portable y self-contained** (no requiere .NET aparte). Al descargarlo y usarlo aceptás el [EULA](EULA.md).

## Qué es

Aplicación de escritorio para Windows que:

- Analiza el equipo: CPU, GPU, RAM, versión de Windows, Secure Boot, TPM, VBS/HVCI, HAGS, MPO, Game Mode, plan de energía y anticheats instalados.
- Explica qué hace cada tweak: riesgo, evidencia, qué modifica, qué puede romper, reversión y fuentes.
- Aplica solo los cambios que elegís, con **punto de restauración**, verificación posterior y **reversión**.
- Incluye una capa de recomendaciones para Ryzen y Radeon (chipset, EXPO/DOCP, SAM/ReBAR, FreeSync, PBO, Adrenalin, shader cache, undervolt y VRR) como guía verificable. **No** aplica BIOS, overclock ni undervolt.

## Requisitos

- Windows 10 2004 o superior, o Windows 11, **x64**.
- 200 MB libres para el ejecutable y los respaldos.
- **Administrador** para aplicar cambios (la app lo pide sola).
- **Protección del sistema** activada para poder crear el punto de restauración.

## Primer inicio

1. Ejecutá `ZequeOptimizador.exe`.
2. El .exe **no está firmado digitalmente**, así que SmartScreen puede advertir. Elegí **Más información → Ejecutar de todas formas**.
3. Aceptá la pantalla de bienvenida y pulsá **Analizar equipo**.
4. Marcá los tweaks y pulsá **Revisar y aplicar seleccionados**. La app muestra el valor actual, el nuevo, la reversión y si requiere reiniciar.

## Perfiles

| Perfil | Items | Qué incluye |
|---|---:|---|
| **Seguro** | 19 | Base verificada. No desinstala ni toca Windows Update/Defender. |
| **Estándar** | 34 | Suma el preset Standard de winutil y telemetría segura. |
| **Avanzado** | 51 | Suma 17 apps reversibles de la whitelist. |
| **Extremo** | 90 (88 seleccionables) | Suma Windows Update/Defender, bloque de 139 servicios, bloques agresivos, apps y funciones de accesibilidad. **Irreversible en varios puntos.** |

**Extremo** es irreversible en varios puntos. Usalo bajo tu responsabilidad; si querés probarlo con una red de seguridad, se recomienda una **VM con snapshot**.

## Reseñas y promoción

Se permite mostrar, reseñar y promocionar el Software en videos, streams, artículos y redes sociales, incluso en canales monetizados, siempre que se enlace a la descarga oficial y no se rehostee ni redistribuya el `.exe`. No se debe sugerir que el Software es propio del canal. Para permisos especiales, contactá a **ZequeOficial**.

## Verificación del binario

| Dato | Valor |
|---|---|
| SHA-256 | `7951B9B6354A574F7631FB7C80BBFBC5BCBC1B2686142853157C48A0C912C904` |
| Tamaño | `62.808.577` bytes |

Para verificarlo en PowerShell:

```powershell
Get-FileHash .\ZequeOptimizador.exe -Algorithm SHA256
Get-Item .\ZequeOptimizador.exe | Select-Object Length
```

## Privacidad y seguridad

- La app **no envía telemetría ni abre conexiones propias a Internet**. Reparar o revertir apps puede usar **winget/Microsoft Store**, y eso sí requiere conexión.
- La base de conocimiento va embebida en el .exe.
- La importación de una base externa es opcional, requiere confirmación y pasa por validación de estructura, política de seguridad y catálogo auditado.
- Los cambios que apliques son responsabilidad tuya. Revisá siempre la vista previa y el punto de restauración.

## Desinstalar

Borrá `ZequeOptimizador.exe` y, si querés limpiar datos, la carpeta:

```
%LOCALAPPDATA%\ZequeOptimizador
```

## Aviso

Este software modifica configuración de Windows. Algunos cambios del perfil Extremo son irreversibles y pueden afectar Windows Update, Defender, aplicaciones y funciones de accesibilidad. Usalo bajo tu responsabilidad y con respaldo.

## Licencia

El uso del binario se rige por el [Acuerdo de Licencia de Usuario Final (EULA)](EULA.md); todos los derechos sobre el binario están reservados. El código fuente no se distribuye y su licencia es MIT. Los componentes de terceros y sus licencias se listan en [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md), incluido **Defender Remover v12.8.4** bajo **CC BY-NC 4.0**.
