<!DOCTYPE html>  
<html lang="fr">  
<head>  
<meta charset="UTF-8" />  
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>  
<title>Portfolio Pokémon - Nicolas Perey</title>  
  
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">  
  
<style>  
*{  
    margin:0;  
    padding:0;  
    box-sizing:border-box;  
}  
  
body{  
    font-family:'Poppins', sans-serif;  
    background:linear-gradient(135deg,#1f1147,#311b92,#0d47a1);  
    color:white;  
    overflow-x:hidden;  
}  
  
/* PARTICLES BACKGROUND */  
body::before{  
    content:"";  
    position:fixed;  
    width:200%;  
    height:200%;  
    background:  
    radial-gradient(circle,#ffffff22 2px, transparent 2px);  
    background-size:40px 40px;  
    animation:moveBg 30s linear infinite;  
    z-index:-1;  
}  
  
@keyframes moveBg{  
    from{transform:translate(0,0);}  
    to{transform:translate(-200px,-200px);}  
}  
  
.container{  
    width:95%;  
    max-width:1400px;  
    margin:auto;  
    padding:40px 20px;  
}  
  
header{  
    text-align:center;  
    margin-bottom:50px;  
}  
  
header h1{  
    font-size:4rem;  
    color:#ffeb3b;  
    text-shadow:0 0 20px #ffeb3b;  
}  
  
header h2{  
    font-size:1.5rem;  
    color:#fff;  
    margin-top:10px;  
}  
  
.card{  
    background:rgba(255,255,255,0.08);  
    border:1px solid rgba(255,255,255,0.2);  
    backdrop-filter:blur(10px);  
    border-radius:25px;  
    padding:30px;  
    margin-bottom:30px;  
    transition:0.4s;  
    position:relative;  
    overflow:hidden;  
}  
  
.card:hover{  
    transform:translateY(-8px) scale(1.01);  
    box-shadow:0 10px 30px rgba(0,0,0,0.4);  
}  
  
.card::before{  
    content:"";  
    position:absolute;  
    top:-50%;  
    left:-50%;  
    width:200%;  
    height:200%;  
    background:linear-gradient(  
    45deg,  
    transparent,  
    rgba(255,255,255,0.08),  
    transparent  
    );  
    transform:rotate(25deg);  
    animation:shine 6s infinite;  
}  
  
@keyframes shine{  
    0%{transform:translateX(-100%) rotate(25deg);}  
    100%{transform:translateX(100%) rotate(25deg);}  
}  
  
.grid{  
    display:grid;  
    grid-template-columns:repeat(auto-fit,minmax(320px,1fr));  
    gap:25px;  
}  
  
.section-title{  
    font-size:1.8rem;  
    margin-bottom:20px;  
    color:#ffeb3b;  
}  
  
.contact p,  
.profile p,  
.timeline p,  
.skills li,  
.interests li{  
    margin-bottom:10px;  
    line-height:1.6;  
}  
  
.timeline-item{  
    margin-bottom:25px;  
    padding-left:20px;  
    border-left:4px solid #ffeb3b;  
}  
  
.timeline-item h3{  
    color:#ffd54f;  
}  
  
.badges{  
    display:flex;  
    flex-wrap:wrap;  
    gap:12px;  
    margin-top:20px;  
}  
  
.badge{  
    background:linear-gradient(45deg,#ff9800,#ffeb3b);  
    color:#000;  
    padding:10px 18px;  
    border-radius:30px;  
    font-weight:600;  
    transition:0.3s;  
    cursor:pointer;  
}  
  
.badge:hover{  
    transform:scale(1.1);  
}  
  
/* EEVEE EVOLUTIONS */  
  
.evolutions{  
    display:flex;  
    flex-wrap:wrap;  
    justify-content:center;  
    gap:20px;  
    margin-top:30px;  
}  
  
.eevee-card{  
    width:160px;  
    height:220px;  
    border-radius:20px;  
    overflow:hidden;  
    position:relative;  
    transition:0.5s;  
    cursor:pointer;  
}  
  
.eevee-card img{  
    width:100%;  
    height:100%;  
    object-fit:cover;  
    transition:0.5s;  
}  
  
.eevee-card:hover img{  
    transform:scale(1.1);  
}  
  
.eevee-card:hover{  
    transform:translateY(-10px);  
    box-shadow:0 0 25px rgba(255,255,255,0.6);  
}  
  
.eevee-name{  
    position:absolute;  
    bottom:0;  
    width:100%;  
    text-align:center;  
    background:rgba(0,0,0,0.6);  
    padding:10px;  
    font-weight:bold;  
}  
  
footer{  
    text-align:center;  
    margin-top:40px;  
    padding:20px;  
    color:#ddd;  
}  
  
.glow{  
    animation:glow 2s infinite alternate;  
}  
  
@keyframes glow{  
    from{  
        text-shadow:0 0 10px #fff;  
    }  
    to{  
        text-shadow:0 0 20px #ffeb3b,  
                     0 0 40px #ffeb3b;  
    }  
}  
  
@media(max-width:768px){  
    header h1{  
        font-size:2.5rem;  
    }  
}  
</style>  
</head>  
  
<body>  
  
<div class="container">  
  
<header>  
    <h1 class="glow">⚡ RESPONSABLE VENDEUR ⚡</h1>  
    <h2>Nicolas Perey</h2>  
</header>  
  
<div class="grid">  
  
    <!-- CONTACT -->  
    <div class="card contact">  
        <h2 class="section-title">📞 Contacts</h2>  
        <p><strong>Nom :</strong> Nicolas Perey</p>  
        <p><strong>Date de naissance :</strong> 17/04/2003</p>  
        <p><strong>Téléphone :</strong> 06 02 38 03 06</p>  
        <p><strong>Email :</strong> nperey.17pro@gmail.com</p>  
        <p><strong>Permis :</strong> Permis B</p>  
        <p><strong>Adresse :</strong> 2160 Route du Col du Bouchet, 42155 Villemontais</p>  
    </div>  
  
    <!-- PROFIL -->  
    <div class="card profile">  
        <h2 class="section-title">✨ Profil</h2>  
        <p>  
            J’aime travailler avec une équipe ou en autonomie.  
            Durant mes trois dernières années j’ai su m’adapter aux différentes situations,  
            améliorant ainsi mon improvisation et ma capacité d’adaptation.  
        </p>  
  
        <p>  
            J’ai pu expérimenter la vente de produits dans un domaine dont j’ignorais les termes.  
            Je suis capable de comprendre et de m’exprimer aisément en anglais.  
        </p>  
    </div>  
  
</div>  
  
<!-- EXPERIENCES -->  
<div class="card">  
    <h2 class="section-title">🚀 Expériences Professionnelles</h2>  
  
    <div class="timeline">  
  
        <div class="timeline-item">  
            <h3>2025-2026 — Responsable Rayon | Brico Dépôt</h3>  
            <p>Alternance à Brico Dépôt Parigny en tant que vendeur conseil en menuiserie.</p>  
            <p>✔ Vente / Conseil clients</p>  
            <p>✔ Mise en rayon</p>  
            <p>✔ Port de charges lourdes</p>  
            <p>✔ Apprentissage termes techniques</p>  
        </div>  
  
        <div class="timeline-item">  
            <h3>2023-2025 — Responsable Adjoint / Vendeur | Stokomani</h3>  
            <p>Alternance à Stokomani Perreux.</p>  
            <p>✔ Mise en rayon</p>  
            <p>✔ Caisses</p>  
            <p>✔ Comptabilité</p>  
            <p>✔ Management d’équipe</p>  
        </div>  
  
        <div class="timeline-item">  
            <h3>2022 — Vendeur | Intermarché</h3>  
            <p>CDD à Intermarché Lentigny.</p>  
            <p>✔ Mise en rayon</p>  
            <p>✔ Drive</p>  
        </div>  
  
        <div class="timeline-item">  
            <h3>2021-2023 — Missions Intérim | Randstad</h3>  
            <p>Usines : Refresco, Mademoiselle Dessert, Tendance...</p>  
        </div>  
  
    </div>  
</div>  
  
<div class="grid">  
  
    <!-- FORMATIONS -->  
    <div class="card">  
        <h2 class="section-title">🎓 Formations</h2>  
  
        <div class="timeline-item">  
            <h3>2025-2026</h3>  
            <p>Bachelor — Chargé d’Affaires Commerciales</p>  
        </div>  
  
        <div class="timeline-item">  
            <h3>2023-2025</h3>  
            <p>BTS — Management Commercial Opérationnel</p>  
        </div>  
  
        <div class="timeline-item">  
            <h3>2018-2021</h3>  
            <p>Baccalauréat Général — Mathématiques / SES</p>  
        </div>  
    </div>  
  
    <!-- COMPETENCES -->  
    <div class="card skills">  
        <h2 class="section-title">💡 Compétences</h2>  
  
        <div class="badges">  
            <div class="badge">Service client</div>  
            <div class="badge">Autonome</div>  
            <div class="badge">Coopératif</div>  
            <div class="badge">Adaptabilité</div>  
            <div class="badge">OpenOffice</div>  
            <div class="badge">Management</div>  
            <div class="badge">Anglais</div>  
            <div class="badge">Projet Voltaire</div>  
        </div>  
  
        <p style="margin-top:20px;">  
            Certifié orthographe professionnelle — Projet Voltaire<br>  
            CSCV : RNCG73A  
        </p>  
    </div>  
  
</div>  
  
<!-- INTERETS -->  
<div class="card interests">  
    <h2 class="section-title">🎮 Centres d’intérêts</h2>  
  
    <div class="badges">  
        <div class="badge">⚽ Football</div>  
        <div class="badge">🎵 Musique</div>  
        <div class="badge">🎮 Jeux Vidéos</div>  
        <div class="badge">🐾 Animaux</div>  
    </div>  
</div>  
  
<!-- EEVEE SECTION -->  
<div class="card">  
    <h2 class="section-title">🌟 Évolutions d’Évoli</h2>  
  
    <div class="evolutions">  
  
        <div class="eevee-card">  
            <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/133.png">  
            <div class="eevee-name">Évoli</div>  
        </div>  
  
        <div class="eevee-card">  
            <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/134.png">  
            <div class="eevee-name">Aquali</div>  
        </div>  
  
        <div class="eevee-card">  
            <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/135.png">  
            <div class="eevee-name">Voltali</div>  
        </div>  
  
        <div class="eevee-card">  
            <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/136.png">  
            <div class="eevee-name">Pyroli</div>  
        </div>  
  
        <div class="eevee-card">  
            <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/196.png">  
            <div class="eevee-name">Mentali</div>  
        </div>  
  
        <div class="eevee-card">  
            <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/197.png">  
            <div class="eevee-name">Noctali</div>  
        </div>  
  
    </div>  
</div>  
  
<footer>  
    Portfolio interactif Pokémon • Nicolas Perey • 2026  
</footer>  
  
</div>  
  
<script>  
// Animation badges  
const badges = document.querySelectorAll(".badge");  
  
badges.forEach(badge => {  
    badge.addEventListener("mouseenter", () => {  
        badge.style.transform = "scale(1.15) rotate(2deg)";  
    });  
  
    badge.addEventListener("mouseleave", () => {  
        badge.style.transform = "scale(1)";  
    });  
});  
  
// Effet cartes Pokémon  
const cards = document.querySelectorAll(".eevee-card");  
  
cards.forEach(card => {  
    card.addEventListener("mousemove", (e) => {  
        const rect = card.getBoundingClientRect();  
        const x = e.clientX - rect.left;  
        const y = e.clientY - rect.top;  
  
        card.style.transform = `  
            rotateY(${(x - rect.width/2)/10}deg)  
            rotateX(${-(y - rect.height/2)/10}deg)  
            scale(1.08)  
        `;  
    });  
  
    card.addEventListener("mouseleave", () => {  
        card.style.transform = "rotateY(0) rotateX(0) scale(1)";  
    });  
});  
</script>  
  
</body>  
</html>  
