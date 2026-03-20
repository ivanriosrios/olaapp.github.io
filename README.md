# ChatFlow Pro IA ⚡

Extensión de Chrome que proporciona **atajos de teclado inteligentes** y **sugerencias impulsadas por IA** para acelerar tus respuestas en chats.

![Version](https://img.shields.io/badge/version-5.0-blue)
![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-Available-brightgreen)
![License](https://img.shields.io/badge/license-MIT-green)

## 🚀 Características

- **⚡ Atajos Personalizados** - Crea atajos con tus respuestas más comunes
- **🤖 IA Inteligente** - Sugerencias impulsadas por Claude y ChatGPT con contexto de 5-10 mensajes previos
- **📚 Casos Típicos** - Importa problemas y soluciones específicas de tu industria en JSON
- **✅ Corrector Ortográfico** - Validación automática en español (300+ correcciones)
- **💰 Plan Freemium** - Gratis: 50 casos | Premium: 500 casos
- **🔧 Variables Dinámicas** - Usa `{nombre}`, `{email}`, `{empresa}` en tus respuestas
- **🔐 Datos Locales** - Todo se almacena en tu navegador, no en servidores remotos

## 📥 Instalación

### Desde Chrome Web Store (Recomendado)
1. Ve a [Chrome Web Store - ChatFlow Pro IA](https://chrome.google.com/webstore)
2. Haz clic en "Agregar a Chrome"
3. ¡Listo! Abre cualquier chat y usa `..` (doble punto) para activar

### Instalación Manual (Desarrollo)
1. Descarga este repositorio: `git clone https://github.com/olaapp/chatflow-pro-ia.git`
2. En Chrome, ve a `chrome://extensions/`
3. Activa "Modo de desarrollador" (arriba a la derecha)
4. Haz clic en "Cargar extensión sin empaquetar"
5. Selecciona la carpeta `chatflow-pro-ia`

## 🎯 Cómo Usar

### Activar la Extensión
- **Mac**: `Alt + Shift + Space`
- **Windows**: `Ctrl + .` (punto)
- **Todos**: Escribe `..` (doble punto) en cualquier chat

### Crear un Atajo
1. Abre el popup de la extensión
2. Ve a la pestaña "⚡ Atajos"
3. Escribe tu atajo: `.saludo`
4. Escribe tu respuesta: "¡Hola! ¿En qué puedo ayudarte?"
5. Guarda
6. Úsalo escribiendo `.saludo` en cualquier chat

### Importar Casos Típicos
1. Ve a la pestaña "📚 Casos Típicos"
2. Haz clic en "Importar JSON"
3. Sube tu archivo `casos-tipicos.json`
4. Los casos se cargarán automáticamente

### Usar IA
1. Ve a la pestaña "⚙ Config"
2. Activa "Sugerencias de IA"
3. Elige Claude o ChatGPT
4. Agrega tu API key
5. La extensión sugerirá respuestas automáticamente

## 📋 Estructura del Proyecto

```
chatflow-pro-ia/
├── manifest.json                 # Configuración de Chrome
├── popup.html                    # Interfaz principal
├── popup.js                      # Lógica de la UI
├── content.js                    # Content script
├── background.js                 # Service worker
├── ai-suggest.js                 # Motor de sugerencias IA
├── spellcheck.js                 # Corrector ortográfico
├── casos-tipicos-TEMPLATE.json   # Template de casos
├── README.md                     # Este archivo
└── images/                       # Iconos y assets
```

## 🔧 Configuración

### Archivo: `casos-tipicos.json`

```json
{
  "metadata": {
    "version": "1.0",
    "sector": "Call Center",
    "empresa": "Tu Empresa",
    "idioma": "es",
    "fecha": "2026-03-20"
  },
  "casos": [
    {
      "id": 1,
      "problema": "Cliente pregunta por estado de pedido",
      "contexto": "Chat en WhatsApp o email",
      "palabras_clave": ["pedido", "estado", "dónde"],
      "respuesta_ideal": "Hola {nombre}, tu pedido #{pedido} está en {estado}. Será entregado el {fecha}.",
      "razón": "Información clara y rápida",
      "pasos": ["Obtener número de pedido", "Verificar en sistema", "Dar estado actual"],
      "tiempo_resolucion": "2 minutos",
      "prioridad": "Alta"
    }
  ]
}
```

## 🤖 Integración con IA

La extensión soporta dos proveedores de IA:

### Claude (Anthropic)
- Obtén tu API key en: https://console.anthropic.com
- Modelo: `claude-3-5-sonnet-20241022`
- Excelente para contexto y comprensión compleja

### ChatGPT (OpenAI)
- Obtén tu API key en: https://platform.openai.com/api-keys
- Modelo: `gpt-4-turbo`
- Rápido y confiable

## 🔐 Privacidad y Seguridad

- **Datos Locales**: Todo se almacena en tu navegador con Chrome Storage API
- **Sin Servidores**: No enviamos tus datos a servidores remotos
- **Control Total**: Exporta o elimina tus datos cuando quieras
- **Opcional IA**: Las sugerencias de IA son completamente opcionales
- **API Keys Seguras**: Tus claves de IA se almacenan solo en tu navegador

Ver [Política de Privacidad](privacidad.html) completa.

## 🚀 Casos de Uso

### Call Centers
- Respuestas rápidas para preguntas frecuentes
- Casos típicos importables
- Sugerencias automáticas de soluciones

### Energía / Servicios
- Información de facturas y consumo
- Protocolos de atención estandarizados
- Respuestas con variables personalizadas

### Atención al Cliente
- Respuestas a consultas comunes
- Escalación de problemas complejos
- Reducción de tiempo de respuesta

### Empresas en General
- Cualquier equipo que envíe mensajes repetitivos
- Ahorro de tiempo significativo
- Mejor calidad de respuestas

## 📊 Ventajas de Freemium

### Plan Gratis
- ✅ 50 casos típicos
- ✅ Atajos de teclado ilimitados
- ✅ Corrector ortográfico
- ❌ IA limitada (solo 5 sugerencias/día)

### Plan Premium
- ✅ 500 casos típicos
- ✅ Atajos ilimitados
- ✅ Corrector ortográfico avanzado
- ✅ IA ilimitada (Claude + ChatGPT)
- ✅ Variables dinámicas avanzadas
- ✅ Sincronización en la nube

## 🐛 Reporte de Bugs

Si encuentras un problema:
1. Ve a [Issues](https://github.com/olaapp/chatflow-pro-ia/issues)
2. Describe el problema detalladamente
3. Incluye tu sistema operativo y versión de Chrome

## 💡 Sugerencias de Mejora

¿Tienes una idea? [Abre una discusión](https://github.com/olaapp/chatflow-pro-ia/discussions) o contáctanos.

## 📝 Licencia

MIT License - Ver [LICENSE](LICENSE) para detalles.

## 👤 Contacto

- **Email**: ivanargemiroriosrios@gmail.com
- **Empresa**: OlaApp
- **GitHub**: [@olaapp](https://github.com/olaapp)

## 🙏 Contribuciones

Las contribuciones son bienvenidas. Por favor:
1. Fork el proyecto
2. Crea una rama (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 🎓 Stack Tecnológico

- Chrome Manifest V3
- Vanilla JavaScript
- Chrome Storage API
- Claude API (Anthropic)
- ChatGPT API (OpenAI)
- MutationObserver para detección de mensajes
- Content Security Policy (CSP) compatible

---

**Hecho con ❤️ por OlaApp para acelerar tu trabajo**
