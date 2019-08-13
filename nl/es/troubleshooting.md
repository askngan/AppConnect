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


# Resolución de problemas de IBM App Connect
{: #troubleshooting}

Para resolver problemas de flujos y servidores de integración de {{site.data.keyword.appconservicefull}}, puede visualizar los registros en Kibana. Si tiene preguntas o problemas al utilizar {{site.data.keyword.appconserviceshort}}, obtenga ayuda buscando información o formulando preguntas a través de un foro. Cuando utilice los foros para hacer una pregunta, etiquete su pregunta para que la vean los equipos de desarrollo de {{site.data.keyword.Bluemix}} y {{site.data.keyword.appconserviceshort}}.

-   Busque en el mosaico un flujo en ejecución en el panel de control de {{site.data.keyword.appconserviceshort}}. Si hay una marca de color verde, el flujo se está ejecutando correctamente; pulse en la marca para ver cuándo se activó por última vez el flujo.

    ![Captura de pantalla que muestra que un flujo se está ejecutando satisfactoriamente](/images/SuccessfulFlow.jpg)

    Si hay un punto de exclamación rojo, hay un problema; pulse en el signo de exclamación para averiguar cuál es el problema. ![Captura de pantalla que muestra que un flujo tiene un problema](/images/ErroredFlow.jpg)

-   Compruebe la página de estado de {{site.data.keyword.appconserviceshort}} para ver si se han notificado problemas o si hay algún mantenimiento planificado: [Página de estado de {{site.data.keyword.appconserviceshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Para ver la información de registro de los flujos, pulse **Registros** en el menú de {{site.data.keyword.appconserviceshort}}. Los mensajes de error y de información de los flujos se muestran de forma predeterminada en Kibana, donde puede ver los datos de un intervalo de tiempo específico o utilizar filtros para mostrar determinados tipos de información. Para ver información de depuración para los flujos, abra el menú en un mosaico de flujo en el panel de control de {{site.data.keyword.appconserviceshort}} y, a continuación, seleccione **Habilitar registro de depuración**.  A continuación, deberá reiniciar el flujo para que comiencen las anotaciones en el registro de depuración.  Cuando se habilita el registro de depuración, las entradas de registro de depuración, incluyendo potencialmente los datos de carga útil, son visibles para los operadores de IBM. Para obtener más información sobre el registro de depuración, consulte [Depuración de los flujos de mensajes en {{site.data.keyword.appconserviceshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  Para obtener más información acerca de Kibana, consulte la [documentación de Kibana ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Para visualizar información de registro de los servidores de integración, abra un servidor de integración y pulse en **Descargar registros** o **Visualizar registros**.  Para visualizar los registros de un servidor de integración en Kibana, debe adjuntar una política de registro a ese servidor de integración (consulte [Visualización de registros de los servidores de integración ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Busque respuestas a las preguntas comunes sobre {{site.data.keyword.appconserviceshort}} en [Preguntas frecuentes acerca de {{site.data.keyword.appconserviceshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Siga las instrucciones paso a paso acerca de cómo conectar aplicaciones en [Guías de aprendizaje para {{site.data.keyword.appconserviceshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Para formular preguntas sobre el servicio y obtener instrucciones de iniciación, utilice el foro [IBM dW Answers ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/answers/topics/app_connect). Incluya las etiquetas "ibm_cloud" y "app_connect" (con un carácter de subrayado).

    Para obtener más información sobre el uso de los mecanismos de soporte de {{site.data.keyword.Bluemix}}, consulte [Soporte ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/unifiedsupport/supportcenter).

## Informar de un problema al equipo de IBM App Connect
{: #reporting}

Si ha seguido las recomendaciones de resolución de problemas y todavía tiene un problema, puede obtener ayuda del equipo de {{site.data.keyword.appconserviceshort}}.  En el menú de {{site.data.keyword.appconserviceshort}}, pulse en **Póngase en contacto con nosotros** y después en **Obtener soporte**.  Inicie sesión con su ID de IBM, pulse en **Crear un caso** y proporcione tanta de la información siguiente como pueda. (También puede pulsar **Soporte** en la consola de {{site.data.keyword.Bluemix}}). 

* La región de {{site.data.keyword.Bluemix}} donde se ha suministrado la instancia de {{site.data.keyword.appconserviceshort}}. (Por ejemplo, Dallas o Londres).
* El ID de instancia del servicio de {{site.data.keyword.appconserviceshort}} que está utilizando. (Puede encontrar este ID mirando en la información de cuenta bajo el identificador de instancia de {{site.data.keyword.appconserviceshort}}).
* El problema que está teniendo. (Por ejemplo, si el problema es con una aplicación o función específica).
* El ID de lote si el problema está relacionado con el proceso por lotes. (Si se producen errores en un proceso por lotes y ha definido un ID para cada registro del proceso por lotes, puede encontrar el ID definido en la columna "batch-record-id_str" del registro de Kibana; consulte [Cómo utilizar el procesamiento por lotes en {{site.data.keyword.appconserviceshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/).)
* La fecha y la hora (incluyendo el huso horario) en que el problema ha aparecido por primera vez y la cantidad de tiempo que el flujo se ha ejecutado hasta que se ha producido el problema.
* Si el problema todavía se produce y si puede replicarlo.
* Si es aplicable, el tipo de navegador y la versión que utiliza. (Sólo se admiten las últimas versiones de los navegadores).
* Cualesquiera entradas de registro que describan el problema.
* El impacto que tiene el problema en su empresa.
