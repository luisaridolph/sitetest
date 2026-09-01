---
layout: default
title: "Home"
permalink: /
---

<!--
  ATENÇÃO: não sobrescreva o index.md atual do repositório sem comparar
  antes — ele já tem conteúdo (a home atual, focada na CTPM). Use esta
  estrutura como referência para reorganizar, não como substituição direta.
-->

<!-- [preencher — descrição breve do grupo] -->

## Coleções

<!-- [preencher — 1-2 linhas + link para /colecoes/ctpm/ e /colecoes/rbetno/] -->

## Últimas publicações

{% assign recentes = site.publicacoes | sort: "data" | reverse | limit: 3 %}
<ul>
  {% for pub in recentes %}
    <li><a href="{{ pub.url | relative_url }}">{{ pub.titulo }}</a></li>
  {% endfor %}
</ul>

## Próximos eventos

{% assign proximos = site.eventos | sort: "data" | limit: 3 %}
<ul>
  {% for evento in proximos %}
    <li><a href="{{ evento.url | relative_url }}">{{ evento.titulo }}</a></li>
  {% endfor %}
</ul>

## Visita autoguiada

<!-- [preencher — chamada para /colecoes/ctpm/visite/] -->
