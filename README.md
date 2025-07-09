# WiFi WarDriver Automático

[![Windows](https://img.shields.io/badge/Windows-10%2F11-blue?logo=windows)](https://www.microsoft.com/windows)
[![C++](https://img.shields.io/badge/C%2B%2B-17-blue?logo=c%2B%2B)](https://isocpp.org/)
[![Visual Studio](https://img.shields.io/badge/Visual%20Studio-2022-purple?logo=visual-studio)](https://visualstudio.microsoft.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> 🚀 Sistema completo de wardriving automático para Windows con interfaz moderna, escaneo WiFi avanzado, geolocalización y exportación de datos.

## ✨ Características

- 🔍 **Escaneo WiFi Avanzado** - Detección automática usando Windows WLAN API
- 📍 **Geolocalización Inteligente** - IP pública + geocodificación inversa con OpenStreetMap
- 🖥️ **Información del Sistema** - Hardware, red y estado de servicios en tiempo real
- 📊 **Exportación Avanzada** - CSV + Mapas HTML interactivos con Leaflet.js
- 📈 **Estadísticas Detalladas** - Análisis visual con barras de progreso y rankings
- 🎨 **Interfaz ASCII Art** - Banner moderno y menú dinámico adaptativo
- ⚡ **Funcionalidades Avanzadas** - Escaneo continuo, filtros, manejo robusto de errores

## 🎯 Vista Previa

```
    _    _                        ___             __                           
   F L  J J     ___ _    _ ___   F __".   _ ___   LJ  _    _   ____     _ ___  
  J J .. L L   F __` L  J '__ ",J |--\ L J '__ ",    J |  | L F __ J   J '__ ",
  | |/  \| |  | |--| |  | |__|-J| |  J | | |__|-J FJ J J  F L| _____J  | |__|-J
  F   /\   J  F L__J J  F L  `-'F L__J | F L  `-'J  LJ\ \/ /FF L___--. F L  `-'
 J___//\\___LJ\____,__LJ__L    J______/FJ__L     J__L \\__//J\______/FJ__L     
 |___/  \___| J____,__F|__L    |______F |__L     |__|  \__/  J______F |__L     
                                                                               
                                    v1.0 - by Pecar                           

📡 ESTADO DEL SISTEMA:
├─ WiFi: ✅ Disponible
└─ GPS:  ✅ Disponible

🎯 OPCIONES DISPONIBLES:
├─ 1. 🔍 Escaneo único
├─ 2. 🔄 Escaneo continuo
├─ 3. 📋 Mostrar redes encontradas
├─ 4. 📊 Exportar a CSV
├─ 5. 🗺️  Generar mapa HTML
├─ 6. 📍 Mostrar información GPS
├─ 7. 🖥️  Información del sistema
├─ 8. 📈 Estadísticas de redes
└─ 9. 🚪 Salir
```

## 🚀 Instalación Rápida

### Prerrequisitos
- Windows 10/11 (x64)
- Visual Studio 2022 con C++ Desktop Development
- Adaptador WiFi compatible
- Conexión a internet

### Pasos
```bash
# 1. Clonar el repositorio
git clone https://github.com/tu-usuario/wifi-wardriver-automatico.git
cd wifi-wardriver-automatico

# 2. Abrir en Visual Studio 2022
# Abrir WiFi WarDriver Automático.sln

# 3. Compilar (Release x64)
# Ctrl+Shift+B

# 4. Ejecutar como administrador
# F5 o Ctrl+F5
```

## 📋 Uso

### Ejecución Inicial
```bash
# Ejecutar como administrador para mejor compatibilidad
WiFi WarDriver Automático.exe
```

### Opciones Principales

| Opción | Descripción | Ejemplo |
|--------|-------------|---------|
| 🔍 **Escaneo único** | Escaneo inmediato de redes WiFi | Detecta todas las redes cercanas |
| 🔄 **Escaneo continuo** | Escaneo automático con intervalos | `Duración: 300s, Intervalo: 30s` |
| 📊 **Exportar CSV** | Exportar datos a Excel | `wardriving_data/scan_2024.csv` |
| 🗺️ **Mapa HTML** | Mapa interactivo con OpenStreetMap | `wardriving_data/map.html` |
| 🖥️ **Info Sistema** | Información de hardware y red | IP pública, RAM, procesador |

## 📊 Estructura de Datos

### CSV Export
```csv
SSID,BSSID,Signal_Strength,Channel,Security_Type,Encryption_Type,Latitude,Longitude,Timestamp,Location_Name
"MiWiFi","AA:BB:CC:DD:EE:FF",-45,6,"WPA2","AES",40.4168,-3.7038,"2024-01-15 14:30:25","Calle Mayor, Madrid"
"RedAbierta","11:22:33:44:55:66",-67,11,"Open","None",40.4168,-3.7038,"2024-01-15 14:30:26","Plaza Mayor, Madrid"
```

### Mapa HTML
- **Marcadores coloridos** por intensidad de señal
- **Popups informativos** con detalles completos
- **Filtros dinámicos** por rango de señal
- **Visualización en tiempo real**

## 🛠️ APIs y Tecnologías

- **Windows WLAN API** - Escaneo WiFi nativo
- **WinHTTP** - Geolocalización y IP pública
- **Winsock2** - Información de red local
- **Windows System APIs** - Información del sistema
- **OpenStreetMap Nominatim** - Geocodificación inversa
- **Leaflet.js** - Mapas interactivos

## 📈 Estadísticas

### Análisis por Seguridad
```
🔒 POR TIPO DE SEGURIDAD:
├─ WPA2        : 45 (75.0%) ████████████████████
├─ WPA3        :  8 (13.3%) ████
├─ Open        :  5  (8.3%) ██
└─ WPA         :  2  (3.3%) █
```

### Top 5 Redes Más Fuertes
```
🏆 TOP 5 REDES MÁS FUERTES:
├─ 🥇 MiWiFi_5G           │ -32 dBm │ 🟢 Excelente │ WPA2
├─ 🥈 RedFuerte           │ -41 dBm │ 🟢 Excelente │ WPA3
├─ 🥉 WiFiRapido          │ -48 dBm │ 🟡 Buena     │ WPA2
├─ 🏅 RedEstable          │ -52 dBm │ 🟡 Buena     │ WPA2
└─ 🏅 RedConfiable        │ -58 dBm │ 🟡 Buena     │ WPA2
```

## 🔧 Configuración

### Personalizar Escaneo
```cpp
// En continuousScan()
this_thread::sleep_for(chrono::seconds(interval_seconds));

// Filtrar por intensidad
if (network.signal_strength > -80) {
    // Solo redes con señal fuerte
}
```

### Integrar GPS Real
```cpp
void initializeGPS() {
    // Conectar con dispositivo GPS real
    // Usar Windows Location API o NMEA
}
```

## 🐛 Solución de Problemas

| Error | Solución |
|-------|----------|
| **WLAN API no inicializada** | Ejecutar como administrador |
| **No se detectan redes** | Verificar WiFi activado |
| **GPS no disponible** | Verificar conexión a internet |
| **Errores de compilación** | Instalar C++ Desktop Development |

## 📝 Changelog

### v1.0 - Versión Actual
- ✅ Sistema completo de wardriving automático
- ✅ Interfaz ASCII art moderna
- ✅ Información del sistema en tiempo real
- ✅ Geolocalización por IP con geocodificación inversa
- ✅ Exportación CSV y mapas HTML interactivos
- ✅ Estadísticas detalladas con visualizaciones
- ✅ Menú dinámico adaptativo
- ✅ Manejo robusto de errores

## 🤝 Contribuir

1. Fork el proyecto
2. Crear rama para feature (`git checkout -b feature/AmazingFeature`)
3. Commit cambios (`git commit -m 'Add AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abrir Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

**Pecar** - Desarrollador del WiFi WarDriver Automático

---

> ⚠️ **Nota**: Este software está diseñado para uso ético y educativo. Cumple con todas las leyes locales sobre wardriving y privacidad de datos.

## ⭐ ¿Te gustó el proyecto?

¡Dale una estrella al repositorio si te resultó útil! 
