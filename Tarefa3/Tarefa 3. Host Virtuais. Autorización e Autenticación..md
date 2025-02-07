Configuramos un servidor virtual para [www.omeusitio.lan](http://www.omeusitio.lan). Descomprime o arquivo omeusitio.lan.tar.gz en  e fai que se monte en /opt/web/oumeusitio.lan 

A configuración do host virtual é a seguinte: 

1. O directorio raíz de documentos debe ser /opt/web/omeusitio.lan/htdocs, e debe permitir o uso de ficheiros .htaccess relacionados coa autenticación e información de ficheiros. Tamén queremos habilitar a opción para amosar un listado do contido do directorio no caso de se introduza un directorio na URL e que non exista ningún dos ficheiros especificados como de procura nese caso. Indica cal é a configuración do sitio virtual e explícaa detalladamente. 

   ![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.001.png)

   El host virtual quedaria asi (la primera parte) 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.002.jpeg)

En el compose.yml ponemos los alias y copiamos la carpeta del sitio a sitios enabled. 

2. No directorio imaxes, queremos permitir so que se descarguen os ficheiros con extensións .jpg, jpeg, bmp, gif, png e tiff. Todos os demais deberían esta bloqueados.  Explica o resultado obtido unha vez accedido cun navegador web á URL[ http://www.omeusitio.lan/imaxes](http://www.omeusitio.lan/imaxes) tendo en conta o contido do directorio imaxes. Comproba se se pode acceder explicitamente ao ficheiro .pdf que hai dentro dese directorio.  

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.003.jpeg)

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.004.jpeg)

**Ahora no se puede acceder a sample.pdf o al directorio directamente.** 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.005.jpeg)

**Las imagenes si son accesibles.** 

3. No directorio datos queremos bloquearlle o acceso aos clientes que teñan enderezo na rede 192.168.58.128/25 mediante ficheiros .htaccess. Indica o contido dese ficheiro, e tamén comproba con un cliente dentro desa subrede e outro fora se se pode acceder ou non a ese directorio. 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.006.png)

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.007.png)

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.008.jpeg)

Desde este cliente que esta en esta red, no se puede acceder 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.009.jpeg)

Ponemos un cliente en otra red 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.010.jpeg)

Ahora ya se puede acceder a este directorio. 

4. No directorio traballadores, queremos habilitar a autenticación Basic, e para elo crearemos os usuarios ana e eva. Gardaremos a lista de usuarios nun ficheiro en /opt/web/omeusitio.lan/ que debería ter un nome que impida ser accedido accidentalmente. Amosa a configuración, a ventá de acceso no navegador e a liña do log onde se ve o nome do usuario que fixo login. 

   ![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.011.png)

   ![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.012.png)

   ![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.013.jpeg)

   Pide usuario y contraseña 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.014.jpeg)

Metemos usuario y contraseña 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.015.jpeg)

Y ya podemos acceder al sitio. 

5. No directorio directivos, queremos habilitar a autenticación Digest, e para elo crearemos os usuarios xan e lois. Gardaremos a lista de usuarios nun ficheiro en /opt/web/omeusitio.lan/ que debería ter un nome que impida ser accedido accidentalmente. Escolleremos como nome de dominio (*realm*) “directivos”. Amosa a configuración, a ventá de acceso no navegador e a liña do log onde se ve o nome do usuario que fixo login. 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.016.png)

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.017.png)

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.018.jpeg)

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.019.jpeg)

Metemos usuario y contraseña 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.020.jpeg)

Y ya tenemos acceso al sitio. 

6. No directorio contas, usando ficheiros .htaccess, queremos permitir o acceso a certos grupos de usuarios usando autenticación Basic. Gardaremos a lista de usuarios nun ficheiro en /opt/web/omeusitio.lan/ que debería ter un nome que impida ser accedido accidentalmente. Poderán acceder o usuario manolo e os membros do grupo directivos (matias, anton) que sexan a súa vez membros do grupo accionistas (anton, maría, olga) e que non sexan a súa vez membros do grupo temporais (matias, olga, xaime) 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.021.png)

Fichero de grupos 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.022.png)

Fichero de usuarios 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.023.jpeg)

Ahora se piden las credenciales. 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.024.jpeg)

Como manolo 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.025.jpeg)

Se puede entrar. 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.026.jpeg)

Como anton  

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.027.jpeg)

Tambien se entra porque ademas de estar en el grupo directivos esta en el de accionistas. 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.028.jpeg)

Como olga 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.029.jpeg)

Te devuelve a la pagina de login porque no tiene permiso de acceso al ser miembro del grupo temporales. 

7. Indica como se faría para impedirlle o acceso á URL[ http://www.omeusitio.lan/secure](http://www.omeusitio.lan/secure) aos clientes que teñan un enderezo IP que comece por 172.16 e aos que teñan un nome cuxo dominio sexa apache.lan 

   ![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.030.png)

   Para eso se podrian usan estas directivas con require not. 

8. Indica como farías para configurar o acceso ao directorio reservado da seguinte maneira: Para poder acceder, ten que cumprirse que o usuario sexa manolo, ou pertencer ao grupo admin e máis administradores e a súa vez estar no grupo vendas ou comerciais, e que baixo ningún concepto se pertenza ao grupo temporais ou interinos ou que o enderezo IP sexa 192.168.58.99 

![](Aspose.Words.4bc110b2-d8d5-49db-9933-a46739a65962.031.jpeg)

Serian estas directivas 
