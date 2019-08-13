---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-06"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# Guía de aprendizaje de iniciación
{: #getting-started}

{{site.data.keyword.appconservicefull}} le ayuda a conectar aplicaciones: desde simples interacciones entre un desencadenante y una acción a complejas integraciones.  Puede utilizar {{site.data.keyword.appconserviceshort}} para crear flujos controlados por sucesos o flujos para API.  O puede cargar y ejecutar las soluciones de integración que cree en IBM Integration Bus, sin la necesidad de adquirir y mantener una infraestructura de TI.  Puede ver y administrar todas sus integraciones: servidores de integración, flujos controlados por sucesos y flujos para las API, en un único lugar del panel de control de {{site.data.keyword.appconserviceshort}}. 

Después de crear una instancia del servicio de {{site.data.keyword.appconserviceshort}}, puede acceder a {{site.data.keyword.appconserviceshort}} desde el panel de control de {{site.data.keyword.Bluemix}}.

Los pasos siguientes le proporcionarán suficiente información para que se inicie con App Connect.  Para obtener instrucciones más detalladas, guías de procedimiento para aplicaciones específicas, guías de aprendizaje y vídeos, consulte el conjunto completo de documentación en [IBM App Connect ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/).

## Creación de un flujo controlado por sucesos

Como sugiere el nombre, un flujo controlado por sucesos consta de un suceso en una aplicación de origen, que desencadena el flujo, y una o más acciones en las aplicaciones de destino. Por lo tanto, cuando sucede algo en la aplicación de origen, se desencadena una acción en las aplicaciones de destino.  Para crear un flujo controlado por sucesos que conecte las aplicaciones basadas en la nube, complete los pasos siguientes.
1.  En el panel de control de {{site.data.keyword.appconserviceshort}}, pulse en **Nuevo** > **Flujo controlado por sucesos**.
    {{site.data.keyword.appconserviceshort}} guarda los cambios automáticamente a medida que avanza. Si navega fuera del flujo en cualquier etapa, el flujo se guarda como un borrador que puede completar en otro momento.
1.  Especifique un nombre para el flujo.
1.  Seleccione el suceso desencadenante para iniciar el flujo expandiendo una aplicación y seleccionando un suceso.
1.  Si aún no está conectado a la aplicación, pulse en **Conectar a la _aplicación_** y escriba los detalles de inicio de sesión para la misma.
    Es posible que tenga que proporcionar detalles de conexión adicionales para algunas aplicaciones; si necesita ayuda para encontrar credenciales para una aplicación en particular, consulte la publicación [Guía de procedimiento para aplicaciones ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/).
1.  Seleccione la acción que debe desencadenarse en la segunda aplicación expandiendo una aplicación y seleccionando una acción.
    Si aún no se ha conectado a la aplicación, pulse en **Conectar a la aplicación** y escriba los detalles de inicio de sesión para la misma.
1. Especifique los datos que desea transferir entre las aplicaciones.
    Puede añadir manualmente nombres de campos de origen pulsando en un campo y, a continuación, pulsando el icono de correlación ![Icono de correlación](/images/MappingIcon.jpg). También puede escribir texto, o utilizar una función de transformación para personalizar el valor de origen. Para obtener más información, consulte [Cómo utilizar las transformaciones ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms).
1. Opcional: puede refinar cómo funciona el flujo realizando las operaciones siguientes:
    * Añada más aplicaciones de destino y acciones pulsando el icono del signo más en el flujo ![Icono de añadir aplicación](/images/AddApp.jpg).
    * Añada acciones de recuperación al flujo para recuperar elementos que coincidan con determinados criterios o recupere un número específico de registros.  También puede añadir acciones de recuperación que definan el manejo de errores o definir cómo maneja los elementos que se recuperan (consulte [Utilización de App Connect para recuperar elementos de las aplicaciones ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).
    * Añada lógica condicional para realizar diferentes acciones que dependan los datos que se reciban de las aplicaciones del flujo (consulte [Añadir lógica condicional a un flujo ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).

1. Cuando el flujo esté configurado, abra el menú de opciones en la barra de cabecera y pulse **Iniciar flujo**.

Si vuelve al panel de control de {{site.data.keyword.appconserviceshort}}, podrá ver que el flujo se está ejecutando.  Cuando se produce un suceso en la primera aplicación,{{site.data.keyword.appconserviceshort}} desencadena automáticamente una acción en la segunda aplicación. Puede visualizar el estado de los flujos en el panel de control de {{site.data.keyword.appconserviceshort}}.  Para visualizar los registros de los flujos, abra el menú de hamburguesa ![Icono de menú de hamburguesa](/images/HamburgerMenuSm.jpg), expanda **Gestionar** y, a continuación, pulse **Registros**.

Para obtener más información, consulte [Creación de un flujo controlado por sucesos ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

## Creación de un flujo para una API

Si desea que un desarrollador pueda crear una aplicación que utilice los datos de las aplicaciones basadas en la nube, puede proporcionar una API. Para crear flujos para una API, complete los pasos siguientes.
1. En el panel de control de {{site.data.keyword.appconserviceshort}}, pulse en **Nuevo** > **Flujos para una API**.
1. Especifique un nombre para la API.
1. Especifique un nombre para el modelo que refleje el tipo de objeto con el que trabaja la API y, a continuación, pulse en **Crear modelo**.
1. Añada las propiedades necesarias para definir la estructura del objeto con el que trabaja la API.
    Por ejemplo, si la API crea o recupera un cliente, puede que tenga que añadir propiedades denominadas Customer_ID, First_Name, Last_Name y Email_Address. Puede escribir el nombre de una propiedad o pulsar en **Seleccionar propiedades de las aplicaciones** para elegir las propiedades de una o varias aplicaciones a las que está conectado.
1. Pulse **Operaciones** para definir cómo interactúa la API con el objeto y añada las operaciones que necesite. 
1. Para cada operación, pulse **Implementar flujo** para crear un flujo que defina la forma en que funciona cada operación. 
1. Añada una o varias aplicaciones de destino al flujo, entre la solicitud y la respuesta. 
    Si desea que el flujo realice operaciones diferentes para condiciones diferentes, también puede añadir lógica condicional (consulte [Añadir lógica condicional a un
flujo ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).
1. Pulse en **Respuesta** en el flujo para definir la respuesta que se devuelve cuando se completa la operación. Correlacione los campos disponibles de la aplicación de destino. 
1. Pulse **Terminado** para volver al modelo.
1. Cuando todos los modelos y operaciones estén definidos, inicie la API seleccionando **Iniciar API** en el menú. 

Los flujos de la API ya están listos. En el panel de control de {{site.data.keyword.appconserviceshort}}, los flujos para las API se identifican mediante el icono de API. Puede iniciarlos y detenerlos de la misma forma que cualquier otro flujo. Puede abrir una API mientras se está ejecutando, pero tiene que detenerla antes de poder editarla.

Para obtener más información, consulte [Creación de flujos para una API ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Para saber cómo probar la API, consulte [Exposición de un flujo de conexión de App Connect a través de API Connect ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/).


## Ejecución de una solución de integración de IBM Integration Bus

Puede desplegar soluciones de integración desarrolladas en IBM Integration Bus o en App Connect Enterprise en la nube sin necesidad de adquirir y mantener una infraestructura de TI. Importe un archivo BAR que contenga todos los artefactos que componen la solución de integración y, a continuación, ejecute el contenido en un servidor de integración de App Connect. Para cargar un archivo BAR en App Connect debe tener IBM Integration Bus versión 10.0.0.4 o posterior, o App Connect Enterprise, que se instala localmente.

Para ejecutar las soluciones de Integration Bus o App Connect Enterprise en App Connect, complete los pasos siguientes.
1. En el panel de control de {{site.data.keyword.appconserviceshort}} pulse en **Nuevo** > **Importar un archivo BAR**.
1. Seleccione el archivo BAR que desea importar, edite el nombre si lo desea y, a continuación, pulse en **Importar**. 
    Si ve un error de autenticación, compruebe que el archivo BAR es válido (consulte [¿Qué hace que un archivo BAR sea válido en App Connect? ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta)).
    Se crea un servidor de integración, y se añade un mosaico al panel de control para representarlo. El estado cambia de "En preparación" a "Detenido" cuando el servidor de integración está listo para ser configurado e iniciado. 
1. Haga clic en el mosaico para abrir el servidor de integración.
1. Configure el servidor de integración:
    * Añada o edite una descripción para la solución de integración.
    * Configure la autenticación básica de HTTPS (consulte [Configuración de la autenticación básica HTTPS ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta)).
    * Adjunte una política para que pueda conectarse a sistemas locales (consulte [Configuración de la conectividad segura entre servidores de integración en App Connect y en los sistemas locales ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta)).
1. Opcional: Para dividir el flujo de proceso de mensajes entre el entorno local y App Connect, configure flujos invocables. Abra el menú de hamburguesa ![Icono de menú de hamburguesa](/images/HamburgerMenuSm.jpg), expanda **Gestionar**, y seleccione **Flujos invocables** (consulte [Compartir el proceso del flujo de mensajes entre App Connect e Integration Bus ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta)).
1. Cuando haya completado la configuración, vuelva al panel de control de App Connect e inicie el servidor de integración abriendo el menú de mosaicos y pulsando en **Iniciar**.

Cuando el servidor de integración se está ejecutando, puede ver y descargar registros abriendo el servidor de integración y pulsando en **Descargar registros** o **Visualizar registros**. Para visualizar los registros, debe adjuntar una política de registro al servidor de integración (consulte [Visualización de registros de los servidores de integración ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).

Para obtener más información, consulte [Ejecución de las soluciones de Integration Bus en App Connect ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan).
