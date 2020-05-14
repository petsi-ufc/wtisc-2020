---
layout: default
title: WTISC - 2020
---
# Sobre

O Workshop de Tecnologia da Informação do Sertão Central (WTISC) é um evento da Universidade Federal do Ceará Campus Quixadá, realizado anualmente no primeiro semestre do ano, pelo grupo PET - Sistemas de Informação.

O objetivo do evento é promover e difundir o conhecimento sobre as diversas áreas de Tecnologia da Informação, de forma a fortalecer e motivar a formação técnico-profissional, por meio da troca de experiências entre profissionais e acadêmicos.

O WTISC é evento público realizado desde 2008, e consiste na oferta de palestras, minicursos, mesa redonda e hackathon. Buscando apresentar aos alunos/participantes um pouco da realidade do mercado de trabalho.

# Programação

## Minicursos

> Clique no título para **ver mais** sobre os minicursos.

<table class="table table-bordered">
  <thead>
    <tr>
      <th scope="col" style="border: none;"></th>
      <th scope="col">11/05</th>
      <th scope="col">12/05</th>
      <th scope="col">13/05</th>
      <th scope="col">14/05</th>
    </tr>
  </thead>  
  <tbody>
    <tr>
      <th scope="row">14:00-16:00</th>
      <td class="table-react" onclick="location.href = 'minicursos/react'">React</td>
      <td class="table-react" onclick="location.href = 'minicursos/react'">React</td>
      <td class="table-flutter" onclick="location.href = 'minicursos/flutter'">Flutter</td>
      <td class="table-flutter" onclick="location.href = 'minicursos/flutter'">Flutter</td>
    </tr>
    <tr>
      <th scope="row">16:00-17:00</th>
      <td class="table-cafe"  onclick="location.href = 'minicursos/cafe-com-docker'">Café com Docker</td>
      <td class="table-cafe"  onclick="location.href = 'minicursos/cafe-com-docker'">Café com Docker</td>
      <td class="table-cafe"  onclick="location.href = 'minicursos/cafe-com-docker'">Café com Docker</td>
      <td class="table-cafe"  onclick="location.href = 'minicursos/cafe-com-docker'">Café com Docker</td>
    </tr>
  
  </tbody>
</table>


## Palestras


{% assign sorted_pages = site.pages | sort:"date" %}
{% for page in sorted_pages %}
{% if page.categories contains 'palestra' %}
{% if page.passou %}
<div class="item"><h3><a href="{{ page.path}}">{{page.date | date: "%d/%m"}} | {{ page.title }}</a></h3></div>
    {{page.description}}
{% else %}
<div class="item"><s><h3><a href="{{ page.path}}">{{page.date | date: "%d/%m"}} | {{ page.title }}</a></h3></s></div>
    {{page.description}}
{% endif %}
{% endif %}
{% endfor %}