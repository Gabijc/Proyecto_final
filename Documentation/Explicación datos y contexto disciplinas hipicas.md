# La competición hípica

En este documento se encuentra un detalle de la información que se va a obtener de la FEI database, el flujo de trabajo que se seguirá al realizar la extracción de los datos, información sobre las disciplinas analizadas, y el esquema de la base de datos. 

Los datos que se van a sacar de la FEI Database se indican a continuación, en función del grupo al que pertenecen.

## Disciplinas

 En la web/documento adjuntado con cada disciplina se encuentra una explicación del funcionamiento de la disciplina, junto a las reglamento y el funcionamiento de las diferentes pruebas que se pueden dar, obtenidas a través de la web de Inside FEI (https://inside.fei.org/). Se adjuntan a continuación.

- Salto:
    - Web salto: https://inside.fei.org/fei/disc/jumping
    - Reglamento: https://inside.fei.org/fei/disc/jumping/rules

- Completo:
    - Web completo: https://inside.fei.org/fei/disc/eventing
    - Reglamento: https://inside.fei.org/node/3822/

- Doma:
    - Web Doma: https://inside.fei.org/fei/disc/dressage
    - reglamento: https://inside.fei.org/node/3821/

## Personas: Jinetes/Judges/Course Designer/Steward/Veterinay/Owners

Se indica a continuación el detalle/columnas que se obtiene sobre cada jinete:

- FEI ID: id de la fei
- Gender: genero
- Civility: Monsieur/Madame
- Family Name: nombre de familia (apellido?)
- First Name: nombre	
- Nationality: nacionalidad
- Status
- Date of Birth: fecha de nacimiento
- Date of Retirement: fecha de retiro	
- Date Deceased: fecha de defuncion	
- Middle Initials: inicialess? no coger?	
- Administering NF: federacion
- Block automatic NF: ??
- admin. requests: ??
- Groups: si es jinete, owner...
- competing for: pais por el que compite (en athlete)

## Caballos

Se indica a continuación el detalle/columnas que se obtiene sobre cada caballo:

- Sex: mare, gelding, stallion
- Birth Name: fecha de nacimiento del caballo.
- Current Name: nombre actual del caballo (no coger?).
- Commercial prefix or suffix: nombre comercial del caballo (no coger?).	
- Complete Name: nombre completo del caballo.
- Shorten Name: nomrbe acortado del caballo (no coger?).
- Status: estatus del caballo.
- Date of Birth: fecha de nacimiento.
- Date of Retirement: fecha de retiro, solo aplicará a aquellos caballos que han sido retirados.
- Date of Death: fecha de defunción del caballo, solo aplicará a aquellos caballos que han muerto.	
- Country of Birth: 	
- Color Code: capa del caballo.	
- Color Complement: complemento del color. 	
- Gender: género del animal (male/female).
- Castrated/Sterilized: información sobre si está castrado o no el caballo/yegua.
- Pony: indicación de si es poni o no el animal.
- Studbook (WBFSH members): libro genealógico del caballo. A continuación se indica el enlace al Studbooks List de la FEI -> https://inside.fei.org/fei/your-role/veterinarians/passports/wbfsh. 
- Breed: raza del caballo.
- Breeder's name: nombre del criador.	
- Sire: padre del caballo.
- Sire's UELN: identificacion UELN del padre.
- Dam: madre del caballo.	 
- Dam's UELN: identificación UELN de la madre.
- Sire of Dam: padre de la madre del caballo.	 
- Dam's Sire's UELN: identificacion UELN del padre de la madre del caballo. 
- Administering NF: federación administrativa.
- Block automatic NF admin. requests: no coger?
- FEI ID: id de la fei.
- National ID: id del pais de pertenencia (id nacional).
- Issuing NF: federacion 	GBR
- FEI Recognized: no coger?
- Document ID: no coger?	
- Issuing Body: no coger?	
- UELN: número de registro del libro genealógico de nacimiento sin modificaciones. En el siguiente enlace hay información sobre el UELN (https://inside.fei.org/fei/your-role/veterinarians/passports/ueln).
- Chip ID: no coger?
- ID Type: no coger?
- Issuing Date: no coger?
- Valid Until: no coger? 
- Revalidation Sticker Nr.: no coger?
- Tabla ownerships

Ejemplo de caballo con diferencias en el nombre y en las ownerships: https://data.fei.org/Horse/Detail.aspx?p=D5AD1391080966E85016281ED04EF37C 

Otros enlaces interesantes:

- Precios de modificación del nombre del caballo: https://inside.fei.org/system/files/Horse%20Name%20Change%20Guidelines_01.03.2020_1.pdf 
- National identification documents approved by the FEI: https://inside.fei.org/fei/veterinarians/passports/national-id 

## Competiciones

Según la disciplina y la competición el reglamento, el funcionamiento de las pruebas y la puntuación van a variar. Vamos a deiferenciar, desde la FEI Database lo siguiente:

https://inside.fei.org/system/files/Jumping%20requirements_v2b.pdf

### Show

Obtendremos la información en el show detail. Se indica a continuación el detalle que se obtiene sobre este apartado:

- Tour: tipo de tour.
- Show Type: tipo de show.
- NF: federacion nacional.
- Venue	Oliva: ubicación de realización.
- Venue Complement:	complemento de la ubicación.
- Contact email(s): mail de contacto.
- Start Date: fecha de inicio.
- End Date: fecha de fin.
- URL: url de la competicion.

A partir del show, se obtienen a continuación los Events, en la sección de Events.

### Event

Obtendremos la información en el show detail. Se indica a continuación el detalle que se obtiene sobre este apartado:

- Venue: ubicacion.	
- Venue Complement: complemento ubicacion.		
- NF: federacion.
- Show Type: tipo competicion.
- Discipline: disciplina.
- Category: categoría jinetes.
- Official Team: por equipos?
- Date from: fechas de inicio y fin.
- Indoor: cerrado o abierto.
- Event Code: tipo de competición (1*, 2*...).
- Code Complement: ??	
- Event on borrowed horses: event con caballos prestados??.
- Draft Schedule Prize Money: dinero estimado en premios.
- Prize Money: dinero destinado en premios.
- Schedule: informaicón general sobre el evento (pdf). Coger y en ese caso donde guardar?

A partir del event, se obtienen a continuación las Competitions, en la sección de Competitions.

### Competition

Obtendremos la información en el show detail. Se indica a continuación el detalle que se obtiene sobre este apartado:

- Event: evento/competicion.
- Schedule Competition: numero schedule competition (referencia al pdf). 
- Rule: tipo de competicion (baremos, fases, puntuación).
- Name: nombre competicion.	
- Start Date: fecha de inicio.	
- End Date: fecha de fin.	
- Individual Competition: individual.	
- Team Competition: por grupos.
- Obstacle Height (cm): altura obstaculos.	
- Draft Schedule Prize Money: precio estimado para premios.	
- Draft Schedule Point Group: categoria/ranking de puntos estimado.	
- Prize Money: dinero destinado a premios.	
- Point Group: ranking?
- Result Status: ?

En este punto se pueden obtener los resultados individuales de la competición, de los cuales se pueden obtener los puestos de cada jinete, y los puntos, eliminaciones, etc, del jinete en dicha competición. En este caso la información va a depender del tipo de competición que se esté buscando (salto, doma o cross). 

Por ejemplo, en el caso de una competición que es Table A, dos rondas, siendo la primera ronda un recorrido a contrareloj (hacer doble cero en el mejor tiempo), y la segunda ronda un jump-off contrareloj (GP), los resultados que se obtienen serían los siguientes:
- Ronda 1:
    - Faltas:
        - Obs Time: X (puntuacion por derribos/rehuses) y X (puntuacion por tiempo)
        - Total: puntuacion obtenida sumando lo anterior.
    - Tiempo: tiempo de realización de la prueba
- Jump-off 1:
    - Faltas:
        - Obs Time: X (puntuacion por derribos/rehuses) y X (puntuacion por tiempo)
        - Total: puntuacion obtenida sumando lo anterior.
    - Tiempo: tiempo de realización de la prueba


En el detalle de los resultados individuales se obtiene lo que gana cada participante en función de la posición en la que han quedado. Hay que tener en cuenta que aquellos binomios que no han pasado al jump-off no tendrñan información sobre el mimso, y aquellos que se han retirado/eliminado no tendrán información sobre ninguna ronda, sino una especificación sobre el status de la prueba (RET/EL).

cositas sobre info (tutorials): https://inside.fei.org/uploads/VIDEOS/entry-system-tutorials/#

## Flujo de trabajo del scrapeo propuesto

Inicio FEI Database -> Calendar/Results -> seleccionar las fechas a buscar, la disciplina y que sea con resultados -> ir a past shows -> seleccionar show -> scrapear info show -> seleccionar event -> scrapear info event -> seleccionar competition -> scrapear info competition -> seleccionar individual results -> seleccionar jinete y scrapear detail de jinete -> volver atrás -> seleccionar caballo y scrapear detail del caballo -> volver atrás -> scrapear info de resultado del binomio -> una vez sacada toda la info de la competition, volver atrás y seleccionar si hay más events, y sino para atrás y seleccionar otro show. 

Ejemplo: https://data.fei.org/Calendar/Search.aspx (seguir el flujo seleccionado una de las competiciones pasadas).

A continuación se indica la estructura inicial de la base de datos (sujeta a modificaciones).

- Tabla jinetes: detalle de jinetes/owners...
- Tabla caballos: detalle caballos
- tabla resultados: diferentes resultados posibles a obtener
- tabla fechas: fechas en general
- tabla de shows
- tabla de events
- tabla de competitions 
- tabla de ubicaciones 
- tabla de disciplinas
- tabla de razas, capas? 
- tabla de federaciones

Pendiente de revisar bien y generar el ERD y tipos de datos para subir a la base. 


Guía de la FEI Database: https://inside.fei.org/docs/nfs/nf-guide/fei-database
FEi perfoemance dashboard: https://performancedashboard.fei.org/
How to FEI: https://howto.fei.org/index.html
https://howto.fei.org/content/26/73/en/how-to-download-and-use-the-fei-sportapp.html 
