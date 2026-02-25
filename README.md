# Laboratorio de Consola Cisco

Apuntes de configuración y resolución de problemas en dispositivos Cisco usando Ubuntu y Packet Tracer.

---

## 📌 Descripción

Este repositorio contiene comandos, configuraciones básicas y soluciones a problemas comunes al trabajar con dispositivos Cisco mediante conexión por consola en Ubuntu y simulaciones en Cisco Packet Tracer.

---

## 🖥 Entorno de Trabajo

- Ubuntu Linux
- Cisco Packet Tracer
- Cable de consola (USB a Serial)
- Herramientas de terminal: `screen` o `minicom`

---

## 🔌 Conexión por Consola en Ubuntu

### 1️⃣ Identificar el puerto serial

```bash
ls /dev/ttyUSB*
2️⃣ Conectarse usando screen
sudo screen /dev/ttyUSB0 9600
3️⃣ Conectarse usando minicom
sudo minicom -s

Configuración típica de consola:

Velocidad (Baud Rate): 9600

Bits de datos: 8

Paridad: Ninguna

Bits de parada: 1

Control de flujo: Ninguno

⚙️ Comandos Básicos en Cisco

Entrar a modo privilegiado:

enable

Entrar a modo de configuración global:

configure terminal

Ver configuración actual:

show running-config

Guardar configuración:

write memory
🚨 Problemas Comunes
Aparición de ####### o caracteres extraños

🔎 Causa: Velocidad incorrecta (baud rate mal configurado).

✅ Solución:
Verificar que esté configurado en 9600 tanto en:

Packet Tracer → Config → Console → Baud Rate

Terminal en Ubuntu (screen o minicom)
