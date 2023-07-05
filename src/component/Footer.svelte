<footer class="footer">
    <div class="email">
        <i class="fa-solid fa-envelope" /> helen.ounsaar@gmail.com
    </div>
    <div class="phone">
        <i class="fa-solid fa-phone" /> +372 53321614
    </div>
    <div class="social">
        <a href="https://github.com/HelenOunsaar"
            ><i class="fa-brands fa-github" /></a
        >

        <a href="https://www.linkedin.com/in/helen-õunsaar-429504167/"
            ><i class="fa-brands fa-linkedin" /></a
        >
    </div>
</footer>

<style>
    @import "@fortawesome/fontawesome-free/css/all.css";

    .footer {
        margin-top: auto;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 10px 5px;
        width: 100%;
        font-size: 14px;
    }

    i {
        padding-right: 5px;
        color: #bfa181;
    }
    .email {
        margin-right: 20px;
    }
    .phone {
        margin-right: 20px;
    }

    .social a + a {
        margin-left: 20px;
    }

    @media (max-width: 768px) {
        .footer {
            position: sticky;
            flex-direction: column;
            height: auto;
        }

        .email,
        .phone,
        .social {
            margin-bottom: 10px;
        }

        i {
            font-size: 22px;
        }
    }
</style>
