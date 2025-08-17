---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<head>
<meta name="keywords" content="Synthesizer, synthesizers, history, analog, digital, modelling, fm, oscillator, filter, amp, modulation, audio, sound, music">
<meta name="description" content="The Synthesizer - All about the history and the application of the synthesizer">
<meta name="author" content="Mathias Dietrich">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link rel="icon" href="https://thesyntheizer.org/img/favicon.png"/>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Rancho&display=swap" rel="stylesheet">

<style>

body{
   font-family: "Verdana: sans-serif";
   padding:0px;
   margin:0px;
   background-color:black;
   background-image: linear-gradient(#00416a, #e4e5e6);
}
  
.header { 
  font-family: "Verdana: sans-serif";
  position: fixed; 
  height:40px;
  width:100%;
  top: 0; 
  left: 0; 
  right:0;
  background-color:#333344;
  color:gray;
  font-size:13px;
  text-align: center;
  display: grid;
  align-items: center;
}

.title{ 
  margin:10px;
  z-index: 20;
  position: relative; 
  top: 15px;
  font-family: "Rancho", cursive;
  font-weight: 400;
  font-style: normal;
  font-size: 4em;
  color: White;
  line-height: 1em;
}

.teaser{
  margin:10px;
  font-family: "Rancho", cursive;
  font-weight: 400;
  font-style: italic;
  font-size: 2.5em;
  color: White;
}
  
.challenge{
  margin:10px;
  font-size: 1em;
  color:white;
}

.footer { 
    height:30px;
    position: fixed; 
    bottom: 0; 
    left: 0; 
    right: 0;
    z-index: 10;
    background-color:#333344;
    color:gray;
    font-size:11px;
    text-align: center;
    display: grid;
	  align-items: center;
}

h2 {
  font-size: 26px;
  margin: 20px 0;
  text-align: center;
  font-size: 0.5em;
}

a{
  color:white;
}
</style>
</head>

<div class="header">The Synthesizer - All about the history and the application of the synthesizer</div>
<div class="title">The Synthesizer</div>
  <br/>
 <h3 class="teaser">Let's add one synthesizer a day challenge: </h3> 
 <div class="challenge">Do you like to add a synthesizer? Email to <a href="mailto:mat@thesynthesizer.org">mat@thesynthesizer.org</a>.</div>

<div class="responsive-table">
  {% for m in site.data.data %}
  <div class="tool-card">
    <div class="tool-image-column">
      <img class="tool-image" src="{{ m[1] }}" alt="{{ m[2] }} logo" />
    </div>
    <div class="tool-info-column">
      <div class="tool-info">
        <h2 class="tool-title">{{ m[2] }}</h2>
        <p class="tool-meta">{{ m[4] }} | {{ m[5] }}, {{ m[3] }}</p>
        <p class="tool-description">
          {{ m[6] }}
        </p>
        <div class="tool-details">
          <span class="detail-item">{{ m[7] }}</span>
          <span class="detail-item">{{ m[8] }}</span>
          <span class="detail-item">{{ m[9] }}</span>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

<style>
.responsive-table {
  list-style: none;
  padding: 20px;
  margin: 0;
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  max-width: 1200px;
  margin: 0 auto;
}

.tool-card {
  display: grid;
  grid-template-columns: 320px 1fr;
  grid-template-rows: auto;
  gap: 0;
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  min-height: 160px;
}

.tool-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}

.tool-image-column {
  grid-column: 1;
  grid-row: 1;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  padding: 20px;
  background: #f8f9fa;
}

.tool-image {
  width: 280px;
  height: 200px;
  object-fit: cover;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.tool-info-column {
  grid-column: 2;
  grid-row: 1;
  display: flex;
  flex-direction: column;
}

.tool-info {
  padding: 20px;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.tool-title {
  margin: 0 0 8px 0;
  font-size: 1.4rem;
  font-weight: bold;
  color: #333;
  line-height: 1.2;
  text-align: left;
}

.tool-meta {
  margin: 0 0 12px 0;
  font-size: 0.9rem;
  color: #666;
  font-weight: 500;
}

.tool-description {
  margin: 0 0 16px 0;
  font-size: 0.9rem;
  line-height: 1.5;
  color: #555;
  flex-grow: 1;
}

.tool-details {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  margin-top: auto;
}

.detail-item {
  font-size: 0.75rem;
  padding: 6px 10px;
  background: #e9ecef;
  border-radius: 12px;
  color: #666;
  font-weight: 500;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .responsive-table {
    grid-template-columns: 1fr;
    padding: 10px;
  }
  
  .tool-card {
    grid-template-columns: 1fr;
    grid-template-rows: auto auto;
  }
  
  .tool-image-column {
    grid-column: 1;
    grid-row: 1;
    padding: 15px;
  }
  
  .tool-info-column {
    grid-column: 1;
    grid-row: 2;
  }
  
  .tool-image {
    width: 120px;
    height: 100px;
  }
  
  .tool-info {
    padding: 15px;
  }
}

@media (max-width: 480px) {
  .tool-image {
    width: 100px;
    height: 80px;
  }
  
  .tool-title {
    font-size: 1.2rem;
  }
}
</style>