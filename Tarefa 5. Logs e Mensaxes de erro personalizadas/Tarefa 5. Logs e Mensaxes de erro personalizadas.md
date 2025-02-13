Tomando como punto de partida a tarefa anterior 

- Queremos facer un log de acceso no ficheiro /var/log/apache2/omeusitio.lan  /acceso.log. Nese log queremos gardar: 
  - Enderezo IP do cliente 
  - Hora na que foi recibida a petición 
  - Bytes recibidos (tamaño da petición) 
  - Tamaño da resposta 
  - Tempo que se tardou en servir a petición 
  - Estado de resolución da petición (código de resposta) 
  - Usuario remoto se foi autenticado 
  - Primeira liña da request 
  - Navegador do usuario 

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.001.png)

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.002.png)

- No caso de que non exista un recurso no servidor, queremos facer que se cargue o documento nonexiste.html. Indica a configuración establecida e inclúe unha captura do navegador accedendo a unha URL que non existe. 

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.003.png)

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.004.png)

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.005.jpeg)

- No caso de que o acceso a un recurso estea prohibido, indica que configuración establecerías para amosar directamente a mensaxe de erro “Acceso prohibido a este recurso” e tamén unha captura do navegador amosando este erro. 

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.006.png)

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.007.jpeg)

- Indica como farías para que se fixese un log dos erros no ficheiro /var/log/apache2/omeusitio.lan/erros.log co seguinte formato: 
  - Enderezo IP do cliente 
  - Hora na que se produce o erro 
  - Nivel de log 
  - Código de estado de erro 
  - Nome do módulo que produce o erro 
  - Mensaxe de Erro 

![](Aspose.Words.79917d5f-a544-4ed0-b3b2-4265d30d873e.008.png)
