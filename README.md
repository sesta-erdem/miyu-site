# Miyu — Kara Kedi Tribute Sitesi 🐈‍⬛

Vintage soul / plak şirketi temalı, tek sayfalık tribute sitesi.
`index.html` + `img/` klasöründen oluşur; basit bir Node sunucusuyla (`server.js`) yayınlanır.

## Yerelde çalıştırma

İki yol var:

1. **En basit:** `index.html`'e çift tıkla, tarayıcıda açılır.
2. **Sunucuyla:**
   ```bash
   npm start
   ```
   Ardından tarayıcıda `http://localhost:3000` adresini aç.

> Müzik (Spotify) için internet gerekir. Site açıldığında çıkan ekrandan
> "Plağı çalmak için dokun" deyince Mitski şarkısı başlar (tarayıcılar sesi
> ilk dokunuştan önce başlatmaya izin vermez).

---

## 1) GitHub'a yükleme

Bu klasörün içinde, terminalde:

```bash
git init
git add .
git commit -m "Miyu tribute sitesi"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADIN/miyu-site.git
git push -u origin main
```

(`KULLANICI_ADIN/miyu-site` yerine kendi GitHub repo adresini yaz. Önce
GitHub'da boş bir repo oluştur: github.com/new)

---

## 2) Railway'e deploy (railway.com)

1. **railway.com**'a giriş yap → **New Project**.
2. **Deploy from GitHub repo** → yukarıda oluşturduğun repoyu seç.
3. Railway, `package.json`'ı görüp otomatik olarak Node uygulaması olarak
   algılar ve `npm start` komutuyla başlatır. Ekstra ayar gerekmez —
   `server.js` Railway'in verdiği `PORT` değişkenini kullanır.
4. Deploy bitince **Settings → Networking → Generate Domain** ile
   `*.up.railway.app` adresini al. Site canlı! 🎉

---

## Alternatif: GitHub Pages (sunucusuz, ücretsiz)

Statik bir site olduğu için Railway yerine GitHub Pages de yeter:

1. Repo'yu GitHub'a yükle (yukarıdaki adım 1).
2. Repo → **Settings → Pages**.
3. **Source: Deploy from a branch**, **Branch: main / (root)** → **Save**.
4. Birkaç dakika sonra `https://KULLANICI_ADIN.github.io/miyu-site/`
   adresinde yayında olur.

---

## İçindekiler

- `index.html` — sitenin tamamı (CSS + JS gömülü)
- `img/` — 95 optimize edilmiş fotoğraf
- `server.js` — sıfır bağımlılıklı statik sunucu (Railway için)
- `package.json` — `npm start` komutu
- `miyu_tek_dosya.html` — *(repoya dahil değil)* tüm görseller gömülü tek
  dosyalık sürüm; paylaşmak/çevrimdışı açmak için
