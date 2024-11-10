[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=16675045)
> Iván García González

# Práctica 9 Introduction to Systems Development" and Static Generators
## Sistemas y Tecnologia Web Servidor

### Despliegue del sitio Web en GitHub pages usando Jekyll
Se ha realizado el despliegue del Sitio Web en GitHub pages, se puede consultar aqui: [Mi Página en Pages](https://ull-mii-sytws-2425.github.io/intro2sd-ivan-garcia-gonzalez-alu0101388786/)

![alt text](img/imagePages.png)

### Resumen de los conceptos del capítulo
Se realiza un resumen del capitulo 1 del libro en un post:
![Resumen](img/imageResumen.png)

### Kanban Board project conteniendo las incidencias de la rúbrica
![Kandban](img/imageBoard.png)

### Despliegue en netlify o Vercel
Se ha realizado el despliegue del Sitio Web en Netlify, se puede consultar aqui: [Mi Página en Netlify](https://staticdeployivan.netlify.app/)

![alt text](img/imageNetlify.png)

### Se ha creado una Jekyll Collection
Se ha creado una nueva colección sobre la lucha canaria en `_lucha_canaria`, con tres posts sobre la historia, reglas y figuras. Se ha realizado además las configuraciones necesarias en el `_config.yml`.
![alt text](img/imageCollection.png)

### Se ha hecho uso de liquid
En el post `Ejemplo de Uso de Liquid`, se muestra un ejemplo sencillo del uso de Liquid en Jekyll, incluyendo un bucle `for`, una estructura condicional `if-else`, y la asignación de variables.

```yml
items:
  - Ordenador
  - Teclado
  - Ratón
  - Monitor
  - Impresora
---

## Listado de Equipos (Uso de For)

{% for item in page.items %}
- Equipo disponible: {{ item }}
{% endfor %}

<!--more-->

## Detalle Condicional de Equipos (Uso de For e If-Else)

{% for item in page.items %}
{% if item == "Impresora" %}
**Nota**: La {{ item }} está en mantenimiento.
{% else %}
El {{ item }} está disponible para su uso.
{% endif %}
{% endfor %}

## Total de Equipos

{% assign total_items = page.items | size %}
Actualmente, hay {{ total_items }} equipos listados.
```
### Se ha hecho uso de un .csv o .json en `_data`
En el post `Ejemplo de Uso de Datos`, se incorpora la informacion de un `.json` llamado `famosos` ubicado en la carpeta `_data` de Jekyll para acceder y mostrar información en un post de manera sencilla.

```md
<table>
  <thead>
    <tr>
      <th>Nombre</th>
      <th>Profesión</th>
      <th>Lugar de Nacimiento</th>
    </tr>
  </thead>
  <tbody>
    {% for persona in site.data.famosos %}
    <tr>
      <td>{{ persona.nombre }}</td>
      <td>{{ persona.profesion }}</td>
      <td>{{ persona.lugar_nacimiento }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
```

### Reconfigurado los defaults del _config.yml
Se ha realizacio varias configuraciones en el fichero _config.tml:
Se ha cambiado el baseurl con el correpondiente de mi repositorio, el nombre de la página por mi nombre y foto, los links a las redes sociales, el footer y el tema de la página.

**Tema, BaseUrl y Name**
![Tema, BaseUrl y name](img/imageTema.png)

**Social**
![alt text](img/imageSocial.png)

**Author**
![alt text](img/imageAuthor.png)

**Footer**
![alt text](img/imageFooter.png)

### Página 404 personalizada usando async JS y web services
Se ha personalizado la página 404, para que realize una llamada a una api que devuelve fotos de perros aleatoriamente
![alt text](img/image404.png)

### Página personal en GitHub Pages
![alt text](img/imagePersonal.png)

### Página personal en GitHub Pages enlazada desde el perfil GitHub del alumno
![alt text](img/imagePersonalEnlazado.png)