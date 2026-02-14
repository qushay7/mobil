<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lintas Sulawesi | Premium VIP Travel</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    
    <style>
        :root {
            --primary: #3b82f6; 
            --accent: #facc15; 
            --text-main: #f8fafc;
            --card-bg: rgba(30, 41, 59, 0.6); 
        }

        html { scroll-behavior: smooth; }
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Plus Jakarta Sans', sans-serif; }
        
        body { 
            margin: 0;
            padding-bottom: 160px;
            color: var(--text-main);
            background: linear-gradient(-45deg, #0f172a, #1e1b4b, #2e1065, #020617);
            background-size: 400% 400%;
            animation: darkGradient 12s ease infinite;
            min-height: 100vh;
        }

        @keyframes darkGradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container { max-width: 800px; margin: 0 auto; padding: 20px; }

        .hero { padding: 60px 20px 20px; text-align: center; }
        .hero h1 { font-size: 2.2rem; font-weight: 800; letter-spacing: -1px; margin-bottom: 5px; }
        .hero p { color: var(--primary); font-weight: 700; font-size: 0.9rem; text-transform: uppercase; letter-spacing: 2px; }

        .card {
            background: var(--card-bg);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 25px;
            margin-bottom: 25px;
            border: 1px solid rgba(255, 255, 255, 0.08);
            box-shadow: 0 20px 50px rgba(0,0,0,0.5);
        }

        h2 { font-size: 1.2rem; margin-bottom: 20px; display: flex; align-items: center; gap: 12px; color: var(--primary); }

        /* SOPIR & INFO */
        .driver-card { display: flex; align-items: center; gap: 15px; background: rgba(59, 130, 246, 0.1); padding: 15px; border-radius: 20px; margin-bottom: 15px; }
        .grid-manfaat { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        .m-item { font-size: 0.75rem; color: #94a3b8; display: flex; align-items: center; gap: 8px; }
        .m-item i { color: #10b981; }

        /* HARGA */
        .price-table { width: 100%; border-collapse: collapse; }
        .price-table th { text-align: left; padding: 12px; font-size: 0.7rem; color: #94a3b8; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .price-table td { padding: 15px 12px; border-bottom: 1px solid rgba(255,255,255,0.05); font-size: 0.85rem; }
        .val-vip { color: var(--accent); font-weight: 800; }

        /* ARMADA 2x2 */
        .armada-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 15px; }
        .armada-item { 
            background: rgba(255, 255, 255, 0.03); 
            border-radius: 24px; padding: 15px; text-align: center; 
            border: 1px solid rgba(255, 255, 255, 0.05); cursor: pointer; transition: 0.4s;
        }
        .armada-item:hover { transform: translateY(-8px); border-color: var(--primary); }
        .armada-item img { width: 100%; border-radius: 15px; height: 90px; object-fit: cover; margin-bottom: 10px; }

        /* TESTIMONI */
        .testi-scroll { display: flex; overflow-x: auto; gap: 15px; padding-bottom: 10px; scrollbar-width: none; }
        .testi-box { min-width: 250px; background: rgba(0,0,0,0.2); padding: 15px; border-radius: 20px; border-left: 4px solid var(--primary); }
        .testi-box p { font-size: 0.8rem; font-style: italic; color: #cbd5e1; }
        .testi-box b { font-size: 0.75rem; color: var(--accent); }

        /* FAQ */
        .faq-item { background: rgba(255,255,255,0.02); padding: 12px; border-radius: 15px; margin-bottom: 10px; }
        .faq-item b { font-size: 0.85rem; color: var(--primary); display: block; }
        .faq-item p { font-size: 0.8rem; color: #94a3b8; }

        /* FORM */
        .field { margin-bottom: 15px; }
        label { font-size: 0.75rem; color: #94a3b8; font-weight: 700; display: block; margin-bottom: 8px; }
        input, select, textarea { 
            width: 100%; padding: 16px; border-radius: 16px; border: 1px solid rgba(255,255,255,0.1); 
            background: rgba(15, 23, 42, 0.8); color: white; font-size: 0.9rem; outline: none;
        }
        .btn-kirim {
            background: var(--primary); color: white; padding: 18px; border: none; 
            border-radius: 20px; font-weight: 800; width: 100%; cursor: pointer;
            box-shadow: 0 10px 25px rgba(59, 130, 246, 0.4);
        }

        /* FLOATING NAV HOME TENGAH */
        .bottom-nav {
            position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 450px; background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(20px); display: flex; justify-content: space-around; align-items: center;
            padding: 10px 15px; border-radius: 50px; border: 1px solid rgba(255,255,255,0.15); z-index: 9999;
            box-shadow: 0 25px 50px rgba(0,0,0,0.8);
        }
        .nav-item { color: #64748b; text-decoration: none; text-align: center; font-size: 0.65rem; font-weight: 700; flex: 1; transition: 0.3s; }
        .nav-item i { display: block; font-size: 1.3rem; margin-bottom: 4px; }

        .nav-home {
            background: var(--primary); color: white !important;
            width: 80px; height: 80px; border-radius: 50%;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            margin-top: -55px; border: 7px solid #0f172a;
            box-shadow: 0 15px 30px rgba(59, 130, 246, 0.6);
        }
        .nav-home i { font-size: 2rem !important; margin: 0 !important; }

        /* WARNA AKTIF */
        .nav-item:active { color: var(--accent); }
        .nav-home:active { background: var(--accent); transform: scale(0.9) translateY(-40px); }

    </style>
</head>
<body>

<div class="hero" id="home">
    <h1>LINTAS SULAWESI</h1>
    <p>Premium VIP Transport</p>
</div>

<div class="container">
    
    <div class="card" id="tentang">
        <h2><i class="fas fa-id-badge"></i> Kenapa Harus Kami?</h2>
        <div class="driver-card">
            <i class="fas fa-steering-wheel" style="font-size: 2rem; color: var(--accent);"></i>
            <div>
                <b style="font-size: 0.9rem; color: var(--accent);">Sopir Berpengalaman</b>
                <p style="font-size: 0.75rem; color: #cbd5e1;">Ramah, jujur, dan paham rute Sulawesi dengan sangat baik.</p>
            </div>
        </div>
        <div class="grid-manfaat">
            <div class="m-item"><i class="fas fa-check-circle"></i> Berpakaian Rapi & Wangi</div>
            <div class="m-item"><i class="fas fa-check-circle"></i> Tidak Merokok di Mobil</div>
            <div class="m-item"><i class="fas fa-check-circle"></i> Antar Jemput Depan Rumah</div>
            <div class="m-item"><i class="fas fa-check-circle"></i> Full AC & Musik</div>
        </div>
    </div>

    <div class="card" id="harga">
        <h2><i class="fas fa-tags"></i> Daftar Tarif Per Kursi</h2>
        <table class="price-table">
            <thead>
                <tr><th>RUTE PERJALANAN</th><th>STD</th><th>VIP</th></tr>
            </thead>
            <tbody>
                <tr><td>Wajo ↔ Makassar</td><td>200rb</td><td class="val-vip">220rb</td></tr>
                <tr><td>Wajo ↔ Sinjai</td><td>150rb</td><td class="val-vip">170rb</td></tr>
                <tr><td>Sinjai ↔ Makassar</td><td>180rb</td><td class="val-vip">200rb</td></tr>
            </tbody>
        </table>
    </div>

    <div class="card" id="mobil">
        <h2><i class="fas fa-car"></i> Pilih Armada Kami</h2>
        <div class="armada-grid">
            <div class="armada-item" onclick="pilihMobil('Pajero Sport (VIP)')">
                <img src="https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?auto=format&fit=crop&w=300&q=80">
                <h4 style="font-size: 0.75rem;">Pajero Sport</h4>
            </div>
            <div class="armada-item" onclick="pilihMobil('Innova Reborn')">
                <img src="https://images.unsplash.com/photo-1605559424843-9e4c228bf1c2?auto=format&fit=crop&w=300&q=80">
                <h4 style="font-size: 0.75rem;">Innova Reborn</h4>
            </div>
            <div class="armada-item" onclick="pilihMobil('Toyota Veloz')">
                <img src="https://images.unsplash.com/photo-1619682817481-e994891cd1f5?auto=format&fit=crop&w=300&q=80">
                <h4 style="font-size: 0.75rem;">Toyota Veloz</h4>
            </div>
            <div class="armada-item" onclick="pilihMobil('Toyota Avanza')">
                <img src="https://images.unsplash.com/photo-1590362891991-f776e747a588?auto=format&fit=crop&w=300&q=80">
                <h4 style="font-size: 0.75rem;">Avanza</h4>
            </div>
        </div>
    </div>

    <div class="card">
        <h2><i class="fas fa-star"></i> Testimoni</h2>
        <div class="testi-scroll">
            <div class="testi-box"><p>"Pajero-nya sangat nyaman, sopirnya ramah."</p><b>- Ibu Sari, Makassar</b></div>
            <div class="testi-box"><p>"Tepat waktu jemput di depan rumah."</p><b>- Pak Andi, Wajo</b></div>
            <div class="testi-box"><p>"Travel paling bersih yang pernah saya naik."</p><b>- Budi, Sinjai</b></div>
        </div>
    </div>

    <div class="card">
        <h2><i class="fas fa-question-circle"></i> Tanya Jawab</h2>
        <div class="faq-item"><b>Berapa kali jadwal keberangkatan?</b><p>Pagi jam 08.00, Siang 13.00, dan Malam 19.00 WITA.</p></div>
        <div class="faq-item"><b>Bisa carter satu mobil?</b><p>Bisa, silakan hubungi admin untuk harga spesial carter.</p></div>
    </div>

    <div class="card" id="pesan">
        <h2><i class="fas fa-clipboard-check"></i> Form Booking</h2>
        <div class="field"><label>Nama Lengkap</label><input type="text" id="nama" placeholder="Ketik nama..."></div>
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px;">
            <div class="field">
                <label>Pilih Unit</label>
                <select id="mobil_pilihan">
                    <option>Innova Reborn</option>
                    <option>Pajero Sport (VIP)</option>
                    <option>Toyota Veloz</option>
                </select>
            </div>
            <div class="field">
                <label>Rute</label>
                <select id="rute">
                    <option>Wajo - Makassar</option>
                    <option>Wajo - Sinjai</option>
                    <option>Sinjai - Makassar</option>
                </select>
            </div>
        </div>
        <div class="field"><label>Alamat Penjemputan</label><textarea id="alamat" placeholder="Alamat lengkap..."></textarea></div>
        <button class="btn-kirim" onclick="kirimWhatsApp()">DAFTAR VIA WHATSAPP</button>
    </div>

</div>

<nav class="bottom-nav">
    <a href="#harga" class="nav-item"><i class="fas fa-tags"></i>Tarif</a>
    <a href="#mobil" class="nav-item"><i class="fas fa-car"></i>Unit</a>
    <a href="#home" class="nav-item nav-home"><i class="fas fa-house"></i></a>
    <a href="#pesan" class="nav-item"><i class="fas fa-edit"></i>Pesan</a>
    <a href="https://wa.me/6281234567890" class="nav-item"><i class="fab fa-whatsapp"></i>Admin</a>
</nav>

<script>
    function pilihMobil(m) {
        document.getElementById('pesan').scrollIntoView({ behavior: 'smooth' });
        document.getElementById('mobil_pilihan').value = m;
    }

    function kirimWhatsApp() {
        const n = document.getElementById('nama').value;
        const m = document.getElementById('mobil_pilihan').value;
        const r = document.getElementById('rute').value;
        const a = document.getElementById('alamat').value;

        if(!n || !a) { alert("Nama dan Alamat harus diisi!"); return; }

        const nomor = "6281234567890"; // GANTI NOMOR ANDA
        const pesan = `*BOOKING LINTAS SULAWESI*%0A👤 *Nama:* ${n}%0A🚗 *Unit:* ${m}%0A📍 *Rute:* ${r}%0A🏠 *Alamat:* ${a}`;
        window.open(`https://wa.me/${nomor}?text=${pesan}`, '_blank');
    }
</script>

</body>
</html>
