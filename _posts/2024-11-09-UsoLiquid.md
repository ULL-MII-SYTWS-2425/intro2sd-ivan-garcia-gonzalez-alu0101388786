---
title: "Ejemplo de Uso de Liquid"
excerpt_separator: "<!--more-->"
categories:
  - Post Formats
tags:
  - Post Formats
  - Liquid
items:
  - Ordenador
  - Teclado
  - Ratón
  - Monitor
  - Impresora
---

En este post, se muestra un ejemplo sencillo del uso de Liquid en Jekyll, incluyendo un bucle `for`, una estructura condicional `if-else`, y la asignación de variables.

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
