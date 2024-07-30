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
.responsive-table {
  li {
    display: table;
    width:100%;
    border-radius: 13px;
    margin-top:5px;
    margin-left:0px;
    padding: 2px 2px;
    display: flex;
    justify-content: space-between;
    margin-bottom: 5px;
  }
  .table-header {
    background-color: #95A5A6;
    font-size: 14px;
    text-transform: uppercase;
    letter-spacing: 0.03em;
  }
  .table-row {
    width:100%;
    background-color: #ffffff;
    box-shadow: 0px 0px 9px 0px rgba(0,0,0,0.1);
    letter-spacing: 0.03em;
  }

  .col-1 {
    flex-basis: 160px;
    text-align: left;
    padding:5px;
  }
  .col-2 {
    flex-basis: 100%;
    margin:5px;
    text-align: left;
    background-color:#EEEEEE;
  }
  .col-3 {
    margin:0px;
    text-align: left;
    background-color:#FFFFFF;
  }
  .col-4 {
    text-align: left;
    flex-basis: 20%;
  }
  .col-5 {
    text-align: left;
    flex-basis: 20%;
  }
  .col-6 {
    text-align: left;
    flex-basis: 20%;
    color:black;
    a{
       color:blue;
    }
  }
  
  <!-- bundle exec jekyll serve  -->
</style>
</head>

<div class="header">The Synthesizer - All about the history and the application of the synthesizer</div>
<div class="title">The Synthesizer</div>
  <br/>
  <ul class="responsive-table">

    {% for m in site.data.data %}
    <li class="table-row">
     <div class="col col-1"><img src="{{ m[1]}}" width=150 height=150/><b>{{m[2]}}</b>
     <br/>{{ m[4] }}
     <br/>{{ m[5] }}, {{ m[3] }}
     </div>
     <div class="col col-2">
      <table >
      <tr>
      <td colspan ="3">
        <div class="col col-3">
          {{ m[6] }}
        </div>
        </td>
        </tr>
      <tr>
        <td><div class="col col-4">{{m[7]}}</div></td>
        <td><div class="col col-5">{{m[8]}}</div></td>
        <td><div class="col col-6">{{m[9]}}</div></td>
       </tr>
      </table>
      </div>
      </li>
    {% endfor %}
</ul>
 <h3 class="teaser">Let's add one synthesizer a day challenge: </h3> 
 <div class="challenge">Do you like to add a synthesizer? Email to <a href="mailto:mat@thesynthesizer.org">mat@thesynthesizer.org</a>.</div>
