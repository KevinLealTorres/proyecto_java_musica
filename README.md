# Proyecto de música con Java
- Por: Kevin Alejandro Leal Torres
- A día: viernes, 3 de mayo de 2024
- Para la materia: Computación en Java
- Profesor: Rodrigo Ildefonso Roman Guzmán


## ¿Qué es?
Se trata de una interfaz gráfica funcional para agregar artistas a una base de datos MySQL


## Requerimientos:
- Maven (ya que hay varias dependencias, como un conector MySQL/J, Jakarta.Persistence e Hibernate).
- Java SDK 18 o superior


## Cómo configurar:
1. Revisar pom.xml y en los campos de "user" y "password" cambiarlas por tu usuario y contraseña en la base de datos MySQL
2. Configurar correctamente la base de datos cómo se describe en el apartado posterior

## Cómo configurar la base de datos
<span style="color:red">Importante: Tener MySQL</span>
1. Crear una base de datos llamada "music" que contenga:


| Tables in music |
| --- |
| albums |
| albumview |
| artists |
| songs |


2. Para la tabla albums:

| Field      | Type    | Null | Key | Default | Extra          |
|------------|---------|------|-----|---------|----------------|
| album_id   | int(11) | NO   | PRI | NULL    | auto_increment |
| album_name | text    | YES  |     | NULL    |                |
| artist_id  | int(11) | YES  | MUL | NULL    |                |

3. Para la tabla albumview:

| Field        | Type    | Null | Key | Default | Extra |
|--------------|---------|------|-----|---------|-------|
| album_name   | text    | YES  |     | NULL    |       |
| artist_name  | text    | YES  |     | NULL    |       |
| track_number | int(11) | YES  |     | NULL    |       |
| song_title   | text    | YES  |     | NULL    |       |

4. Para la tabla artists:

| Field       | Type    | Null | Key | Default | Extra          |
|-------------|---------|------|-----|---------|----------------|
| artist_id   | int(11) | NO   | PRI | NULL    | auto_increment |
| artist_name | text    | YES  |     | NULL    |                |

5. Para la tabla:

| Field        | Type    | Null | Key | Default | Extra          |
|--------------|---------|------|-----|---------|----------------|
| song_id      | int(11) | NO   | PRI | NULL    | auto_increment |
| track_number | int(11) | YES  |     | NULL    |                |
| song_title   | text    | YES  |     | NULL    |                |
| album_id     | int(11) | YES  | MUL | NULL    |                |


## Punto de inicio:
Es ```MusicManagementApp.java``` que es una GUI
