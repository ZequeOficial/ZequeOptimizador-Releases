# Avisos de terceros

ZequeOptimizador incluye o deriva trabajo de los siguientes proyectos. Las licencias se reproducen completas cuando corresponde.

---

## winutil

- Proyecto: ChrisTitusTech/winutil
- Uso: la base de conocimiento se construyó a partir de `config/tweaks.json`, `config/feature.json` y `config/appx.json` del commit `2ef5e5dc7852634bc40ad789a3d1115ee3913c41`. Las rutas de registro, servicios, features y paquetes AppX provienen de ese repositorio.
- Licencia: MIT

```
MIT License

Copyright (c) 2022 CT Tech Group LLC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Defender Remover

- Proyecto: [ionuttbara/windows-defender-remover](https://github.com/ionuttbara/windows-defender-remover)
- Binario: `DefenderRemover.exe` v12.8.4, 842.994 bytes
- SHA-256: `C8DFEDFDB3EE6C5761AC119655D522850ABD84649E13D0BF55EFA8F0AD4F7FD7`
- Uso: embebido en el .exe y ejecutado a pedido desde **Herramientas**.
- Licencia: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- Licencia upstream: [LICENSE](https://github.com/ionuttbara/windows-defender-remover/blob/main/LICENSE)

---

## .NET 10 Runtime

- Proyecto: dotnet/runtime
- Uso: runtime autocontenido incluido en el .exe.
- Licencia: MIT
- https://github.com/dotnet/runtime/blob/main/LICENSE.TXT

---

## System.Management

- Paquete: System.Management 8.0.0
- Uso: consultas WMI/CIM para la detección de hardware.
- Licencia: MIT
- https://github.com/dotnet/runtime

---

## System.ServiceProcess.ServiceController

- Paquete: System.ServiceProcess.ServiceController 8.0.0
- Uso: lectura y control del estado de servicios de Windows.
- Licencia: MIT
- https://github.com/dotnet/runtime

---

## xUnit.net

- Paquetes: xunit 2.9.2, xunit.runner.visualstudio 2.8.2
- Uso: pruebas automatizadas (no se distribuye con el .exe).
- Licencia: Apache License 2.0
- https://github.com/xunit/xunit/blob/main/LICENSE

---

## Microsoft.NET.Test.Sdk

- Paquete: Microsoft.NET.Test.Sdk 17.11.1
- Uso: infraestructura de pruebas (no se distribuye con el .exe).
- Licencia: MIT
- https://github.com/microsoft/vstest

---

ZequeOptimizador incluye DefenderRemover.exe v12.8.4 bajo CC BY-NC 4.0. El resto de los binarios de terceros corresponden al runtime de .NET. La app no descarga código propio en tiempo de ejecución ni envía datos a servidores; reparar o revertir apps puede usar winget/Microsoft Store, que sí requieren conexión.
