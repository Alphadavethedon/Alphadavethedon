<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Email Template</title>
<style>
    :root {
        --bg-light: #ffffff;
        --bg-dark: #121212;
        --text-light: #2d2d2d;
        --text-dark: #f5f5f5;
        --primary: #4f46e5;
        --accent: #6366f1;
        --transition-speed: 0.3s;
        --font-primary: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    }
    body {
        font-family: var(--font-primary);
        margin: 0;
        padding: 0;
        background: var(--bg-light);
        color: var(--text-light);
        line-height: 1.6;
        transition: background var(--transition-speed) ease, color var(--transition-speed) ease;
    }
    .dark-mode {
        background: var(--bg-dark);
        color: var(--text-dark);
    }
    .container {
        max-width: 700px;
        margin: 0 auto;
        padding: 2rem;
        border-radius: 16px;
        background: inherit;
    }
    h1 {
        color: var(--primary);
        margin-bottom: 1rem;
        font-size: 1.5rem;
        transition: color var(--transition-speed) ease;
    }
    p {
        font-size: 1rem;
        margin-bottom: 1rem;
    }
    .toggle-btn {
        padding: 0.5rem 1rem;
        background: var(--primary);
        color: #fff;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        font-size: 0.9rem;
        transition: background var(--transition-speed) ease, transform var(--transition-speed) ease;
    }
    .toggle-btn:hover {
        background: var(--accent);
        transform: translateY(-2px);
    }
    .signature {
        margin-top: 2rem;
        border-top: 1px solid rgba(0,0,0,0.1);
        padding-top: 1rem;
        font-size: 0.9rem;
    }
    /* Smooth Fade-In Animation */
    @keyframes fadeIn {
        0% { opacity: 0; transform: translateY(10px); }
        100% { opacity: 1; transform: translateY(0); }
    }
    .container {
        animation: fadeIn 0.8s ease-in-out;
    }
</style>
</head>
<body>
<div class="container" id="emailContainer">
    <h1>Ticket Review Update</h1>
    <p>Hi,</p>
    <p>Thanks for reaching out. I’ve received your ticket and I’m currently reviewing it. I have noticed that you have not indicated the DCST of the affected agent. Kindly note that the affected agent’s credentials are necessary for any further ticket escalations, if required.</p>
    <p>If there’s anything else you’d like to share in the meantime, please feel free to reply to this email.</p>
    
    <div class="signature">
        Best regards,<br>
        <strong>Davis Wabwile</strong><br>
        Desktop Support Engineer
    </div>

    <button class="toggle-btn" onclick="toggleDarkMode()">Toggle Dark Mode</button>
</div>

<script>
function toggleDarkMode() {
    document.body.classList.toggle('dark-mode');
}
</script>
</body>
</html>
