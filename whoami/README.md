<style type="text/css">
.container {
  margin: 0 auto;
  max-width: 1200px;
  padding: 0 1rem;
  position: absolute;
}
.responsive-image {
  max-width: 100%;
  width: 400px;
  padding: 10px;
}
.cell img {
  display: block;
  position: relative;
  z-index: -1;
}

@media screen and (min-width: 600px) {
  .grid {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
  }
  .cell {
    width: 50%;
  }
}

@media screen and (min-width: 1000px) {
  .cell {
    width: calc(100% / 6);
  }
}

.cell img {
	-webkit-transform: scale(1);
	transform: scale(1);
	-webkit-transition: .3s ease-in-out;
	transition: .3s ease-in-out;
}
.cell:hover img {
	-webkit-transform: scale(1.3);
	transform: scale(1.3);
}
.cell div.background {
  background: #CCC;
  filter: alpha(opacity=60);
  -moz-opacity: 0.6;
  opacity: 0.6;
  top: -15%;
  left: 60%;
  height: 20%;
  width: 100%;
}
.cell div.label {
  position: relative;
  /* top: -15%; */
  left: 60%;
  transform: translate(-50%, -50%);
}
.cell div.name {
  font-size: 50%;
}
.cell div.role, div.contact {
  font-size: 30%;
}
.cell div.contact {
  top: 1%;
}
</style>

<section class="nes-container t-grey with-title">
  <h2 class="title tred">Who's Who</h2>
    <div class="gallery">
      <div class="grid">
      {% for page in site.pages %}
        {% if page.resource == true %}
          {% for pc in page.categories %}
            {% if pc == "whoami" %}
              {% assign counter = counter | plus:1 %}
        <div class="cell">
          <a href="/tamedia-hackdays{{ page.url }}">
            <img src="/tamedia-hackdays/whoami/pics/{{ page.name | replace:'.md','.png' }}" class="responsive-image"/>
          </a>
          <!-- <div class="background"></div> -->
          <div class="label name">{{ page.yourname }}</div>
          <div class="label role">{{ page.role }}</div>
          <div class="label contact">{{ page.contact | markdownify }}</div>
        </div>
            {% endif %}   <!-- cat-match-p -->
          {% endfor %}  <!-- page-category -->
        {% endif %}   <!-- resource-p -->
      {% endfor %}  <!-- page -->
      </div>
    </div>

</section>

<i class="nes-charmander"></i>

<section class="nes-container t-grey with-title">
  <h2 class="title tred">Hints for Adding Yourself to this List</h2>

  <ul class="nes-list is-disc">
    <li>Put your character sheet in the /tamedia-hackdays/whoami/ directory of this git repository</li>
    <li>You can use <a href="/tamedia-hackdays/whoami/harryfuecks">this page</a> as a template. Make sure to use the meta tags at the top of the file (see template for clues)</li>
    <li>If you want a Gameboy-ified version of your photo <a href="http://yrlab.zatunen.com/webgl/gbpic/gbpic.html">try this</a> (Google Translate FTW)</li>
    <li>Put your pictures in the /tamedia-hackdays/whoami/pics/ directory of this repo</li>
  </ul>
</section>