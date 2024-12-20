# ✨ SkillAlexaClima200051

### _Alexa Skill_  
📱 **Unidad 3 - Desarrollo Móvil Integral**

---

## Descripción
Este proyecto consiste en el desarrollo de una aplicación en **Flutter** para dispositivos móviles. Es la primera aplicación en Flutter como parte de la unidad 2 de la asignatura de Desarrollo Móvil Integral.

---

### 📅 Historial de Prácticas:

| No. | Nombre                                   | Potenciador | Estatus |
| --- | ---------------------------------------- | ----------- | ------- |
| 26  | Creacion de Skill Alexa Clima  | 6          | Activa  |

---


# 🚀 Practica26: Skill Alexa Clima

![images](https://github.com/user-attachments/assets/0be46ab0-5d71-440b-b268-887a77dd7d4a)
<p align="center">
  <img src="img/Logo.jpg" alt="Logo del proyecto" width="300"/>
  <img src="img/utxj.jpg" alt="Logo de la institución" width="300"/>
</p>

### 📝 Datos del Estudiante
- **Nombre:** Daniela Aguilar Torres  
- **Carrera:** Ingeniería en Desarrollo y Gestión de Software  
- **Cuatrimestre:** 10  
- **Grupo:** A  

---
## Descripción
Este proyecto tiene como objetivo diseñar una skill para Alexa que utilice una API externa, como OpenWeatherMap, para recopilar y proporcionar información climática de una ciudad. 

Los participantes aprenderán a crear una skill básica para Alexa, integrando servicios web para obtener datos en tiempo real y responder de manera efectiva a las consultas de los usuarios.

## Características
- Obtención de datos meteorológicos en tiempo real.
- Respuestas personalizadas basadas en la ciudad solicitada.
- Uso de tecnologías modernas para asistentes virtuales y servicios web.

## Objetivo
Desarrollar una herramienta interactiva que permita a los usuarios consultar el clima de forma sencilla, mejorando su experiencia mediante la integración de Alexa con datos actualizados proporcionados por APIs externas.

## Requisitos
- **API**: Acceso a OpenWeatherMap (o similar).
- **Herramientas**: Amazon Developer Console, Alexa Skills Kit (ASK).

# Pasos para Crear una Alexa Skill

## 1. Crear una Cuenta de Desarrollador en Amazon
- Accede a la [Amazon Developer Console](https://developer.amazon.com/).
- Regístrate o inicia sesión con tu cuenta de Amazon.
- Navega a la consola de desarrollador de Alexa.

- ![Imagen 2](https://github.com/user-attachments/assets/8901d2c9-3d10-43e3-810b-2c6e821f071d "IMG2")

---


## 2. Crear un Nuevo Proyecto de Alexa
- En la consola de Alexa, selecciona **"Create Skill"**.
- Configura lo siguiente:
  - **Idioma:** Selecciona el idioma de tu skill (e.g., Español).
  - **Tipo de Skill:** Selecciona **"Custom"** (Skill Personalizada).
  - **Nombre de la Skill:** Asigna un nombre único (e.g., "Clima Alexa").
 
  - ![Imagen 8](https://github.com/user-attachments/assets/011f1d00-1e0c-4a2d-90ec-9eaf7fab5715 "IMG8")
  - ![Imagen 9](https://github.com/user-attachments/assets/2285500d-e6c4-4105-bc7f-74a5c81f2052 "IMG9")
  - ![Imagen 10](https://github.com/user-attachments/assets/ab6bef1e-ad60-4280-ac80-fdc52a650d3d "IMG10")
  - ![Imagen 11](https://github.com/user-attachments/assets/cbb260d4-c471-4be5-a9fc-466ea4116afd "IMG11")



---

## 3. Configurar las Intenciones de la Skill
- En el editor de intents (intenciones), crea una nueva llamada **"Clima"**.
- Agrega frases de activación, como:
  - "Como sera el clima hoy "
  - "hara sol hoy"
- Estas frases ayudarán a Alexa a reconocer cuándo activar esta intención.
- ![Imagen 12](https://github.com/user-attachments/assets/21b74ee4-ece8-49df-b797-5543d09ebc0c "IMG12")

- 
---
## 4. Verificar las Intenciones en el Editor JSON
- Revisa el archivo JSON en la sección de **Interaction Model**.
- Asegúrate de que las intenciones creadas estén reflejadas en el modelo.
- ![Captura de pantalla 2024-12-06 092922](https://github.com/user-attachments/assets/6c87dd7e-e0c0-48e3-9bbc-fae1391b1c45)

---


## 5. Aplicar las Coordenadas
- Configura la habilidad para aceptar coordenadas de ubicación como entrada.
- Si usas OpenWeatherMap, asegúrate de enviar las coordenadas adecuadas para obtener datos precisos.
- ![Imagen 14](https://github.com/user-attachments/assets/4260cea4-d2d2-495e-904f-d6aab7d0150c "IMG14")

---

## 6. Configurar el Nombre de Invocación
- Establece el **nombre de invocación** en la sección de configuración de tu skill (e.g., "Clima Fácil").
- Este será el nombre que los usuarios dirán para activar la skill (e.g., "Alexa, abre Clima Fácil").
- ![Imagen 16](https://github.com/user-attachments/assets/c2689c1a-e3a6-4e7e-99ca-fd76021d9453 "IMG16")


---

## 7. Personalizar el Ícono de la Skill
- Diseña un ícono representativo para tu skill.
- Súbelo en los formatos requeridos (tamaño: 108x108 y 512x512 píxeles).
- ![Imagen 17](https://github.com/user-attachments/assets/d979af43-c168-4c78-8c35-b8cb0a690fe0 "IMG17")


---

## 8. Configurar la Privacidad y Publicación
- Asegúrate de configurar correctamente los permisos y políticas de privacidad.
- Envia la skill para su validación por parte del equipo de Amazon.
- ![Imagen 18](https://github.com/user-attachments/assets/0342c98b-2159-451a-89c7-9b5e46ddc474 "IMG18")

---

![Imagen 19](https://github.com/user-attachments/assets/436c478d-95ef-4e12-b87b-f18c3ad338ac "IMG19")

## 9. Realizar Pruebas
- Prueba tu skill en el **Simulador de Alexa Developer Console**.
![Resultado](https://github.com/user-attachments/assets/e5be5266-64e3-4e2a-87b8-5b27899b716b)
---

## 📂 Código Fuente

```

const Alexa = require('ask-sdk-core');
const axios = require('axios');

const LaunchRequestHandler = {
  canHandle(handlerInput) {
    return Alexa.getRequestType(handlerInput.requestEnvelope) === 'LaunchRequest';
  },
  handle(handlerInput) {
    const speakOutput = 'Esta es la Skill hecha por: Daniela Aguilar ';

    return handlerInput.responseBuilder
      .speak(speakOutput)
      .reprompt(speakOutput)
      .getResponse();
  }
};

const WeatherIntentHandler = {
  canHandle(handlerInput) {
    return (
      Alexa.getRequestType(handlerInput.requestEnvelope) === 'IntentRequest' &&
      Alexa.getIntentName(handlerInput.requestEnvelope) === 'Clima'
    );
  },
  async handle(handlerInput) {
    try {
      const apiKey = '4712cc4dd1d36867b723b2109144413b'; // Reemplaza con tu clave de API de OpenWeatherMap
      const lat = 19.050; // Reemplaza con la latitud deseada
      const lon = -98.200; // Reemplaza con la longitud deseada

      const response = await axios.get(
        `https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lon}&appid=${apiKey}&units=metric`
      );

      const temperature = response.data.main.temp;
      const weatherDescription = response.data.weather[0].description;
      const location = response.data.name;
      const humedad = response.data.main.humidity;
      const tem_max = response.data.main.temp_min;
      //NUEVO
      const sepone = response.data.sys.sunset;
      const sunsetDate = new Date(sepone);
      const sunsetHour = sunsetDate.getHours();
      const sunsetMinutes = sunsetDate.getMinutes();

      

      const speakOutput = `La temperatura actual en ${location} es de ${temperature} grados Celsius y la humedad es de ${humedad} y el sol se oculta a las ${sunsetHour}:${sunsetMinutes}.`;

      return handlerInput.responseBuilder.speak(speakOutput).getResponse();
    } catch (error) {
      console.log('Error al obtener el clima:', error);

      const speakOutput = 'Lo siento, no pude obtener la información del clima en este momento.';
      return handlerInput.responseBuilder.speak(speakOutput).getResponse();
    }
  },
};

const HelpIntentHandler = {
  canHandle(handlerInput) {
    return (
      Alexa.getRequestType(handlerInput.requestEnvelope) === 'IntentRequest' &&
      Alexa.getIntentName(handlerInput.requestEnvelope) === 'AMAZON.HelpIntent'
    );
  },
  handle(handlerInput) {
    const speakOutput = 'Puedes preguntarme sobre el clima diciendo: ¿Cuál es el clima actual?';

    return handlerInput.responseBuilder.speak(speakOutput).getResponse();
  },
};

const CancelAndStopIntentHandler = {
  canHandle(handlerInput) {
    return (
      Alexa.getRequestType(handlerInput.requestEnvelope) === 'IntentRequest' &&
      (Alexa.getIntentName(handlerInput.requestEnvelope) === 'AMAZON.CancelIntent' ||
        Alexa.getIntentName(handlerInput.requestEnvelope) === 'AMAZON.StopIntent')
    );
  },
  handle(handlerInput) {
    const speakOutput = '¡Hasta luego!';

    return handlerInput.responseBuilder.speak(speakOutput).getResponse();
  },
};

const FallbackIntentHandler = {
  canHandle(handlerInput) {
    return (
      Alexa.getRequestType(handlerInput.requestEnvelope) === 'IntentRequest' &&
      Alexa.getIntentName(handlerInput.requestEnvelope) === 'AMAZON.FallbackIntent'
    );
  },
  handle(handlerInput) {
    const speakOutput = 'Lo siento, no puedo ayudarte con eso. Por favor, inténtalo de nuevo.';

    return handlerInput.responseBuilder.speak(speakOutput).getResponse();
  },
};

const SessionEndedRequestHandler = {
  canHandle(handlerInput) {
    return Alexa.getRequestType(handlerInput.requestEnvelope) === 'SessionEndedRequest';
  },
  handle(handlerInput) {
    console.log(`Sesión terminada: ${JSON.stringify(handlerInput.requestEnvelope)}`);
    return handlerInput.responseBuilder.getResponse();
  },
};

const IntentReflectorHandler = {
  canHandle(handlerInput) {
    return Alexa.getRequestType(handlerInput.requestEnvelope) === 'IntentRequest';
  },
  handle(handlerInput) {
    const intentName = Alexa.getIntentName(handlerInput.requestEnvelope);
    const speakOutput = `Acabas de activar la intención ${intentName}.`;

    return handlerInput.responseBuilder.speak(speakOutput).getResponse();
  },
};

const ErrorHandler = {
  canHandle() {
    return true;
  },
  handle(handlerInput, error) {
    console.log(`Error manejado: ${JSON.stringify(error)}`);

    const speakOutput = 'Lo siento, hubo un problema al procesar tu solicitud. Por favor, inténtalo de nuevo.';

    return handlerInput.responseBuilder.speak(speakOutput).getResponse();
  },
};

exports.handler = Alexa.SkillBuilders.custom()
  .addRequestHandlers(
    LaunchRequestHandler,
    WeatherIntentHandler,
    HelpIntentHandler,
    CancelAndStopIntentHandler,
    FallbackIntentHandler,
    SessionEndedRequestHandler,
    IntentReflectorHandler
  )
  .addErrorHandlers(ErrorHandler)
  .lambda();

```

