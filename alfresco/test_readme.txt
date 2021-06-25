
Baixar i instal·lar Alfresco.

Si es disposa de docker es pot emprar la imatge:
  docker pull pdubois/docker-alfresco
i arrancar amb
  docker run -d --name alfresco -e INITIAL_PASS=admin -p 9090:8080 -p 9443:8443 pdubois/docker-alfresco
 (es pot ometre un dels dos ports si només es vol emprar HTTP o només HTTPS)
 (adaptar 9090, o 9443 a un port que no doni conflictes a la màquina local)

Una vegada instal·lat Alfresco o arrancada la imatge de Docker:

 - Conectar a http[s]://HOST:PORT/share amb l'usuari administrador (normalment: admin/admin)
 - Anar a Sites -> Create Site, i crear un site amb el nom "ODES"
 - Anar a Admin Tools -> Users -> New User, i crear un usuari. Emprar username/pass proves/proves
 - Anar a Sites -> ODES -> Site members i fer un Invite a l'usuari proves i donar-li el role "Manager".
 - Sortir i entrar com usuari proves/proves per acceptar l'invitació. Anar a Tasks -> My tasks.
 - Visualitzar la invitació i acceptar-la
 - Anar a Sites -> My Sites -> ODES -> Document Library i crear les següenst carpetes:
    * test
    * testFull
    * testAutomaticMetadatas
    * testReposWithFolder
    * testSimpleDoc
 - Descomprimir dins la carpeta "test" el contingut del zip test_retro_606443123400344.zip
   (si arrastrant la carpeta no funciona, crear primer la subcarpeta 606443123400344 i després pujar-hi els
   10 fitxers dedins arrastrant-los)

I ja es poden executar els tests