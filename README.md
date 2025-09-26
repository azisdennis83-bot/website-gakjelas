<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Ilegal</title>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    <style>
        html { scroll-behavior: smooth; }
        body {
            font-family: Arial, sans-serif;
            margin: 0; padding: 0;
            background: linear-gradient(135deg, #454646, #4a4a4b);
            color: #333;
        }
        header {
            background: rgba(68, 68, 68, 0.9);
            color: white; padding: 15px 20px; text-align: center;
            position: sticky; top: 0; z-index: 1000;
        }
        nav a { color:white; margin:0 10px; text-decoration:none; font-weight:bold; }
        nav a:hover { color:#ffdd57; }
        main { padding:20px; text-align:center; }
        section {
            margin-bottom: 60px;
            background: rgba(255,255,255,0.9);
            padding: 20px; border-radius: 12px;
            box-shadow: 0px 6px 15px rgba(0,0,0,0.1);
        }
        h2 { color:#0077cc; }
        img { max-width:300px; border-radius:10px; margin:15px 0; }
        .btn {
            display:inline-block; padding:10px 20px; background:#0077cc; 
            color:white; text-decoration:none; border-radius:8px; font-weight:bold;
            cursor:pointer; border:none;
        }
        .btn:hover { background:#005fa3; }
        form {
            max-width:400px; margin:20px auto; text-align:left;
        }
        form label { display:block; margin-bottom:5px; font-weight:bold; }
        form input, form textarea {
            width:100%; padding:10px; margin-bottom:15px; border-radius:8px; border:1px solid #ccc;
        }
        footer {
            background: rgba(51,51,51,0.9);
            color:white; text-align:center; padding:15px;
        }
        .social-icons a {
            color:white; font-size:24px; margin:0 10px; transition:0.3s;
        }
        .social-icons a:hover { color:#ffdd57; transform:scale(1.2); }
    </style>
</head>
<body>
    <header>
        <h1>Selamat Datang di Website Ilegal</h1>
        <nav>
            <a href="#home">Home</a> | 
            <a href="#tentang">Tentang</a> | 
            <a href="#kontak">Kontak</a>
        </nav>
    </header>

    <main>
        <section id="home">
            <h2>Home</h2>
            <p>Ini adalah halaman utama dari website Ilegal saya.</p>
            <img src="https://i0.wp.com/prolegal.id/wp-content/uploads/2023/07/senpi.jpg?fit=1000%2C667&ssl=1" alt="Gambar Contoh">
            <br>
            <a href="#tentang" class="btn">Pelajari Lebih Lanjut</a>
        </section>

        <section id="tentang">
            <h2>Tentang Saya</h2>
            <p>Halo Mas Bro! Saya sedang memperjualbelikan barang Ilegal.</p>
            <img src="https://statik.tempo.co/data/2023/07/20/id_1221169/1221169_720.jpg" alt="Foto Profil">
            <br>
            <a href="#kontak" class="btn">Hubungi Saya</a>
        </section>

        <section id="kontak">
            <h2>Kontak</h2>
            <p>Silakan isi formulir di bawah ini untuk menghubungi saya:</p>
            
            <form id="contactForm">
                <label for="nama">Nama</label>
                <input type="text" id="nama" name="nama" placeholder="Masukkan nama Anda" required>

                <label for="email">Email</label>
                <input type="email" id="email" name="email" placeholder="Masukkan email Anda" required>

                <label for="pesan">Pesan</label>
                <textarea id="pesan" name="pesan" placeholder="Tulis pesan Anda..." required></textarea>

                <button type="submit" class="btn">Kirim</button>
            </form>
            <p id="statusMsg"></p>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Website Gak Jelas</p>
        <div class="social-icons">
            <a href="https://instagram.com" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://wa.me/6281234567890" target="_blank"><i class="fab fa-whatsapp"></i></a>
            <a href="https://github.com" target="_blank"><i class="fab fa-github"></i></a>
        </div>
    </footer>

    <script>
        const scriptURL = "https://script.google.com/macros/s/AKfycbyXLHBj1jmHPkAc1CfAtLQkTHkflfPv1bvjtraPqzZxTyF0QIAML0gMkAJm61DJ7RQ/exec"; // Ganti dengan URL Web App dari Google Apps Script
        const form = document.getElementById("contactForm");
        const statusMsg = document.getElementById("statusMsg");

        form.addEventListener("submit", e => {
            e.preventDefault();
            const data = {
                nama: form.nama.value,
                email: form.email.value,
                pesan: form.pesan.value
            };

            fetch(scriptURL, {
                method: "POST",
                body: JSON.stringify(data)
            })
            .then(res => res.json())
            .then(response => {
                statusMsg.innerText = "✅ Pesan berhasil dikirim!";
                form.reset();
            })
            .catch(error => {
                console.error("Error!", error);
                statusMsg.innerText = "❌ Terjadi kesalahan, coba lagi.";
            });
        });
    </script>
</body>
</html>
