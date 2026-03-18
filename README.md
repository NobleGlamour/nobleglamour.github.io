
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Noble Glamour – Britisch Kurzhaar Hobbyzucht</title>

<!-- Webfonts (falls lokal nicht vorhanden, kannst du dies z. B. mit Google Fonts ersetzen) -->
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Lato:wght@400;600;700&display=swap" rel="stylesheet">

<style>
    :root{
   		--LightGold_Hell: #F9EEC7;
        --LightGold_Mittel: #F1DFA2; 
        --Light_Dunkel: #E6C96A;
        --Gold_Hell: #DBB84F;
        --Gold_Mittel: #D4AF37;
        --Gold_Dunkel: #BD982F; 
        --Bronze_Hell: #A7812A; 
        --Bronze_Mittel: #8A6823; 
        --Bronze_Dunkel: #6C511C;
	    --black:#000000;
        --white:#ffffff;
    }

    /* ====== Base ====== */
    *{ box-sizing:border-box; }
    html,body{ margin:0; padding:0; }
    body{
        font-family:Calibri, "Segoe UI", Arial, Helvetica, sans-serif;
        color:var(--black);
        background:var(--white);
        line-height:1.6;
    }
    h1,h2,h3{
        font-family: Calibri, "Segoe UI", Arial, Helvetica, sans-serif;
        color:var(--Gold_Mittel);
        margin:0 0 .6em 0;
        line-height:1.25;
    }
    p{ margin:0 0 1em 0; }
    a{ color:var(--Gold_Mittel); text-decoration:none; }
    .container{ max-width:1200px; margin:0 auto; padding:0 20px; }
    .section{ padding:70px 0; }
    .LightGold_Hell{ background:var(--LightGold_Hell); }
    .btn{
        display:inline-block;
        padding:12px 20px;
        border:2px solid var(--Gold_Mittel);
        color:var(--black);
        background:transparent;
        font-weight:700;
        border-radius:4px;
        transition:.25s ease;
    }
    .btn:hover{ background:var(--black); color:var(--Gold_Mittel); }

    /* ====== Header / Navigation ====== */
    header{
        position:sticky; top:0; z-index:1000;
        background:var(--black); color:var(--Gold_Mittel);
        border-bottom:1px solid rgba(212,175,55,.25);
    }
    .nav{
        display:flex; align-items:center; justify-content:space-between;
        height:68px;
    }
    .logo{ font-weight:800; letter-spacing:.5px; }
    .logo span{ color:var(--Gold_Mittel); }
    nav ul{ list-style:none; margin:0; padding:0; display:flex; gap:18px; }
    nav a{ color:var(--Gold_Mittel); font-weight:700; }
    .burger{ display:none; cursor:pointer; color:var(--Gold_Mittel); }

    /* ====== Hero ====== */
    .hero{
        position:relative;
        background:url('hero.jpg') center/cover no-repeat;
        min-height:58vh;
        display:flex; align-items:center;
        text-align:center; color:var(--Gold_Mittel);
    }
    .hero::after{
        content:""; position:absolute; inset:0;
        background:linear-gradient(180deg, rgba(250,238,200,.35), rgba(250,238,200,.55));
    }
    .hero-inner{
        position:relative; z-index:1; width:100%;
        padding:80px 20px;
    }
    .hero h1{ font-size:clamp(2rem, 4.5vw, 3.2rem); margin-bottom:.25em; }
    .hero p{ color:#D4AF37; font-weight:600; margin-bottom:1em; }
    .hero .btn{ background:var(--Gold_Mittel); color:var(--black); border-color:var(--Gold_Mittel); }

    /* ====== Grids ====== */
    .cards{
        display:grid; grid-template-columns:repeat(12, 1fr); gap:24px;
    }
    .card{ grid-column:span 6; background:var(--white); border:1px solid #e9e9e9; border-radius:8px; overflow:hidden; box-shadow:0 2px 10px rgba(0,0,0,.04); }
    .card img{ width:100%; aspect-ratio:4/3; object-fit:cover; display:block; }
    .card-body{ padding:18px; }

    /* ====== Kontakt / Formulare ====== */
    .contact-form{
        max-width:680px; margin:30px auto 0 auto;
        display:flex; flex-direction:column; gap:14px;
    }
    .contact-form label{ font-weight:700; color:var(--black); }
    .contact-form input,
    .contact-form select,
    .contact-form textarea{
        padding:12px 14px; font-size:16px;
        border:2px solid var(--Gold_Mittel); border-radius:4px; background:var(--white);
    }
    .contact-form textarea{ min-height:140px; resize:vertical; }
    .checkbox{ display:flex; align-items:center; gap:10px; font-size:14px; }
    .submit-btn{
        background:var(--Gold_Mittel); color:var(--black); border:none;
        padding:14px 20px; font-weight:800; cursor:pointer; border-radius:4px; transition:.25s ease;
    }
    .submit-btn:hover{ background:var(--black); color:var(--Gold_Mittel); }
    .hint{ font-size:13px; color:var(--black); opacity:.85; }

    /* ====== Footer ====== */
    footer{ background:var(--black); color:#D4AF37; }
    footer a{ color:#D4AF37; text-decoration:underline; }

    /* ====== Responsive ====== */
    @media (max-width:900px){
        .card{ grid-column:span 12; }
    }
    @media (max-width:800px){
        nav ul{ display:none; position:absolute; top:68px; right:0; left:0; background:var(--black); padding:18px; border-bottom:1px solid rgba(212,175,55,.25); }
        nav ul.open{ display:flex; flex-direction:column; gap:14px; }
        .burger{ display:block; }
    }
</style>
</head>
<body>

<!-- ====== Header / Nav ====== -->
<header>
    <div class="container nav">
        <div class="burger" id="burger">☰ Menü</div>
        <nav>
            <ul id="menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#katzen">Katzen</a></li>
                <li><a href="#zucht">Zucht</a></li>
                <li><a href="#kitten">Kitten</a></li>
                <li><a href="#galerie">Galerie</a></li>
                <li><a href="#warteliste">Warteliste</a></li>
                <li><a href="#kontakt">Kontakt</a></li>
            </ul>
        </nav>
    </div>
</header>

<!-- ====== Hero ====== -->
<section class="hero" id="home">
    <div class="hero-inner container">
	    <img src="Logo ohne Banner Entwurf Stufe 8 Gold 600dpi.png.png" alt="Noble Glamour Logo" />
		<div class="card-body">
		</div>
	    <h1>NOBLE GLAMOUR</h1>
        <p>Britisch Kurzhaar Hobbyzucht</p>
        <a class="btn" href="#katzen">Zu unseren Katzen</a>
    </div>
</section>

<!-- ====== Willkommen / Philosophie ====== -->
<section class="section LightGold_Hell">
    <div class="container">
        <h2>Willkommen bei Noble Glamour</h2>
        <p>Wie schön, dass Sie den Weg zu unseren bezaubernden Britisch Kurzhaar Katzen gefunden haben.
		   Wir sind eine kleine, liebevolle Hobbyzucht aus Köln. 
		   Unser Anspruch: Wohlbefinden der Tiere, offene Kommunikation mit Interessenten, 
           und eine Zucht, die langfristig verantwortungsvoll geplant ist.
		   Wir haben uns besonders auf den exklusiven Goldvarianten dieser wundervollen Rasse fokussiert. 
		   Mit Hingabe, Erfahrung und großer Verantwortung begleiten wir unsere Katzen von Anfang an.
		   Unsere kleinen Samtpfoten wachsen mit viel Liebe, Fürsorge und vollständig in unseren Familienalltag eingebunden auf.
		   Wir wünschen Ihnen viel Freude beim Stöbern auf unserer Website und beim Entdecken unserer liebenswerten Fellnasen.
           Herzlichst,
           Noble Glamour
		</p>
    </div>
</section>

<!-- ====== Unsere Katzen (Teaser) ====== -->
<section class="section" id="katzen">
    <div class="container">
        <h2>Unsere Katzen</h2>
        <div class="cards" style="margin-top:24px;">
            <article class="card">
                <img src="scarlett.jpg" alt="Scarlett Noble Azure – Golden Shell" />
                <div class="card-body">
                    <h3>Scarlett Noble Azure · BRI ny12</h3>
                    <p>Black Golden Shell – DNA getestet; HCM/PKD geprüft - ruhig und gelassen. </p>
                </div>
            </article>
            <article class="card">
                <img src="conny.jpg" alt="Conny von Schnurrkätzchen – Golden Shell" />
                <div class="card-body">
                    <h3>Conny von Schnurrkätzchen · BRI ny12</h3>
                    <p>Black Golden Shell – DNA getestet; HCM/PKD geprüft - kommunikativ und verspielt. </p>
                </div>
            </article>
        </div>
    </div>
</section>

<!-- ====== Zucht / Genetik ====== -->
<section class="section LightGold_Hell" id="zucht">
    <div class="container">
        <h2>Wissenschaftlich fundierte Zucht</h2>
        <p>Wir züchten mit Fokus auf Gesundheit, Wesen und rassetypische Eleganz. 
		   Alle Zuchttiere werden gemäß den Empfehlungen auf <strong>HCM</strong>, <strong>PKD</strong>, 
           <strong>FeLV</strong> und <strong>FIV</strong> untersucht. Zudem nutzen wir DNA Tests (u.a. PKD1, PRA, SMA) 
           und berücksichtigen Farbgene (Agouti, Wideband, Inhibitor, Point), um unsere Zuchtziele verantwortungsvoll zu erreichen. 
		   Selbstverständlich liegt der vollständige Stammbaum vor und kann auf Wunsch bereitgestellt werden.</p>
        <p class="hint">Hinweis: Blutgruppenbestimmung beider Elterntiere zur Vermeidung neonataler Isoerythrolyse ist fester Bestandteil unserer Abläufe.</p>
    </div>
</section>

<!-- ====== Kitten (Teaser) ====== -->
<section class="section" id="kitten">
    <div class="container">
        <h2>Unsere Kitten</h2>
        <p>Die Sozialisation im geborgenen Familienalltag bietet den bestmöglichen Start ins Leben. 
           Mit vollständig transparenten Gesundheitsnachweisen schaffen wir zusätzlich Klarheit und Vertrauen. 
           Interessiert? Trag dich in unsere <a href="#warteliste"><strong>Warteliste</strong></a> ein.</p>
    </div>
</section>

<!-- ====== Galerie (Platzhalter) ====== -->
<section class="section LightGold_Hell" id="galerie">
    <div class="container">
        <h2>Galerie</h2>
        <p>Bald folgen hier aktuelle Eindrücke unserer Katzen & Kitten.</p>
    </div>
</section>

<!-- ====== Warteliste – Formular ====== -->
<section class="section" id="warteliste">
    <div class="container">
        <h2>Warteliste für Kitten</h2>
        <p>Trage dich unverbindlich in unsere Warteliste ein. Wir melden uns, sobald passende Kitten verfügbar sind.</p>

        <form class="contact-form" id="waitlistForm" novalidate>
            <label for="wl-name">Vollständiger Name*</label>
            <input type="text" id="wl-name" name="name" required>

            <label for="wl-email">E-Mail-Adresse*</label>
            <input type="email" id="wl-email" name="email" required>

            <label for="wl-telefon">Telefonnummer (optional)</label>
            <input type="text" id="wl-telefon" name="telefon" inputmode="tel" placeholder="+49 …">

            <label for="wl-farbe">Wunschfarbe</label>
            <select id="wl-farbe" name="farbe">
                <option value="">Keine Präferenz</option>
                <option value="ny11">Golden Shaded (ny11)</option>
                <option value="ny12">Golden Shell (ny12)</option>
                <option value="ny25">Golden Ticked (ny25)</option>
                <option value="ny23">Golden Mackerel Tabby (ny23)</option>
                <option value="ny22">Golden Classic Tabby (ny22)</option>
                <option value="ny24">Golden Spotted (ny24)</option>
                <option value="33">Golden Point (ny11/12/25 33)</option>
            </select>

            <label for="wl-geschlecht">Gewünschtes Geschlecht</label>
            <select id="wl-geschlecht" name="geschlecht">
                <option value="">Keine Präferenz</option>
                <option value="weiblich">Weiblich</option>
                <option value="männlich">Männlich</option>
            </select>

            <label for="wl-ziel">Wunsch: Zucht oder Liebhaber?</label>
            <select id="wl-ziel" name="ziel">
                <option value="">Keine Präferenz</option>
                <option value="liebhaber">Liebhabertier</option>
                <option value="zucht">Zuchttier</option>
            </select>

            <label for="wl-erfahrung">Katzenerfahrung</label>
            <select id="wl-erfahrung" name="erfahrung">
                <option value="">Bitte auswählen</option>
                <option value="viel">Ich habe viel Erfahrung</option>
                <option value="mittel">Ich habe etwas Erfahrung</option>
                <option value="keine">Ich bin Erstkatzenhalter/in</option>
            </select>

            <label for="wl-nachricht">Nachricht oder Wünsche</label>
            <textarea id="wl-nachricht" name="nachricht" placeholder="Erzähl uns gerne etwas über dein Zuhause :)"></textarea>

            <label class="checkbox">
                <input type="checkbox" id="wl-dsgvo" required>
                Ich stimme der Verarbeitung meiner Daten gemäß <a href="#datenschutz">Datenschutzerklärung</a> zu.
            </label>

            <button type="submit" class="btn submit-btn">In Warteliste eintragen</button>
            <p id="wl-feedback" class="hint" role="status" aria-live="polite" style="display:none;"></p>
        </form>
    </div>
</section>

<!-- ====== Kontakt (einfaches Formular) ====== -->
<section class="section LightGold_Hell" id="kontakt">
    <div class="container">
        <h2>Kontakt</h2>
        <p>Fragen? Schreib uns gern – wir melden uns zeitnah.</p>

        <form class="contact-form" id="contactForm" novalidate>
            <label for="ct-name">Name*</label>
            <input type="text" id="ct-name" name="name" required>

            <label for="ct-email">E-Mail*</label>
            <input type="email" id="ct-email" name="email" required>

            <label for="ct-betreff">Betreff</label>
            <input type="text" id="ct-betreff" name="betreff">

            <label for="ct-nachricht">Nachricht*</label>
            <textarea id="ct-nachricht" name="nachricht" required></textarea>

            <label class="checkbox">
                <input type="checkbox" id="ct-dsgvo" required>
                Ich stimme der Verarbeitung meiner Daten gemäß <a href="#datenschutz">Datenschutzerklärung</a> zu.
            </label>

            <button type="submit" class="btn submit-btn">Nachricht senden</button>
            <p id="ct-feedback" class="hint" role="status" aria-live="polite" style="display:none;"></p>
        </form>
    </div>
</section>

<!-- ====== Footer ====== -->
<footer class="section">
    <div class="container" style="display:flex; flex-direction:column; gap:10px;">
        <div style="color:var(--gold); font-weight:800;">Mitglied bei CatManiac e.V.</div>
        <div style="display:flex; gap:16px; flex-wrap:wrap;">
            <a href="#impressum">Impressum</a>
            <a href="#datenschutz" id="datenschutz">Datenschutz</a>
        </div>
        <div style="opacity:.7; font-size:13px;">© <span id="year"></span> NOBLE GLAMOUR | Britisch Kurzhaar Hobbyzucht</div>
    </div>
</footer>

<!-- ====== Kleine JS-Helfer (Menü + Dummy-Submit für Preview) ====== -->
<script>
    // Jahr im Footer
    document.getElementById('year').textContent = new Date().getFullYear();

    // Mobile Menü
    const burger = document.getElementById('burger');
    const menu = document.getElementById('menu');
    burger?.addEventListener('click', () => menu.classList.toggle('open'));

    // Dummy-Submit (Preview): verhindert echtes Absenden und zeigt Feedback
    function hookForm(formId, feedbackId, successText){
        const form = document.getElementById(formId);
        const fb = document.getElementById(feedbackId);
        form?.addEventListener('submit', (e) => {
            e.preventDefault();
            if(!form.checkValidity()){
                form.reportValidity();
                return;
            }
            fb.style.display = 'block';
            fb.textContent = successText + ' (Preview). In der Live-Version richte ich dir E-Mail-Versand/Sheet-Speicherung ein.';
            form.reset();
        });
    }
    hookForm('waitlistForm','wl-feedback','Vielen Dank! Du wurdest auf die Warteliste gesetzt.');
    hookForm('contactForm','ct-feedback','Danke für deine Nachricht!');

</script>

</body>
</html>
``

