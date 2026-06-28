<!-- WEDDING WISHES LANDING -->
<div class="wedding-page">

    <!-- Декоративный фон -->
    <div class="wedding-background">
        <div class="blur-circle blur-circle-one"></div>
        <div class="blur-circle blur-circle-two"></div>
        <div class="grain"></div>
    </div>

    <!-- Главный экран -->
    <section class="hero-section">

        <div class="hero-decoration hero-decoration-left">✦</div>
        <div class="hero-decoration hero-decoration-right">✦</div>

        <div class="hero-content reveal">

            <p class="hero-label">НАША СВАДЬБА</p>

            <h1 class="couple-names">
                Алан
                <span class="ampersand">&</span>
                Алина
            </h1>

            <div class="wedding-date">
                <span></span>
                <p>12 сентября 2026</p>
                <span></span>
            </div>

            <p class="hero-description">
                Сегодня для нас особенный день.<br>
                Оставьте несколько тёплых слов, которые мы сохраним
                вместе с воспоминаниями об этом празднике.
            </p>

            <a href="#wish-form" class="main-button">
                <span>Оставить пожелание</span>
                <span class="button-arrow">↓</span>
            </a>

        </div>

        <div class="scroll-text">
            <span>Листайте вниз</span>
            <div class="scroll-line"></div>
        </div>

    </section>

    <!-- Цитата -->
    <section class="quote-section">
        <div class="quote-card reveal">

            <div class="quote-mark">“</div>

            <p class="quote-text">
                Счастье становится больше,<br>
                когда им делишься с близкими.
            </p>

            <p class="quote-caption">
                Спасибо, что разделяете этот день вместе с нами
            </p>

        </div>
    </section>

    <!-- Форма пожелания -->
    <section class="form-section" id="wish-form">

        <div class="form-container reveal">

            <div class="form-heading">
                <p class="section-label">КНИГА ПОЖЕЛАНИЙ</p>
                <h2>Оставьте частичку тепла</h2>
                <p>
                    Напишите пожелание, совет, воспоминание
                    или несколько слов от сердца.
                </p>
            </div>

            <!--
            Вставьте вместо YOUR_FORM_ID ссылку Formspree.
            Пример:
            action="https://formspree.io/f/abcdefgh"
            -->

            <form
                class="wish-form"
                id="weddingWishForm"
                action="https://formspree.io/f/YOUR_FORM_ID"
                method="POST"
            >

                <div class="input-group">
                    <label for="guestName">Ваше имя</label>
                    <input
                        type="text"
                        id="guestName"
                        name="Имя гостя"
                        placeholder="Как к вам обращаться?"
                        required
                    >
                </div>

                <div class="input-group">
                    <label for="guestRelation">Кем вы приходитесь молодожёнам</label>
                    <input
                        type="text"
                        id="guestRelation"
                        name="Кем приходится"
                        placeholder="Друг, родственник, коллега..."
                    >
                </div>

                <div class="input-group">
                    <label for="guestWish">Ваше пожелание</label>

                    <textarea
                        id="guestWish"
                        name="Пожелание"
                        rows="6"
                        maxlength="1000"
                        placeholder="Напишите несколько тёплых слов..."
                        required
                    ></textarea>

                    <div class="character-counter">
                        <span id="characterCount">0</span> / 1000
                    </div>
                </div>

                <!-- Защита от автоматического спама -->
                <input type="text" name="_gotcha" class="hidden-field">

                <button type="submit" class="submit-button">
                    <span class="submit-text">Отправить пожелание</span>
                    <span class="submit-icon">♡</span>
                </button>

                <p class="privacy-text">
                    Ваше пожелание увидят только молодожёны
                </p>

            </form>

            <!-- Сообщение после отправки -->
            <div class="success-message" id="successMessage">

                <div class="success-icon">♡</div>

                <h3>Спасибо!</h3>

                <p>
                    Ваши слова стали частью нашей семейной истории.
                </p>

                <button type="button" class="secondary-button" id="newWishButton">
                    Оставить ещё одно пожелание
                </button>

            </div>

        </div>

    </section>

    <!-- Финальный блок -->
    <footer class="wedding-footer">

        <div class="footer-symbol">∞</div>

        <p class="footer-names">Алан & Алина</p>

        <p class="footer-date">12 · 09 · 2026</p>

        <p class="footer-thanks">
            С любовью и благодарностью каждому из вас
        </p>

    </footer>

</div>


<style>
    @import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Manrope:wght@300;400;500;600&display=swap');

    :root {
        --background: #f5f1eb;
        --background-light: #faf8f4;
        --text: #25221f;
        --muted-text: #736d66;
        --accent: #8b6f58;
        --accent-dark: #624c3c;
        --line: rgba(74, 62, 52, 0.16);
        --white: #ffffff;
        --shadow: 0 30px 80px rgba(65, 52, 42, 0.1);
        --serif: "Cormorant Garamond", Georgia, serif;
        --sans: "Manrope", Arial, sans-serif;
    }

    * {
        box-sizing: border-box;
    }

    html {
        scroll-behavior: smooth;
    }

    body {
        margin: 0;
    }

    .wedding-page {
        position: relative;
        width: 100%;
        overflow: hidden;
        color: var(--text);
        background: var(--background);
        font-family: var(--sans);
    }

    .wedding-background {
        position: absolute;
        inset: 0;
        overflow: hidden;
        pointer-events: none;
    }

    .blur-circle {
        position: absolute;
        border-radius: 50%;
        filter: blur(20px);
        opacity: 0.45;
    }

    .blur-circle-one {
        top: 4%;
        left: -200px;
        width: 450px;
        height: 450px;
        background: rgba(220, 196, 178, 0.55);
    }

    .blur-circle-two {
        top: 45%;
        right: -250px;
        width: 600px;
        height: 600px;
        background: rgba(196, 207, 188, 0.42);
    }

    .grain {
        position: absolute;
        inset: 0;
        opacity: 0.035;
        background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='.8'/%3E%3C/svg%3E");
    }

    .hero-section {
        position: relative;
        z-index: 1;
        min-height: 100svh;
        padding: 80px 24px 50px;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
    }

    .hero-content {
        width: 100%;
        max-width: 850px;
    }

    .hero-label,
    .section-label {
        margin: 0 0 25px;
        color: var(--accent);
        font-size: 11px;
        font-weight: 600;
        letter-spacing: 0.38em;
    }

    .couple-names {
        margin: 0;
        font-family: var(--serif);
        font-size: clamp(72px, 12vw, 150px);
        font-weight: 400;
        line-height: 0.77;
        letter-spacing: -0.055em;
    }

    .ampersand {
        display: block;
        margin: 13px 0 15px;
        color: var(--accent);
        font-size: 0.55em;
        font-style: italic;
        line-height: 0.7;
    }

    .wedding-date {
        margin: 52px auto 0;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 20px;
    }

    .wedding-date span {
        width: 70px;
        height: 1px;
        background: var(--line);
    }

    .wedding-date p {
        margin: 0;
        color: var(--accent-dark);
        font-size: 12px;
        font-weight: 500;
        letter-spacing: 0.23em;
        text-transform: uppercase;
    }

    .hero-description {
        max-width: 610px;
        margin: 34px auto 0;
        color: var(--muted-text);
        font-family: var(--serif);
        font-size: clamp(20px, 2.5vw, 27px);
        font-weight: 400;
        line-height: 1.45;
    }

    .main-button {
        min-width: 260px;
        min-height: 62px;
        margin-top: 42px;
        padding: 17px 23px 17px 29px;
        display: inline-flex;
        align-items: center;
        justify-content: space-between;
        gap: 30px;
        color: var(--white);
        background: var(--text);
        border: 1px solid var(--text);
        border-radius: 100px;
        font-size: 13px;
        font-weight: 500;
        letter-spacing: 0.04em;
        text-decoration: none;
        transition:
            transform 0.3s ease,
            background 0.3s ease,
            box-shadow 0.3s ease;
    }

    .main-button:hover {
        transform: translateY(-3px);
        background: var(--accent-dark);
        box-shadow: 0 15px 35px rgba(53, 43, 36, 0.19);
    }

    .button-arrow {
        width: 32px;
        height: 32px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text);
        background: var(--white);
        border-radius: 50%;
        font-size: 16px;
    }

    .hero-decoration {
        position: absolute;
        top: 50%;
        color: var(--accent);
        font-size: 18px;
        opacity: 0.5;
    }

    .hero-decoration-left {
        left: 8%;
    }

    .hero-decoration-right {
        right: 8%;
    }

    .scroll-text {
        position: absolute;
        bottom: 28px;
        left: 50%;
        display: flex;
        align-items: center;
        flex-direction: column;
        transform: translateX(-50%);
    }

    .scroll-text span {
        color: var(--muted-text);
        font-size: 9px;
        letter-spacing: 0.24em;
        text-transform: uppercase;
    }

    .scroll-line {
        width: 1px;
        height: 30px;
        margin-top: 10px;
        overflow: hidden;
        background: var(--line);
    }

    .scroll-line::after {
        content: "";
        display: block;
        width: 1px;
        height: 15px;
        background: var(--accent);
        animation: scrollLine 1.8s ease-in-out infinite;
    }

    @keyframes scrollLine {
        0% {
            transform: translateY(-18px);
        }

        100% {
            transform: translateY(35px);
        }
    }

    .quote-section {
        position: relative;
        z-index: 1;
        padding: 110px 24px;
    }

    .quote-card {
        max-width: 980px;
        margin: 0 auto;
        padding: 80px 35px;
        text-align: center;
        border: 1px solid var(--line);
        border-radius: 32px;
        background: rgba(255, 255, 255, 0.35);
        backdrop-filter: blur(18px);
        -webkit-backdrop-filter: blur(18px);
    }

    .quote-mark {
        height: 45px;
        color: var(--accent);
        font-family: var(--serif);
        font-size: 90px;
        line-height: 1;
    }

    .quote-text {
        margin: 20px 0 0;
        font-family: var(--serif);
        font-size: clamp(34px, 5vw, 59px);
        font-weight: 400;
        line-height: 1.1;
        letter-spacing: -0.025em;
    }

    .quote-caption {
        margin: 30px 0 0;
        color: var(--muted-text);
        font-size: 12px;
        letter-spacing: 0.08em;
    }

    .form-section {
        position: relative;
        z-index: 1;
        padding: 110px 24px 130px;
    }

    .form-container {
        max-width: 760px;
        margin: 0 auto;
        padding: 70px;
        border-radius: 36px;
        background: var(--background-light);
        box-shadow: var(--shadow);
    }

    .form-heading {
        margin-bottom: 50px;
        text-align: center;
    }

    .form-heading h2 {
        margin: 0;
        font-family: var(--serif);
        font-size: clamp(45px, 7vw, 71px);
        font-weight: 400;
        line-height: 0.98;
        letter-spacing: -0.035em;
    }

    .form-heading > p:last-child {
        max-width: 500px;
        margin: 25px auto 0;
        color: var(--muted-text);
        font-size: 14px;
        line-height: 1.7;
    }

    .wish-form {
        display: flex;
        flex-direction: column;
        gap: 28px;
    }

    .input-group {
        position: relative;
    }

    .input-group label {
        display: block;
        margin-bottom: 11px;
        color: var(--text);
        font-size: 11px;
        font-weight: 600;
        letter-spacing: 0.1em;
        text-transform: uppercase;
    }

    .input-group input,
    .input-group textarea {
        width: 100%;
        padding: 19px 20px;
        color: var(--text);
        background: transparent;
        border: 1px solid var(--line);
        border-radius: 14px;
        outline: none;
        font-family: var(--sans);
        font-size: 15px;
        font-weight: 400;
        transition:
            border-color 0.25s ease,
            background 0.25s ease,
            box-shadow 0.25s ease;
    }

    .input-group textarea {
        min-height: 180px;
        padding-bottom: 40px;
        resize: vertical;
        line-height: 1.65;
    }

    .input-group input::placeholder,
    .input-group textarea::placeholder {
        color: #aaa39b;
    }

    .input-group input:focus,
    .input-group textarea:focus {
        border-color: var(--accent);
        background: var(--white);
        box-shadow: 0 0 0 4px rgba(139, 111, 88, 0.08);
    }

    .character-counter {
        position: absolute;
        right: 16px;
        bottom: 13px;
        color: #aaa39b;
        font-size: 10px;
    }

    .hidden-field {
        position: absolute !important;
        left: -9999px !important;
        opacity: 0 !important;
    }

    .submit-button {
        width: 100%;
        min-height: 66px;
        margin-top: 7px;
        padding: 16px 22px 16px 28px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        color: var(--white);
        background: var(--text);
        border: none;
        border-radius: 100px;
        cursor: pointer;
        font-family: var(--sans);
        font-size: 14px;
        font-weight: 500;
        transition:
            transform 0.3s ease,
            background 0.3s ease,
            box-shadow 0.3s ease;
    }

    .submit-button:hover {
        transform: translateY(-2px);
        background: var(--accent-dark);
        box-shadow: 0 16px 35px rgba(53, 43, 36, 0.17);
    }

    .submit-button:disabled {
        cursor: wait;
        opacity: 0.7;
        transform: none;
    }

    .submit-icon {
        width: 37px;
        height: 37px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text);
        background: var(--white);
        border-radius: 50%;
        font-size: 20px;
    }

    .privacy-text {
        margin: -10px 0 0;
        color: #999189;
        font-size: 10px;
        text-align: center;
    }

    .success-message {
        display: none;
        padding: 45px 0 20px;
        text-align: center;
    }

    .success-message.active {
        display: block;
        animation: successAppear 0.7s ease forwards;
    }

    @keyframes successAppear {
        from {
            opacity: 0;
            transform: translateY(15px);
        }

        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .success-icon {
        width: 80px;
        height: 80px;
        margin: 0 auto 25px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--white);
        background: var(--accent);
        border-radius: 50%;
        font-size: 36px;
    }

    .success-message h3 {
        margin: 0;
        font-family: var(--serif);
        font-size: 60px;
        font-weight: 400;
    }

    .success-message p {
        max-width: 400px;
        margin: 18px auto 30px;
        color: var(--muted-text);
        font-size: 14px;
        line-height: 1.7;
    }

    .secondary-button {
        padding: 15px 25px;
        color: var(--text);
        background: transparent;
        border: 1px solid var(--line);
        border-radius: 100px;
        cursor: pointer;
        font-family: var(--sans);
        font-size: 12px;
        transition:
            background 0.25s ease,
            border-color 0.25s ease;
    }

    .secondary-button:hover {
        background: var(--white);
        border-color: var(--accent);
    }

    .wedding-footer {
        position: relative;
        z-index: 1;
        padding: 90px 24px 60px;
        color: var(--white);
        background: var(--text);
        text-align: center;
    }

    .footer-symbol {
        color: #d4bca7;
        font-family: var(--serif);
        font-size: 45px;
    }

    .footer-names {
        margin: 20px 0 0;
        font-family: var(--serif);
        font-size: clamp(44px, 7vw, 72px);
        font-weight: 400;
    }

    .footer-date {
        margin: 17px 0 0;
        color: #d4bca7;
        font-size: 11px;
        letter-spacing: 0.28em;
    }

    .footer-thanks {
        margin: 45px 0 0;
        color: rgba(255, 255, 255, 0.56);
        font-size: 11px;
        letter-spacing: 0.08em;
    }

    .reveal {
        opacity: 0;
        transform: translateY(28px);
        transition:
            opacity 0.9s ease,
            transform 0.9s ease;
    }

    .reveal.visible {
        opacity: 1;
        transform: translateY(0);
    }

    @media (max-width: 768px) {
        .hero-section {
            min-height: 100svh;
            padding: 70px 20px 55px;
        }

        .couple-names {
            font-size: clamp(69px, 25vw, 105px);
            line-height: 0.82;
        }

        .wedding-date {
            gap: 12px;
            margin-top: 40px;
        }

        .wedding-date span {
            width: 30px;
        }

        .wedding-date p {
            font-size: 10px;
            letter-spacing: 0.15em;
        }

        .hero-description br {
            display: none;
        }

        .hero-decoration {
            display: none;
        }

        .scroll-text {
            display: none;
        }

        .quote-section {
            padding: 70px 16px;
        }

        .quote-card {
            padding: 60px 22px;
            border-radius: 24px;
        }

        .quote-text br {
            display: none;
        }

        .form-section {
            padding: 60px 14px 90px;
        }

        .form-container {
            padding: 50px 20px 35px;
            border-radius: 25px;
        }

        .form-heading {
            margin-bottom: 40px;
        }

        .wish-form {
            gap: 24px;
        }

        .wedding-footer {
            padding-top: 70px;
        }
    }

    @media (max-width: 420px) {
        .hero-label,
        .section-label {
            letter-spacing: 0.27em;
        }

        .main-button {
            width: 100%;
            max-width: 330px;
        }

        .couple-names {
            font-size: 76px;
        }

        .hero-description {
            font-size: 21px;
        }

        .form-heading h2 {
            font-size: 48px;
        }
    }
</style>


<script>
    document.addEventListener("DOMContentLoaded", function () {
        const form = document.getElementById("weddingWishForm");
        const successMessage = document.getElementById("successMessage");
        const newWishButton = document.getElementById("newWishButton");
        const wishTextarea = document.getElementById("guestWish");
        const characterCount = document.getElementById("characterCount");
        const submitButton = form.querySelector(".submit-button");
        const submitText = form.querySelector(".submit-text");

        // Счётчик символов
        wishTextarea.addEventListener("input", function () {
            characterCount.textContent = wishTextarea.value.length;
        });

        // Анимация появления блоков
        const revealElements = document.querySelectorAll(".reveal");

        const revealObserver = new IntersectionObserver(
            function (entries) {
                entries.forEach(function (entry) {
                    if (entry.isIntersecting) {
                        entry.target.classList.add("visible");
                        revealObserver.unobserve(entry.target);
                    }
                });
            },
            {
                threshold: 0.12
            }
        );

        revealElements.forEach(function (element) {
            revealObserver.observe(element);
        });

        // Отправка формы без перезагрузки страницы
        form.addEventListener("submit", async function (event) {
            event.preventDefault();

            const formAction = form.getAttribute("action");

            if (formAction.includes("YOUR_FORM_ID")) {
                alert(
                    "Сначала вставьте свою ссылку Formspree вместо YOUR_FORM_ID."
                );
                return;
            }

            submitButton.disabled = true;
            submitText.textContent = "Отправляем...";

            const formData = new FormData(form);

            try {
                const response = await fetch(formAction, {
                    method: "POST",
                    body: formData,
                    headers: {
                        Accept: "application/json"
                    }
                });

                if (!response.ok) {
                    throw new Error("Ошибка отправки формы");
                }

                form.style.display = "none";
                successMessage.classList.add("active");

                createConfetti();

            } catch (error) {
                alert(
                    "Не удалось отправить пожелание. Проверьте подключение формы и попробуйте ещё раз."
                );

            } finally {
                submitButton.disabled = false;
                submitText.textContent = "Отправить пожелание";
            }
        });

        // Повторное заполнение формы
        newWishButton.addEventListener("click", function () {
            form.reset();
            characterCount.textContent = "0";
            successMessage.classList.remove("active");
            form.style.display = "flex";

            document
                .getElementById("guestName")
                .focus();
        });

        // Небольшое конфетти
        function createConfetti() {
            const symbols = ["♡", "✦", "·", "❀"];

            for (let i = 0; i < 30; i++) {
                const confetti = document.createElement("span");

                confetti.textContent =
                    symbols[Math.floor(Math.random() * symbols.length)];

                confetti.style.position = "fixed";
                confetti.style.left = Math.random() * 100 + "vw";
                confetti.style.top = "-30px";
                confetti.style.zIndex = "999999";
                confetti.style.pointerEvents = "none";
                confetti.style.color =
                    Math.random() > 0.5 ? "#8b6f58" : "#c4a98e";
                confetti.style.fontSize =
                    12 + Math.random() * 16 + "px";
                confetti.style.opacity = "0.8";
                confetti.style.transition =
                    "transform 2.5s ease-out, opacity 2.5s ease-out";

                document.body.appendChild(confetti);

                setTimeout(function () {
                    confetti.style.transform =
                        "translateY(110vh) rotate(" +
                        Math.random() * 720 +
                        "deg)";
                    confetti.style.opacity = "0";
                }, 30);

                setTimeout(function () {
                    confetti.remove();
                }, 2700);
            }
        }
    });
</script>
