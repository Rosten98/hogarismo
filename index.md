---
layout: default
title: Inicio
---
<header>
    <nav class="container">
        <img src="/assets/logo.svg" alt="Logo de Hogarismo" width="50px">
        <div class="links">
            <a href="/">Inicio</a>
            <a href="/#contact">Contacto</a>
          <!-- <a href="#">Nosotros</a> -->
        </div>
    </nav>
    <div class="copy container">
        <h1>Hogar hecho realidad</h1>
        <p>Invierte en tu patrimonio y encuentra tu hogar ideal</p>
       <a href="#properties" class="btn">Ver propiedades</a>
    </div>
</header>


<section class="properties" id="properties">
    <div class="container">
      <div class="heading">
        <h2 class="">Propiedades</h2>
        <div class="line"></div>
      </div>
      <!-- <label for="search-property">
        Busca una propiedad:
      </label>
      <br>
      <input type="text" id="search-property" placeholder="Busca por: colonia, precio, ciudad..."> -->
    </div>
    <div class="container properties-cards">
      {% for post in site.posts %}
      <div class="property-card">
        <img src="{{ post.images | relative_url }}/1.jpeg" alt="" class="fade">
        <div class="property-card-footer">
          <p class="title">{{post.title}}</p>
          <p class="price">{{post.price}} MXN</p>
          <p class="location "><i class="fas fa-map-marker-alt"></i> {{post.location}}</p>
          <a href="{{post.url}}" class="btn-sm">Saber más</a>
        </div>
      </div>
      {%endfor%}
    </div>
</section>

<div class="container">
  <div class="heading">
    <h2 style="background:white">Contacto</h2>
    <div class="line"></div>
  </div>
</div>
<section class="contact container" id="contact">

  <div class="contact-form">
    <b>¿Encontraste lo que buscabas?</b>
    <br><br>
    <form class="" action="https://formspree.io/mrgywrav" method="POST">
      <label for="fullname">Nombre completo</label><br>
      <input type="text" id="fullname" name="fullname" value="" placeholder="Juan Pérez" required>
      <br>
      <label for="phone">Número celular:</label><br>
      <input type="text" id="phone" name="phone" value="" placeholder="3350503365" required>
      <br>
      <label for="message">¿En qué te podemos ayudar?</label><br>
      <textarea name="message" id="message" rows="8" cols="50" required></textarea>
      <button type="submit" name="button" class="btn">Enviar</button>
    </form>
  </div>

  <div class="social">
    <b>Encuentranos en redes sociales y WhatsApp</b>
    <div class="fb-page"
      data-href="https://www.facebook.com/HogarismoMx"
      data-width="400"
      data-hide-cover="false"
      data-show-facepile="true">
    </div>
    <!-- <button type="button" name="button" class="fb-cta"><i class="fab fa-facebook-messenger"></i>Mensaje a Hogarismo Facebook</button> -->
    <a href="https://wa.me/5213302020202?text=Me%%20interesa%20obtener%20info%20sobre%20Hogarismo" class="wa-cta"><i class="fab fa-whatsapp"></i>Mensaje a Hogarismo WhatsApp</a>
  </div>
</section>
