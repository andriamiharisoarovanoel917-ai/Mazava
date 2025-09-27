<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mazava - La lumière des créatifs</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
<style>
  * { margin:0; padding:0; box-sizing:border-box; font-family: 'Montserrat', sans-serif; scroll-behavior:smooth;}
  body { background:#fff; color:#333; line-height:1.6; overflow-x:hidden;}

  /* HEADER */
  header { display:flex; justify-content:space-between; align-items:center; padding:20px; background:#f7c948; position:sticky; top:0; z-index:100; }
  header h1 { font-size:28px; font-weight:700; color:#fff; }
  nav a { margin-left:20px; font-weight:600; color:#fff; transition:0.3s; }
  nav a:hover { color:#333; }

  /* HERO */
  .hero { display:flex; flex-direction:column; justify-content:center; align-items:center; height:80vh; background:#333 url('https://via.placeholder.com/1600x600.png?text=Mazava+Hero') center/cover no-repeat; color:#fff; text-align:center; }
  .hero h2 { font-size:40px; margin-bottom:20px; text-shadow:2px 2px 4px rgba(0,0,0,0.6); opacity:0; transform:translateY(20px); transition:0.8s ease-in-out;}
  .hero p { font-size:20px; margin-bottom:30px; text-shadow:1px 1px 3px rgba(0,0,0,0.5); opacity:0; transform:translateY(20px); transition:0.8s ease-in-out 0.2s;}
  .hero button { padding:15px 35px; font-size:16px; border:none; background:#f7c948; color:#333; cursor:pointer; border-radius:5px; transition:0.3s; opacity:0; transform:translateY(20px); transition:0.8s ease-in-out 0.4s;}
  .hero button:hover { background:#fff; color:#f7c948; }

  /* Sections */
  section { padding:80px 20px; max-width:1200px; margin:0 auto; opacity:0; transform:translateY(20px); transition:0.8s ease-in-out; }
  section h2 { font-size:32px; text-align:center; margin-bottom:50px; color:#f7c948; }

  /* Offres */
  .plans { display:flex; flex-wrap:wrap; justify-content:center; gap:30px; }
  .plan { border:2px solid #f7c948; border-radius:15px; padding:40px 30px; width:300px; text-align:center; transition: transform 0.3s, box-shadow 0.3s; background:#fff;}
  .plan:hover { transform: translateY(-10px); box-shadow:0 10px 25px rgba(0,0,0,0.2); }
  .plan h3 { font-size:24px; margin-bottom:20px; color:#f7c948; }
  .plan p { margin-bottom:25px; font-size:16px; }
  .plan button { padding:12px 25px; border:none; background:#f7c948; color:#333; font-weight:700; cursor:pointer; border-radius:5px; transition:0.3s;}
  .plan button:hover { background:#fff; color:#f7c948; }

  /* Bibliothèque */
  .library { display:grid; grid-template-columns:repeat(auto-fit, minmax(250px, 1fr)); gap:25px; }
  .item { border-radius:15px; overflow:hidden; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition:0.3s; background:#fff; }
  .item:hover { transform: translateY(-5px); box-shadow:0 10px 25px rgba(0,0,0,0.2);}
  .item img { width:100%; display:block; }
  .item h4 { padding:15px; font-size:18px; color:#f7c948; }
  .item button { margin:0 15px 15px 15px; padding:10px 15px; border:none; background:#f7c948; color:#333; border-radius:5px; cursor:pointer; transition:0.3s;}
  .item button:hover { background:#fff; color:#f7c948; }

  /* Fidélité & Bonus */
  .bonus { display:flex; flex-wrap:wrap; justify-content:center; gap:20px; }
  .bonus-card { border:2px solid #f7c948; border-radius:15px; padding:25px; width:250px; text-align:center; transition:0.3s; background:#fff; }
  .bonus-card:hover { transform: translateY(-5px); box-shadow:0 10px 25px rgba(0,0,0,0.2);}
  .bonus-card h4 { font-size:20px; margin-bottom:15px; color:#f7c948; }
  .bonus-card p { font-size:16px; }

  /* Témoignages */
  .testimonials { display:grid; grid-template-columns:repeat(auto-fit, minmax(250px,1fr)); gap:25px; }
  .testimonial { padding:20px; border-radius:15px; background:#f7c948; color:#fff; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition:0.3s; }
  .testimonial:hover { transform: translateY(-5px); }

  /* Contact */
  .contact form { display:flex; flex-direction:column; max-width:500px; margin:0 auto; }
  .contact input, .contact textarea { padding:12px; margin-bottom:20px; border:1px solid #ccc; border-radius:7px; font-size:16px; }
  .contact button { padding:15px; border:none; background:#f7c948; color:#333; cursor:pointer; border-radius:5px; font-weight:700; transition:0.3s; }
  .contact button:hover { background:#fff; color:#f7c948; }

  /* Footer */
  footer { background:#333; color:#fff; text-align:center; padding:25px; font-size:14px; }

  /* Responsive */
  @media(max-width:768px){
    header { flex-direction:column; }
    nav a { margin:10px 0 0 0; }
    .hero h2 { font-size:28px; }
    .hero p { font-size:16px; }
  }
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <h1>Mazava</h1>
  <nav>
    <a href="#offres">Offres</a>
    <a href="#library">Bibliothèque</a>
    <a href="#bonus">Bonus</a>
    <a href="#testimonials">Témoignages</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<!-- HERO -->
<div class="hero">
  <h2>La lumière des créatifs</h2>
  <p>Templates, presets et musiques pour vos projets vidéo et graphiques</p>
  <button onclick="window.location.href='#offres'">Essai gratuit 7 jours</button>
</div>

<!-- OFFRES -->
<section id="offres">
  <h2>Nos Abonnements</h2>
  <div class="plans">
    <div class="plan">
      <h3>Essai gratuit</h3>
      <p>7 jours d’accès limité aux ressources de base</p>
      <button>S’inscrire</button>
    </div>
    <div class="plan">
      <h3>Plus - 20 000 Ar</h3>
      <p>Accès aux packs standards avec téléchargement illimité</p>
      <button>S’abonner</button>
    </div>
    <div class="plan">
      <h3>Pro - 30 000 Ar</h3>
      <p>Accès complet + bonus exclusifs mensuels</p>
      <button>S’abonner</button>
    </div>
  </div>
</section>

<!-- BIBLIOTHÈQUE -->
<section id="library">
  <h2>Bibliothèque de Ressources</h2>
  <div class="library">
    <div class="item">
      <img src="https://via.placeholder.com/300x200.png?text=Template+Video" alt="Template vidéo">
      <h4>Template DaVinci Resolve</h4>
      <button>Télécharger</button>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/300x200.png?text=Preset+Graphique" alt="Preset graphique">
      <h4>Preset Photoshop</h4>
      <button>Télécharger</button>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/300x200.png?text=Musique+Libre" alt="Musique libre">
      <h4>Morceau libre de droits</h4>
      <button>Télécharger</button>
    </div>
  </div>
</section>

<!-- BONUS / FIDÉLITÉ -->
<section id="bonus">
  <h2>Bonus & Fidélité</h2>
  <div class="bonus">
    <div class="bonus-card">
      <h4>3 mois</h4>
      <p>Pack bonus offert pour les abonnés réguliers</p>
    </div>
    <div class="bonus-card">
      <h4>6 mois</h4>
      <p>Tutoriels exclusifs pour les créatifs</p>
    </div>
    <div class="bonus-card">
      <h4>12 mois</h4>
      <p>Réduction spéciale pour votre fidélité</p>
    </div>
  </div>
</section>

<!-- TÉMOIGNAGES -->
<section id="testimonials">
  <h2>Témoignages</h2>
  <div class="testimonials">
    <div class="testimonial">
      <p>"Grâce à Mazava, j’ai amélioré mes montages vidéo et gagné beaucoup de temps !"</p>
      <strong>- Alex, Monteur</strong>
    </div>
    <div class="testimonial">
      <p>"Les presets Photoshop sont incroyables, mon flux de travail est beaucoup plus rapide."</p>
      <strong>- Lova, Graphiste</strong>
    </div>
    <div class="testimonial">
      <p>"Les templates DaVinci Resolve sont faciles à utiliser et super professionnels."</p>
      <strong>- Hery, Colorist</strong>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="contact">
  <h2>Contactez-nous</h2>
  <form>
    <input type="text" placeholder="Nom" required>
    <input type="email" placeholder="Email" required>
    <textarea placeholder="Votre message" rows="5" required></textarea>
    <button type="submit">Envoyer</button>
  </form>
</section>

<!-- FOOTER -->
<footer>
  &copy; 2025 Mazava - Tous droits réservés
</footer>

<script>
  // Animation scroll pour fade-in
  const sections = document.querySelectorAll('section, .hero h2, .hero p, .hero button');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if(entry.isIntersecting){
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });
  sections.forEach(sec => observer.observe(sec));
</script>

</body>
</html>
