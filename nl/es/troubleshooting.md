---

copyright:
  years: 2017
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

-   Busque en el mosaico un flujo en ejecución en el panel de instrumentos de {{site.data.keyword.appconserviceshort}}. Si hay una marca de color verde, el flujo se ha ejecutado correctamente; pulse la marca para ver cuándo se activó por última vez el flujo.

    ![Captura de pantalla que muestra que un flujo se ha ejecutado correctamente](/images/SuccessfulFlow.jpg)

    Si hay un punto de exclamación rojo, hay un problema; pulse en el signo de exclamación para averiguar qué ha fallado. ![Captura de pantalla que muestra que un flujo tiene un problema](/images/ErroredFlow.jpg)

-   Compruebe la página de estado de {{site.data.keyword.appconserviceshort}} para ver si hay problemas conocidos actuales o si hay algún mantenimiento planificado: [página de estado de {{site.data.keyword.appconserviceshort}}![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Para ver la información de registro de los flujos, pulse **Anotaciones** en el menú hamburguesa de {{site.data.keyword.appconserviceshort}}. Los mensajes de error y de información de los flujos se muestran de forma predeterminada en Kibana, donde puede ver los datos de un intervalo de tiempo específico o utilizar filtros para mostrar determinados tipos de información. Para ver información de depuración para los flujos, abra el menú en un mosaico de flujo en el panel de instrumentos de {{site.data.keyword.appconserviceshort}} y, a continuación, seleccione **Habilitar registro de depuración**.  Necesitará reiniciar el flujo para que comiencen las anotaciones en el registro de depuración.  Tenga en cuenta que cuando se habilita el registro de depuración, las entradas de registro de depuración, incluyendo potencialmente los datos de carga útil, son visibles para los operadores de IBM. Para obtener más información sobre el registro de depuración, consulte [Depuración de los flujos de mensajes en {{site.data.keyword.appconserviceshort}}](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  Para obtener más información acerca de Kibana, consulte la [documentación de Kibana ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Para visualizar información de registro de los servidores de integración, abra un servidor de integración y pulse en **Descargar registros** o **Visualizar registros**.  Para visualizar los registros de un servidor de integración en Kibana, debe adjuntar una política de registro a ese servidor de integración (consulte [Visualización de registros de los servidores de integración ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo") ](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Busque respuestas a las preguntas comunes sobre {{site.data.keyword.appconserviceshort}} en [Preguntas frecuentes acerca de {{site.data.keyword.appconserviceshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Siga las instrucciones paso a paso acerca de cómo conectar aplicaciones en [Guías de aprendizaje para {{site.data.keyword.appconserviceshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Si tiene preguntas técnicas sobre el desarrollo o el despliegue de una aplicación con {{site.data.keyword.appconserviceshort}}, publique su pregunta en [Stack Overflow ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) y etiquete su pregunta con "ibm-bluemix" y "app-connect" (con un guión).
-   Para obtener información sobre el servicio y sobre cómo empezar a utilizarlo, utilice el foro [IBM developerWorks&reg; dW Answers ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix). Incluya las etiquetas "bluemix" y "app_connect" (con un carácter de subrayado).

    Para obtener más información sobre el uso de los mecanismos de soporte de {{site.data.keyword.Bluemix}}, consulte [Obtención de ayuda ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.ng.bluemix.net/docs/support/index.html#getting-help).


