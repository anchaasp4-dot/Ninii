# Ninii
Web for my love
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Sayangku 💛</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    font-family: "Trebuchet MS", sans-serif;
    background: linear-gradient(135deg, #fff8cf, #ffe0eb, #fff4b8);
    color: #79502d;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow-x: hidden;
    padding: 20px;
}

.card {
    width: 100%;
    max-width: 420px;
    background: rgba(255,255,255,0.88);
    border: 3px solid #ffe28b;
    border-radius: 30px;
    padding: 30px 22px;
    text-align: center;
    box-shadow: 0 12px 35px rgba(208, 155, 85, 0.2);
    position: relative;
    z-index: 2;
    animation: muncul 1s ease;
}

@keyframes muncul {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.nailong {
    font-size: 95px;
    line-height: 1.3;
    animation: goyang 2s infinite ease-in-out;
}

@keyframes goyang {
    0%, 100% { transform: rotate(-5deg); }
    50% { transform: rotate(5deg); }
}

h1 {
    font-size: 29px;
    color: #ff7299;
    margin: 12px 0;
    line-height: 1.4;
}

.subtitle {
    font-size: 15px;
    margin-bottom: 20px;
}

button {
    background: #ff7da5;
    color: white;
    border: none;
    padding: 14px 24px;
    border-radius: 30px;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 5px 0 #e85e87;
    transition: 0.2s;
    margin-top: 15px;
}

button:active {
    transform: translateY(4px);
    box-shadow: 0 1px 0 #e85e87;
}

.hidden {
    display: none;
}

.message {
    background: #fff9e8;
    border: 2px dashed #f7c96b;
    border-radius: 20px;
    padding: 20px 16px;
    margin-top: 20px;
    text-align: left;
    line-height: 1.9;
    font-size: 15px;
}

.message h2 {
    text-align: center;
    color: #ff7299;
    margin-bottom: 15px;
}

.signature {
    text-align: center;
    font-weight: bold;
    color: #ff6996;
    margin-top: 18px;
    font-size: 18px;
}

.footer {
    margin-top: 22px;
    font-size: 12px;
    color: #b18b64;
}

.heart {
    position: fixed;
    bottom: -30px;
    z-index: 1;
    pointer-events: none;
    animation: terbang linear forwards;
}

@keyframes terbang {
    from {
        transform: translateY(0) rotate(0deg);
        opacity: 1;
    }
    to {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
    }
}

.cake {
    font-size: 65px;
    margin: 12px 0;
}

.small {
    font-size: 13px;
    margin-top: 12px;
    color: #ad8a69;
}
</style>
</head>

<body>

<div class="card">

    <div class="nailong">🦖💛</div>

    <div id="opening">
        <h1>Hai, Sayangku! 💗</h1>

        <p class="subtitle">
            Ada sesuatu yang spesial buat kamu...
            <br>
            Coba buka, yaa! 🎁
        </p>

        <button onclick="bukaUcapan()">
            Buka Hadiahmu 💝
        </button>
    </div>

    <div id="birthday" class="hidden">

        <h1>Happy Birthday!</h1>

        <p class="subtitle">
            Untuk seseorang yang paling spesial 💛
        </p>

        <div class="cake">🎂</div>

        <p>
            Hari ini hari spesial kamu!
            <br>
            Ada ucapan kecil dari aku buat kamu 🥹
        </p>

        <button onclick="tampilkanSurat()">
            Baca Surat Cinta 💌
        </button>

    </div>

    <div id="letter" class="hidden">

        <div class="nailong">🦖💕</div>

        <div class="message">

            <h2>Happy Birthday, Sayangku! 🎂</h2>

            <p>
                Happy Birthday Sayaangku,
                Semoga di usia yang bertambah ini
                kamu diberi kesehatan, selalu
                dikelilingi orang baik, apa yang
                kamu inginkan bisa tercapai,
                selalu happy, dan makin disayang
                sama pasangannya (adalah gwe). 💗
            </p>

            <p class="signature">
                I love u, Fanny Olivia. 💛
            </p>

        </div>

        <div class="cake">🎂🎁🎈</div>

        <button onclick="tiupLilin()">
            Tiup Lilinnya! 🕯️
        </button>

        <p class="small">
            Semoga semua harapanmu menjadi kenyataan ✨
        </p>

        <button onclick="ulangDariAwal()">
            Baca Lagi 💕
        </button>

    </div>

    <div class="footer">
        Made with love, khusus buat kamu 💛
    </div>

</div>

<script>
function bukaUcapan() {
    document.getElementById("opening").classList.add("hidden");
    document.getElementById("birthday").classList.remove("hidden");
    buatHati();
}

function tampilkanSurat() {
    document.getElementById("birthday").classList.add("hidden");
    document.getElementById("letter").classList.remove("hidden");
    buatHati();
}

function buatHati() {
    const simbol = ["💗", "💛", "💕", "✨", "🌸"];

    for (let i = 0; i < 22; i++) {
        setTimeout(() => {
            const hati = document.createElement("div");
            hati.className = "heart";
            hati.textContent =
                simbol[Math.floor(Math.random() * simbol.length)];

            hati.style.left = Math.random() * 100 + "vw";
            hati.style.fontSize = (18 + Math.random() * 20) + "px";
            hati.style.animationDuration = (3 + Math.random() * 4) + "s";

            document.body.appendChild(hati);

            setTimeout(() => hati.remove(), 7000);
        }, i * 120);
    }
}

function tiupLilin() {
    alert(
        "Yeayyy! 🎂💛\n\n" +
        "Selamat ulang tahun, Fanny Olivia!\n" +
        "Jangan lupa berdoa dan buat harapan terbaikmu, yaa.\n\n" +
        "I love u so much! 💗🦖"
    );

    buatHati();
}

function ulangDariAwal() {
    document.getElementById("letter").classList.add("hidden");
    document.getElementById("birthday").classList.add("hidden");
    document.getElementById("opening").classList.remove("hidden");

    window.scrollTo(0, 0);
}
</script>

</body>
</html>
