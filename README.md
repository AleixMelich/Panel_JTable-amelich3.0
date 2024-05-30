# Panel_JTable-amelich3.0
This is my third JTable panel implemented with Java, the project is made from IntellIJ. 

## *MP03 - UF6*

### Instruccions generals
Heu de fer un projecte MAVEN en Java a l’IntelliJ que inclogue (en negreta el que es nou a esta UF6): 
mode gràfic en patró MVC,
connexió a una BD Oracle utilitzant l’API JDBC,
fer el CRUD sobre alguna taula de la BD HR d'Oracle, però creada per vatros. Si useu una sola taula la nota màxima serà un 8, si voleu excel·lent heu de tindre mínim 2 taules relacionades, 
interfície DAO i classe DAOException personalitzada. Incloeu  dins la interfície DAO els nous mètodes abstractes que hagueu necessitat a la classe implementació (delete, update, ….), 
ús de la vostra excepció personalitzada pel tractament dels possibles errors en la BD,
finestra en taula, botons per Insertar, Borrar i Modificar, etiquetes i camps (mínim 1 tipo text, un tipo numèric i un booleà),
tractament d'excepcions dels camps (text no buit, números correctes, ...) usant la vostra pròpia excepció,
Ús d’expressions regulars per controlar els valors dels camps,
Ús d’enumeracions per selecció de valors fixos d’algun camp, inclòs dins un JComboBox
ús del fitxer Properties per connectar-se a la BD,
ús de Prepared Statements, per fer consultes i actualitzacions a la BD,
creació de la/es taula/es des d'un procediment emmagatzemat de l'Oracle, codificat en PL/SQL,
crida a alguna funció emmagatzemada de l'Oracle (PL/SQL),
inclussió de mètodes per tasques repetitives al controlador,
documentació en Javadoc dels mètodes, i comentaris al codi allà on 
Es valorarà positivamernt:
Ús d’algun disparador d’Oracle per evitar alguna situació indesitjable a la BD,
Accés a una variable cursor de l’Oracle des de Java, mitjançant algun procediment o funció emmagatzemada.
Quan accepteu la tasca del github classroom se us crearà un repositori que conté:
Un projecte MAVEN de l’IntelliJ incomplet en codi per poder-se connectar a la BD Oracle, que seguix el patró MVC i conté la interfície DAO, la classe DAOException, … 
Una carpeta PLSQL on haureu de copiar el codi PL/SQL de creació de la/es taula/es, procediment i/o funció emmagatzemats, triggers...., al fitxer pl.sql inclòs.
Una carpeta documentació per si us calgués entregar-ne. Els documents de text s’han de lliurar en format PDF. Aquí heu de mostrar on i com heu implementat cadascun dels punts demanats, sent més important el detall en tot allò que sigue nou a esta UF.
La intenció és fer la correcció a classe durant els 2 últims dies (29 i 31 de maig), però si no ho teniu acabat haureu de presentar documentació o presentar-ho a la segona convocatòria.
La durada del projecte serà d’aproximadament 15h, que es correspon en la durada real de la UF5 llevat dels dies de correcció.   

Del projecte s’haurà d’entregar:
el projecte en sí mateix (codi font),
El codi PLSQL utilitzat a l’Oracle, 
la documentació en cas de ser necessari.

Com a material de consulta disposareu al MOODLE de tots els apunts presentats pel professor, així com de tota la informació que pugueu trobar per internet.
Interessant:
Podeu obtindre els drivers de connexió a Oracle des del propi contenedor docker, fent el següent (a l'exemple el contenedor se diu oracle18):
docker cp oracle18:/opt/oracle/product/18c/dbhomeXE/jdbc .      


L'anterior ordre crea una carpeta jdbc al directori actual.
Ens desplacem al directori jdbc/lib i en la següent ordre instal·lem el driver al repositori maven local: 
mvn install:install-file -Dfile=ojdbc8.jar -DgroupId=com.oracle -DartifactId=ojdbc8 -Dversion=18.4 -Dpackaging=jar

 
Fixeu-vos que el groupId, artifactId i version, seran els paràmetres que haurem de posar a les dependències del MAVEN (fitxer pom.xml del projecte).

### Criteris d’avaluació
Per calcular la nota se distingiran 2 blocs:
documentació entregada
aplicació o programari desenvolupat

El pes de cadascuna pot variar, però en principi serà de 35% i 65%, respectivament.

Les faltes d’assistència compten com en qualsevol UF, per tant superar el 20% de faltes, pot implicar la pèrdua d’avaluació continua i per tant el suspens en la UF. 

Per poder aprovar el projecte s’ha de treure una nota mínima de 5 a cadascuna de les parts, en cas contrari l’alumne haurà de recuperar la part o parts suspeses, i/o presentar-se a un examen a la convocatòria extraordinària.

