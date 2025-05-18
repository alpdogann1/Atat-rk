# Atat-rk
import zipfile
import os

folder_name = '/mnt/data/ataturk_web_site'
os.makedirs(folder_name, exist_ok=True)

files = {
    "index.html": """
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Atatürk - Anasayfa</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="overlay"></div>
  <header>
    <nav>
      <ul>
        <li><a href="index.html" class="active">Anasayfa</a></li>
        <li><a href="sozler.html">Sözler</a></li>
        <li><a href="fotograflar.html">Fotoğraflar</a></li>
        <li><a href="videolar.html">Videolar</a></li>
        <li><a href="yorumlar.html">Yorumlar</a></li>
        <li><a href="sesler.html">Sesler</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="intro">
      <h1>Mustafa Kemal Atatürk</h1>
      <p>
        Türkiye Cumhuriyeti'nin kurucusu, büyük lider Mustafa Kemal Atatürk'ü tanıyın. 
        Yenilikçi fikirleri, liderliği ve cesareti ile Türkiye'nin modernleşmesinin mimarıdır.
      </p>
    </section>
  </main>

  <footer>
    <p>© 2025 Atatürk Web Sitesi</p>
  </footer>
</body>
</html>
""",
    "sozler.html": """
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Atatürk - Sözler</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="overlay"></div>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Anasayfa</a></li>
        <li><a href="sozler.html" class="active">Sözler</a></li>
        <li><a href="fotograflar.html">Fotoğraflar</a></li>
        <li><a href="videolar.html">Videolar</a></li>
        <li><a href="yorumlar.html">Yorumlar</a></li>
        <li><a href="sesler.html">Sesler</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="sozler">
      <h2>Atatürk’ün En Güzel Sözleri</h2>
      <ul>
        <li>"Yurtta sulh, cihanda sulh."</li>
        <li>"Egemenlik, kayıtsız şartsız milletindir."</li>
        <li>"Hayatta en hakiki mürşit ilimdir."</li>
        <li>"Beni görmek demek mutlaka yüzümü görmek değildir."</li>
        <li>"Muasır medeniyet seviyesinin üzerine çıkmak hedefimizdir."</li>
      </ul>
    </section>
  </main>

  <footer>
    <p>© 2025 Atatürk Web Sitesi</p>
  </footer>
</body>
</html>
""",
    "fotograflar.html": """
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Atatürk - Fotoğraflar</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="overlay"></div>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Anasayfa</a></li>
        <li><a href="sozler.html">Sözler</a></li>
        <li><a href="fotograflar.html" class="active">Fotoğraflar</a></li>
        <li><a href="videolar.html">Videolar</a></li>
        <li><a href="yorumlar.html">Yorumlar</a></li>
        <li><a href="sesler.html">Sesler</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="galeri">
      <h2>Atatürk Fotoğraf Galerisi</h2>
      <div class="grid">
        <img src="images/1.jpg" alt="Atatürk Fotoğraf 1" />
        <img src="images/2.jpg" alt="Atatürk Fotoğraf 2" />
        <img src="images/3.jpg" alt="Atatürk Fotoğraf 3" />
        <img src="images/4.jpg" alt="Atatürk Fotoğraf 4" />
      </div>
    </section>
  </main>

  <footer>
    <p>© 2025 Atatürk Web Sitesi</p>
  </footer>
</body>
</html>
""",
    "videolar.html": """
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Atatürk - Videolar</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="overlay"></div>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Anasayfa</a></li>
        <li><a href="sozler.html">Sözler</a></li>
        <li><a href="fotograflar.html">Fotoğraflar</a></li>
        <li><a href="videolar.html" class="active">Videolar</a></li>
        <li><a href="yorumlar.html">Yorumlar</a></li>
        <li><a href="sesler.html">Sesler</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="videolar">
      <h2>Atatürk Videoları</h2>
      <div class="video-container">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/jU0Jt2AIVyQ" 
        title="Atatürk Video" frameborder="0" allowfullscreen></iframe>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2025 Atatürk Web Sitesi</p>
  </footer>
</body>
</html>
""",
    "yorumlar.html": """
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Atatürk - Yorumlar</title>
  <link rel="stylesheet" href="style.css" />
  <script>
    function yorumEkle(e) {
      e.preventDefault();
      const isim = document.getElementById('isim').value.trim();
      const yorum = document.getElementById('yorum').value.trim();
      const yorumlarListesi = document.getElementById('yorumlar-listesi');
      if (!isim || !yorum) {
        alert('Lütfen isim ve yorum girin!');
        return;
      }
      const yorumlar = JSON.parse(localStorage.getItem('yorumlar') || '[]');
      yorumlar.push({ isim, yorum });
      localStorage.setItem('yorumlar', JSON.stringify(yorumlar));
      yorumListele();
      e.target.reset();
    }

    function yorumListele() {
      const yorumlarListesi = document.getElementById('yorumlar-listesi');
      yorumlarListesi.innerHTML = '';
      const yorumlar = JSON.parse(localStorage.getItem('yorumlar') || '[]');
      yorumlar.forEach(y => {
        const li = document.createElement('li');
        li.innerHTML = `<strong>${y.isim}</strong>: ${y.yorum}`;
        yorumlarListesi.appendChild(li);
      });
    }

    window.onload = yorumListele;
  </script>
</head>
<body>
  <div class="overlay"></div>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Anasayfa</a></li>
        <li><a href="sozler.html">Sözler</a></li>
        <li><a href="fotograflar.html">Fotoğraflar</a></li>
        <li><a href="videolar.html">Videolar</a></li>
        <li><a href="yorumlar.html" class="active">Yorumlar</a></li>
        <li><a href="sesler.html">Sesler</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="yorumlar">
      <h2>Atatürk Hakkında Yorumlarınız</h2>
      <form onsubmit="yorumEkle(event)">
        <input id="isim" type="text" placeholder="Adınız" required />
        <textarea id="yorum" placeholder="Yorumunuz" required></textarea>
        <button type="submit">Gönder</button>
      </form>
      <ul id="yorumlar-listesi"></ul>
    </section>
  </main>

  <footer>
    <p>© 2025 Atatürk Web Sitesi</p>
  </footer>
</body>
</html>
""",
    "sesler.html": """
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Atatürk - Sesler</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="overlay"></div>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Anasayfa</a></li>
        <li><a href="sozler.html
