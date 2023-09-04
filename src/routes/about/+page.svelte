<script>
    let fullName = "Buğra Altun";
    let role = "Junior Developer";
    let aboutText = `
      I am Buğra Altun (a.k.a rabug), I started coding at age 9 with C#. Still, I love programming, and my goal is to be a student at Ecole 42.
      I live in Turkey 🇹🇷. I studied English in the English project class for 4 years straight, but it's still not perfect. I don't believe coding requires math because
      solving a math problem is a computer job, and I find this funny. By the way, a funny fact: this website is 75% coded by GPT 💀 because I am too lazy to make a website.
      I also make animations, 3D models, games, and design. Anyway, if you want to contact me or something, you can look at the contact page.
    `;
</script>


<main>
    <div class="mac-full">
        <div class="mac-title-bar">
            <div class="mac-title">About Me</div>
            <div class="mac-buttons">
                <div class="mac-button close"></div>
                <div class="mac-button minimize"></div>
                <div class="mac-button zoom"></div>
            </div>
        </div>
        <div class="mac-window">
            <img src="../src/lib/images/rabug.jpeg" alt="rabug" style="border-radius: 1000px; margin: 10px auto" width="100px">
            <h2>{fullName}</h2>
            <p class="role">{role}</p>
            <p style="margin: auto 30px;">{aboutText}</p>
            <br>
        </div>
    </div>
</main>

<style>
    /* Add your CSS styles here for the About page */
    h2 {
        font-size: 1.5rem;
    }

    .role {
        color: #777;
        margin-bottom: 1rem;
    }

    p {
        font-size: 1.1rem;
        line-height: 1.6;
    }

    .mac-full{
        width: 650px;
        margin: 0px auto;
        margin-top: 100px;
    }

    .mac-window {
        background-color: #313131;
        border-bottom-left-radius: 8px;
        border-bottom-right-radius: 8px;
        border-top: 0px 0px;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
        position: relative;
        text-align: center;
    }

    .mac-title-bar {
        background-color: #858585;
        display: flex;
        justify-content: space-between;
        padding: 0.5rem;
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
    }

    .mac-title {
        font-size: 1.25rem;
        font-weight: bold;
        margin: -5px 10px;
    }

    .mac-buttons {
        display: flex;
        gap: 0.25rem;
    }

    .mac-button {
        width: 18px;
        height: 18px;
        border-radius: 50%;
        background-color: #f64d3f;
        margin: auto auto;
    }

    .mac-button.close {
        background-color: #f64d3f;
    }

    .mac-button.minimize {
        background-color: #ffb830;
    }

    .mac-button.zoom {
        background-color: #4cd964;
    }

    img {
        max-width: 100%;
        height: auto;
    }
</style>
