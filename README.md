<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CHL Constructora</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
font-family:'Montserrat',sans-serif;
background:#0b0b0b;
color:white;
scroll-behavior:smooth;
}

header{
position:fixed;
top:0;
width:100%;
background:rgba(0,0,0,0.92);
backdrop-filter:blur(10px);
display:flex;
justify-content:space-between;
align-items:center;
padding:18px 8%;
z-index:1000;
border-bottom:1px solid #222;
}

.logo{
font-weight:700;
letter-spacing:2px;
font-size:14px;
}

.header-right{
display:flex;
align-items:center;
gap:20px;
}

.lang-switch{
cursor:pointer;
font-size:13px;
letter-spacing:1px;
opacity:0.85;
}

.menu-toggle{
font-size:24px;
cursor:pointer;
}

nav{
position:fixed;
top:70px;
right:-100%;
width:280px;
height:calc(100vh - 70px);
background:#080808;
display:flex;
flex-direction:column;
align-items:center;
padding-top:45px;
transition:0.3s ease;
box-shadow:-10px 0 35px rgba(0,0,0,0.85);
z-index:999;
}

nav a{
color:white;
text-decoration:none;
margin:15px 0;
font-size:13px;
letter-spacing:1.3px;
text-transform:uppercase;
opacity:0.8;
}

nav a:hover{opacity:1;}
nav.active{right:0;}

.hero{
min-height:100vh;
background:
linear-gradient(rgba(0,0,0,0.45),rgba(0,0,0,0.82)),
url('https://images.unsplash.com/photo-1503387762-592deb58ef4e?auto=format&fit=crop&w=1800&q=80') center/cover no-repeat;
display:flex;
align-items:center;
padding:120px 8% 80px;
}

.hero-box{
max-width:900px;
}

.hero-tag{
font-size:13px;
letter-spacing:2.5px;
text-transform:uppercase;
color:#d6b46d;
margin-bottom:18px;
font-weight:600;
}

.hero h1{
font-family:'Playfair Display',serif;
font-size:52px;
line-height:1.1;
margin-bottom:24px;
}

.hero p{
font-size:17px;
color:#e0e0e0;
line-height:1.7;
max-width:760px;
}

.hero-buttons{
margin-top:32px;
display:flex;
gap:15px;
flex-wrap:wrap;
}

.btn{
display:inline-block;
padding:13px 24px;
background:#25D366;
color:white;
text-decoration:none;
border-radius:4px;
font-weight:700;
font-size:14px;
transition:0.3s;
}

.btn:hover{background:#1ebe5d;}

.btn-dark{
background:transparent;
border:1px solid #d6b46d;
color:#d6b46d;
}

.btn-dark:hover{
background:#d6b46d;
color:#000;
}

.section{
padding:85px 8%;
}

.section-title{
font-family:'Playfair Display',serif;
font-size:36px;
margin-bottom:18px;
}

.section-intro{
color:#cfcfcf;
line-height:1.7;
max-width:800px;
margin-bottom:40px;
}

.grid{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:24px;
}

.card{
background:linear-gradient(180deg,#171717,#101010);
padding:32px;
border-radius:10px;
border:1px solid #252525;
box-shadow:0 18px 40px rgba(0,0,0,0.45);
}

.card h3{
font-size:18px;
margin-bottom:15px;
color:white;
}

.card p{
color:#c9c9c9;
line-height:1.6;
font-size:14.5px;
}

.split{
display:grid;
grid-template-columns:1fr 1fr;
gap:30px;
align-items:center;
}

.image-box{
min-height:420px;
border-radius:12px;
background:url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1400&q=80') center/cover no-repeat;
box-shadow:0 20px 45px rgba(0,0,0,0.6);
}

.dark-box{
background:#121212;
border:1px solid #242424;
padding:42px;
border-radius:12px;
}

.dark-box p{
color:#ccc;
line-height:1.7;
margin-bottom:15px;
}

.highlight{
color:#d6b46d;
font-weight:700;
}

.band{
background:#111;
padding:70px 8%;
border-top:1px solid #222;
border-bottom:1px solid #222;
}

.band-grid{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:20px;
text-align:center;
}

.stat{
padding:25px;
background:#171717;
border-radius:10px;
border:1px solid #252525;
}

.stat strong{
display:block;
font-size:26px;
color:#d6b46d;
margin-bottom:8px;
}

.stat span{
font-size:13px;
color:#ccc;
}

.contact{
background:#080808;
padding:85px 8%;
text-align:center;
}

.contact-box{
background:linear-gradient(180deg,#171717,#101010);
padding:45px;
border-radius:12px;
max-width:620px;
margin:auto;
border:1px solid #252525;
box-shadow:0 20px 45px rgba(0,0,0,0.55);
}

.contact-box h2{
font-family:'Playfair Display',serif;
font-size:34px;
margin-bottom:15px;
}

.contact-box p{
color:#ccc;
line-height:1.6;
margin-bottom:22px;
}

.contact-number{
font-size:18px;
margin-bottom:22px;
font-weight:700;
}

footer{
padding:25px 8%;
text-align:center;
font-size:12px;
color:#777;
background:#000;
border-top:1px solid #1f1f1f;
}

@media(max-width:900px){
.hero h1{font-size:38px;}
.grid{grid-template-columns:1fr;}
.split{grid-template-columns:1fr;}
.band-grid{grid-template-columns:1fr 1fr;}
}

@media(max-width:600px){
header{padding:16px 6%;}
.hero{padding:110px 6% 70px;}
.section,.band,.contact{padding:65px 6%;}
.hero h1{font-size:33px;}
.hero p{font-size:15.5px;}
.band-grid{grid-template-columns:1fr;}
}
</style>
</head>

<body>

<header>
<div class="logo">CHL CONSTRUCTORA</div>
<div class="header-right">
<div class="lang-switch" onclick="toggleLanguage()">ES | DE</div>
<div class="menu-toggle" onclick="toggleMenu()">☰</div>
</div>
</header>

<nav id="menu">
<a href="#obras" data-i="menu1">Reformas y Obras</a>
<a href="#suiza" data-i="menu2">Mano de Obra para Suiza</a>
<a href="#servicios" data-i="menu3">Servicios</a>
<a href="#quienes" data-i="menu4">Quiénes Somos</a>
<a href="#contacto" data-i="menu5">Contacto</a>
</nav>

<section class="hero">
<div class="hero-box">
<div class="hero-tag" data-i="tag">Construcción · Reformas · Coordinación Profesional</div>
<h1 data-i="titulo">Soluciones profesionales en construcción, reformas y mano de obra especializada</h1>
<p data-i="subtitulo">
CHL Constructora ofrece servicios de reformas, obras y soluciones técnicas en España, junto con una división especializada en la coordinación de profesionales cualificados para empresas del sector construcción en Suiza.
</p>
<div class="hero-buttons">
<a href="#contacto" class="btn" data-i="btn_contacto">Solicitar presupuesto</a>
<a href="#suiza" class="btn btn-dark" data-i="btn_suiza">Personal para Suiza</a>
</div>
</div>
</section>

<section class="section" id="obras">
<h2 class="section-title" data-i="obras_t">Reformas y Obras en España</h2>
<p class="section-intro" data-i="obras_intro">
Realizamos trabajos de reforma, acondicionamiento y obra para viviendas, locales comerciales y proyectos profesionales, con una gestión seria, directa y orientada a resultados.
</p>

<div class="grid">
<div class="card">
<h3 data-i="obra1_t">Reformas integrales</h3>
<p data-i="obra1_p">Coordinamos reformas completas de viviendas, locales y espacios comerciales, desde la planificación hasta la ejecución final.</p>
</div>

<div class="card">
<h3 data-i="obra2_t">Locales comerciales</h3>
<p data-i="obra2_p">Acondicionamiento de bares, restaurantes, oficinas y negocios, cuidando acabados, tiempos y funcionalidad.</p>
</div>

<div class="card">
<h3 data-i="obra3_t">Albañilería y acabados</h3>
<p data-i="obra3_p">Trabajos de obra, tabiquería, pladur, pintura, suelos, revestimientos y soluciones técnicas para cada proyecto.</p>
</div>
</div>
</section>

<section class="section">
<div class="split">
<div class="image-box"></div>
<div class="dark-box">
<h2 class="section-title" data-i="vision_t">Una constructora con visión internacional</h2>
<p data-i="vision_1">
CHL Constructora combina experiencia real en obra con conocimiento del mercado laboral español y suizo.
</p>
<p data-i="vision_2">
Nuestro objetivo es ofrecer soluciones serias tanto a clientes que necesitan realizar reformas u obras en España como a empresas que buscan personal cualificado para proyectos en Suiza.
</p>
<p class="highlight" data-i="vision_3">España · Suiza · Construcción · Reformas · Personal especializado</p>
</div>
</div>
</section>

<section class="band">
<div class="band-grid">
<div class="stat">
<strong>01</strong>
<span data-i="stat1">Gestión profesional</span>
</div>
<div class="stat">
<strong>02</strong>
<span data-i="stat2">Experiencia en obra</span>
</div>
<div class="stat">
<strong>03</strong>
<span data-i="stat3">Personal cualificado</span>
</div>
<div class="stat">
<strong>04</strong>
<span data-i="stat4">España y Suiza</span>
</div>
</div>
</section>

<section class="section" id="suiza">
<h2 class="section-title" data-i="suiza_t">Coordinación de Mano de Obra para Suiza</h2>
<p class="section-intro" data-i="suiza_intro">
Además de nuestros servicios de construcción y reformas, gestionamos procesos de selección, documentación e incorporación de profesionales cualificados para empresas suizas del sector construcción.
</p>

<div class="grid">
<div class="card">
<h3 data-i="sui1_t">Selección de perfiles</h3>
<p data-i="sui1_p">Filtrado de albañiles, peones, oficiales y perfiles técnicos según las necesidades reales de cada empresa.</p>
</div>

<div class="card">
<h3 data-i="sui2_t">Gestión documental</h3>
<p data-i="sui2_p">Apoyo en documentación, permisos, currículums, coordinación administrativa y preparación del proceso de incorporación.</p>
</div>

<div class="card">
<h3 data-i="sui3_t">Incorporación profesional</h3>
<p data-i="sui3_p">Acompañamiento en entrevistas, logística inicial, condiciones laborales y adaptación al entorno profesional suizo.</p>
</div>
</div>
</section>

<section class="section" id="servicios">
<h2 class="section-title" data-i="serv_t">Servicios</h2>

<div class="grid">
<div class="card">
<h3 data-i="serv1_t">Construcción y reformas</h3>
<p data-i="serv1_p">Reformas integrales, obra menor, locales comerciales, viviendas, pladur, pintura, suelos y acabados.</p>
</div>

<div class="card">
<h3 data-i="serv2_t">Soluciones para empresas</h3>
<p data-i="serv2_p">Apoyo a empresas que necesitan personal, coordinación profesional y procesos estructurados de incorporación.</p>
</div>

<div class="card">
<h3 data-i="serv3_t">Acompañamiento completo</h3>
<p data-i="serv3_p">Trato directo, planificación, seguimiento y comunicación clara durante todo el proceso de trabajo.</p>
</div>
</div>
</section>

<section class="section" id="quienes">
<div class="dark-box">
<h2 class="section-title" data-i="qs_t">Quiénes Somos</h2>
<p data-i="qs_1">
CHL Constructora nace de la experiencia directa en el sector construcción y del conocimiento práctico del mercado español y suizo.
</p>
<p data-i="qs_2">
Trabajamos con una visión clara: ofrecer soluciones serias, profesionales y bien coordinadas, tanto en reformas y obras como en procesos de mano de obra especializada.
</p>
<p data-i="qs_3">
Nuestra prioridad es la confianza, la transparencia y el cumplimiento en cada proyecto.
</p>
</div>
</section>

<section class="contact" id="contacto">
<div class="contact-box">
<h2 data-i="contact_t">Contacto</h2>
<p data-i="contact_1">
Para presupuestos de reformas, obras o información sobre personal para Suiza, puede contactarnos directamente por WhatsApp.
</p>
<div class="contact-number">+41 76 740 15 41</div>
<a href="https://wa.me/41767401541?text=Hola%20quisiera%20m%C3%A1s%20informaci%C3%B3n%20sobre%20CHL%20Constructora" class="btn" target="_blank" data-i="btn_whatsapp">Contactar por WhatsApp</a>
</div>
</section>

<footer>
CHL CONSTRUCTORA · Construcción, reformas y coordinación profesional
</footer>

<script>
function toggleMenu(){
document.getElementById("menu").classList.toggle("active");
}

let currentLang = "es";

const translations = {
es:{
menu1:"Reformas y Obras",
menu2:"Mano de Obra para Suiza",
menu3:"Servicios",
menu4:"Quiénes Somos",
menu5:"Contacto",
tag:"Construcción · Reformas · Coordinación Profesional",
titulo:"Soluciones profesionales en construcción, reformas y mano de obra especializada",
subtitulo:"CHL Constructora ofrece servicios de reformas, obras y soluciones técnicas en España, junto con una división especializada en la coordinación de profesionales cualificados para empresas del sector construcción en Suiza.",
btn_contacto:"Solicitar presupuesto",
btn_suiza:"Personal para Suiza",
obras_t:"Reformas y Obras en España",
obras_intro:"Realizamos trabajos de reforma, acondicionamiento y obra para viviendas, locales comerciales y proyectos profesionales, con una gestión seria, directa y orientada a resultados.",
obra1_t:"Reformas integrales",
obra1_p:"Coordinamos reformas completas de viviendas, locales y espacios comerciales, desde la planificación hasta la ejecución final.",
obra2_t:"Locales comerciales",
obra2_p:"Acondicionamiento de bares, restaurantes, oficinas y negocios, cuidando acabados, tiempos y funcionalidad.",
obra3_t:"Albañilería y acabados",
obra3_p:"Trabajos de obra, tabiquería, pladur, pintura, suelos, revestimientos y soluciones técnicas para cada proyecto.",
vision_t:"Una constructora con visión internacional",
vision_1:"CHL Constructora combina experiencia real en obra con conocimiento del mercado laboral español y suizo.",
vision_2:"Nuestro objetivo es ofrecer soluciones serias tanto a clientes que necesitan realizar reformas u obras en España como a empresas que buscan personal cualificado para proyectos en Suiza.",
vision_3:"España · Suiza · Construcción · Reformas · Personal especializado",
stat1:"Gestión profesional",
stat2:"Experiencia en obra",
stat3:"Personal cualificado",
stat4:"España y Suiza",
suiza_t:"Coordinación de Mano de Obra para Suiza",
suiza_intro:"Además de nuestros servicios de construcción y reformas, gestionamos procesos de selección, documentación e incorporación de profesionales cualificados para empresas suizas del sector construcción.",
sui1_t:"Selección de perfiles",
sui1_p:"Filtrado de albañiles, peones, oficiales y perfiles técnicos según las necesidades reales de cada empresa.",
sui2_t:"Gestión documental",
sui2_p:"Apoyo en documentación, permisos, currículums, coordinación administrativa y preparación del proceso de incorporación.",
sui3_t:"Incorporación profesional",
sui3_p:"Acompañamiento en entrevistas, logística inicial, condiciones laborales y adaptación al entorno profesional suizo.",
serv_t:"Servicios",
serv1_t:"Construcción y reformas",
serv1_p:"Reformas integrales, obra menor, locales comerciales, viviendas, pladur, pintura, suelos y acabados.",
serv2_t:"Soluciones para empresas",
serv2_p:"Apoyo a empresas que necesitan personal, coordinación profesional y procesos estructurados de incorporación.",
serv3_t:"Acompañamiento completo",
serv3_p:"Trato directo, planificación, seguimiento y comunicación clara durante todo el proceso de trabajo.",
qs_t:"Quiénes Somos",
qs_1:"CHL Constructora nace de la experiencia directa en el sector construcción y del conocimiento práctico del mercado español y suizo.",
qs_2:"Trabajamos con una visión clara: ofrecer soluciones serias, profesionales y bien coordinadas, tanto en reformas y obras como en procesos de mano de obra especializada.",
qs_3:"Nuestra prioridad es la confianza, la transparencia y el cumplimiento en cada proyecto.",
contact_t:"Contacto",
contact_1:"Para presupuestos de reformas, obras o información sobre personal para Suiza, puede contactarnos directamente por WhatsApp.",
btn_whatsapp:"Contactar por WhatsApp"
},

de:{
menu1:"Umbauten und Bauarbeiten",
menu2:"Fachkräfte für die Schweiz",
menu3:"Dienstleistungen",
menu4:"Über uns",
menu5:"Kontakt",
tag:"Bau · Renovierung · Professionelle Koordination",
titulo:"Professionelle Lösungen für Bau, Renovierung und qualifizierte Fachkräfte",
subtitulo:"CHL Constructora bietet Bau- und Renovierungsdienstleistungen in Spanien sowie eine spezialisierte Abteilung für die Koordination qualifizierter Fachkräfte für Schweizer Bauunternehmen.",
btn_contacto:"Offerte anfragen",
btn_suiza:"Personal für die Schweiz",
obras_t:"Renovierungen und Bauarbeiten in Spanien",
obras_intro:"Wir führen Renovierungs-, Ausbau- und Bauarbeiten für Wohnungen, Geschäftslokale und professionelle Projekte aus – seriös, direkt und ergebnisorientiert.",
obra1_t:"Komplettrenovierungen",
obra1_p:"Wir koordinieren komplette Renovierungen von Wohnungen, Lokalen und Gewerbeflächen von der Planung bis zur finalen Ausführung.",
obra2_t:"Geschäftslokale",
obra2_p:"Ausbau von Bars, Restaurants, Büros und Geschäftsräumen mit Fokus auf Ausführung, Zeitplanung und Funktionalität.",
obra3_t:"Maurerarbeiten und Ausbau",
obra3_p:"Bauarbeiten, Trockenbau, Malerarbeiten, Böden, Verkleidungen und technische Lösungen für jedes Projekt.",
vision_t:"Ein Bauunternehmen mit internationaler Vision",
vision_1:"CHL Constructora verbindet praktische Bauerfahrung mit Kenntnissen des spanischen und schweizerischen Arbeitsmarktes.",
vision_2:"Unser Ziel ist es, seriöse Lösungen für Kunden in Spanien sowie für Unternehmen anzubieten, die qualifiziertes Personal für Projekte in der Schweiz suchen.",
vision_3:"Spanien · Schweiz · Bau · Renovierung · Fachpersonal",
stat1:"Professionelle Abwicklung",
stat2:"Erfahrung im Bau",
stat3:"Qualifiziertes Personal",
stat4:"Spanien und Schweiz",
suiza_t:"Koordination von Fachkräften für die Schweiz",
suiza_intro:"Neben unseren Bau- und Renovierungsdienstleistungen koordinieren wir Auswahl-, Dokumentations- und Integrationsprozesse für qualifizierte Fachkräfte im Schweizer Bausektor.",
sui1_t:"Auswahl von Profilen",
sui1_p:"Vorauswahl von Maurern, Bauhelfern, Facharbeitern und technischen Profilen nach den tatsächlichen Anforderungen jedes Unternehmens.",
sui2_t:"Dokumentenmanagement",
sui2_p:"Unterstützung bei Dokumenten, Bewilligungen, Lebensläufen, administrativer Koordination und Vorbereitung der Integration.",
sui3_t:"Professionelle Integration",
sui3_p:"Begleitung bei Interviews, erster Logistik, Arbeitsbedingungen und Anpassung an das Schweizer Arbeitsumfeld.",
serv_t:"Dienstleistungen",
serv1_t:"Bau und Renovierung",
serv1_p:"Komplettrenovierungen, kleinere Bauarbeiten, Geschäftslokale, Wohnungen, Trockenbau, Malerarbeiten, Böden und Ausbau.",
serv2_t:"Lösungen für Unternehmen",
serv2_p:"Unterstützung für Unternehmen, die Personal, professionelle Koordination und strukturierte Integrationsprozesse benötigen.",
serv3_t:"Komplette Begleitung",
serv3_p:"Direkter Kontakt, Planung, Nachverfolgung und klare Kommunikation während des gesamten Arbeitsprozesses.",
qs_t:"Über uns",
qs_1:"CHL Constructora entstand aus direkter Erfahrung im Bausektor und praktischem Wissen über den spanischen und schweizerischen Markt.",
qs_2:"Wir arbeiten mit einer klaren Vision: seriöse, professionelle und gut koordinierte Lösungen – sowohl bei Renovierungen und Bauarbeiten als auch bei Fachkräfteprozessen.",
qs_3:"Unsere Priorität ist Vertrauen, Transparenz und Zuverlässigkeit in jedem Projekt.",
contact_t:"Kontakt",
contact_1:"Für Offerten, Bauprojekte oder Informationen über Personal für die Schweiz können Sie uns direkt per WhatsApp kontaktieren.",
btn_whatsapp:"Über WhatsApp kontaktieren"
}
};

function toggleLanguage(){
currentLang = currentLang === "es" ? "de" : "es";

document.querySelectorAll("[data-i]").forEach(el=>{
let key = el.getAttribute("data-i");
el.innerHTML = translations[currentLang][key];
});
}
</script>

</body>
</html>
