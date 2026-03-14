<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Ban Appeal • Itzz_daniel 🍊 Community</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    :root {
      --bg: #050816;
      --accent: #f97316;
      --accent-blue: #3b82f6;
      --text-main: #e5e7eb;
      --text-soft: #9ca3af;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: system-ui, -apple-system, "Segoe UI", sans-serif;
    }

    body {
      background: radial-gradient(circle at top, #111827 0, #020617 45%, #000 100%);
      color: var(--text-main);
      height: 100vh;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    /* INTRO OVERLAY */
    .intro-overlay {
      position: fixed;
      inset: 0;
      background: #020617;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 20;
      overflow: hidden;
      transition: opacity 0.7s ease, visibility 0.7s ease;
    }

    .intro-overlay.hidden {
      opacity: 0;
      visibility: hidden;
    }

    .intro-panels {
      position: absolute;
      inset: 0;
      display: flex;
    }

    .intro-panel {
      flex: 1;
      background: linear-gradient(135deg, rgba(59,130,246,0.15), rgba(15,23,42,0.95));
      animation: slideLeft 2.4s ease-in-out infinite;
    }

    .intro-panel:nth-child(2) {
      background: linear-gradient(135deg, rgba(168,85,247,0.18), rgba(15,23,42,0.95));
      animation: slideRight 2.4s ease-in-out infinite;
    }

    .intro-panel:nth-child(3) {
      background: linear-gradient(135deg, rgba(249,115,22,0.18), rgba(15,23,42,0.95));
      animation: slideLeft 2.4s ease-in-out infinite;
    }

    @keyframes slideLeft {
      0% { transform: translateX(0); }
      50% { transform: translateX(-6%); }
      100% { transform: translateX(0); }
    }

    @keyframes slideRight {
      0% { transform: translateX(0); }
      50% { transform: translateX(6%); }
      100% { transform: translateX(0); }
    }

    .intro-content {
      position: relative;
      z-index: 2;
      background: rgba(15,23,42,0.9);
      padding: 24px;
      border-radius: 20px;
      border: 1px solid rgba(148,163,184,0.4);
      text-align: center;
      width: 90%;
      max-width: 420px;
    }

    .intro-title {
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 0.15em;
      color: var(--text-soft);
      margin-bottom: 8px;
    }

    .intro-main {
      font-size: 18px;
      font-weight: 600;
      margin-bottom: 10px;
    }

    .intro-main span {
      color: var(--accent);
      text-shadow: 0 0 16px rgba(249,115,22,0.8);
    }

    .intro-dots {
      display: flex;
      justify-content: center;
      gap: 6px;
      margin-top: 10px;
    }

    .intro-dot {
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background: rgba(148,163,184,0.6);
      animation: pulse 1.2s infinite;
    }

    .intro-dot:nth-child(2) { animation-delay: 0.15s; }
    .intro-dot:nth-child(3) { animation-delay: 0.3s; }

    @keyframes pulse {
      0%,100 { opacity: 0.4; transform: scale(0.9); }
      50% { opacity: 1; transform: scale(1.2); }
    }

    /* MAIN FORM */
    .form-wrapper {
      width: 100%;
      max-width: 540px;
      background: radial-gradient(circle at top left, rgba(59,130,246,0.18), rgba(15,23,42,0.95));
      border: 1px solid rgba(148,163,184,0.5);
      border-radius: 22px;
      padding: 24px 22px 20px;
      box-shadow: 0 30px 80px rgba(0,0,0,0.85);
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.7s ease, transform 0.7s ease;
      position: relative;
      overflow: hidden;
    }

    .form-wrapper::before {
      content: "";
      position: absolute;
      inset: -40%;
      background: radial-gradient(circle at top, rgba(59,130,246,0.25), transparent 55%);
      opacity: 0.7;
      pointer-events: none;
    }

    .form-wrapper.show {
      opacity: 1;
      transform: translateY(0);
    }

    .form-inner {
      position: relative;
      z-index: 1;
    }

    .form-title {
      font-size: 20px;
      font-weight: 600;
      margin-bottom: 4px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .form-title span {
      color: var(--accent);
      text-shadow: 0 0 12px rgba(249,115,22,0.8);
    }

    .form-sub {
      font-size: 13px;
      color: var(--text-soft);
      margin-bottom: 18px;
    }

    label {
      font-size: 13px;
      margin-bottom: 6px;
      display: block;
      color: var(--text-main);
    }

    input, textarea {
      width: 100%;
      padding: 10px;
      border-radius: 10px;
      border: 1px solid rgba(148,163,184,0.5);
      background: rgba(2,6,23,0.9);
      color: var(--text-main);
      margin-bottom: 14px;
      font-size: 14px;
      outline: none;
      transition: border 0.15s ease, box-shadow 0.15s ease, background 0.15s ease;
    }

    input:focus, textarea:focus {
      border-color: var(--accent-blue);
      box-shadow: 0 0 0 1px rgba(59,130,246,0.6);
      background: rgba(15,23,42,0.95);
    }

    textarea {
      height: 120px;
      resize: none;
    }

    .submit-btn {
      width: 100%;
      padding: 12px;
      border-radius: 999px;
      border: none;
      background: linear-gradient(135deg, #f97316, #fb923c);
      color: #111;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      transition: 0.2s;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
    }

    .submit-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 14px 40px rgba(249,115,22,0.7);
    }

    .submit-btn:disabled {
      opacity: 0.6;
      cursor: default;
      transform: none;
      box-shadow: none;
    }

    .status-text {
      margin-top: 10px;
      font-size: 13px;
      color: var(--text-soft);
      min-height: 18px;
    }

    .status-text.ok {
      color: #4ade80;
    }

    .status-text.err {
      color: #f97373;
    }

    /* COOLDOWN OVERLAY */
    .cooldown-overlay {
      position: fixed;
      inset: 0;
      background: #000;
      display: none;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      color: #f9fafb;
      z-index: 30;
    }

    .cooldown-overlay.show {
      display: flex;
    }

    .clock {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      border: 3px solid rgba(148,163,184,0.6);
      position: relative;
      margin-bottom: 18px;
    }

    .clock::before,
    .clock::after {
      content: "";
      position: absolute;
      background: #f9fafb;
      left: 50%;
      top: 50%;
      transform-origin: bottom center;
    }

    .clock::before {
      width: 3px;
      height: 26px;
      transform: translate(-50%, -100%) rotate(0deg);
      animation: hourHand 12s linear infinite;
    }

    .clock::after {
      width: 2px;
      height: 32px;
      transform: translate(-50%, -100%) rotate(0deg);
      animation: minuteHand 4s linear infinite;
      opacity: 0.8;
    }

    @keyframes hourHand {
      to { transform: translate(-50%, -100%) rotate(360deg); }
    }

    @keyframes minuteHand {
      to { transform: translate(-50%, -100%) rotate(360deg); }
    }

    .cooldown-text {
      font-size: 16px;
      text-align: center;
      margin-bottom: 6px;
    }

    .cooldown-sub {
      font-size: 13px;
      color: #9ca3af;
      text-align: center;
    }
  </style>
</head>
<body>

  <!-- INTRO -->
  <div class="intro-overlay" id="intro">
    <div class="intro-panels">
      <div class="intro-panel"></div>
      <div class="intro-panel"></div>
      <div class="intro-panel"></div>
    </div>

    <div class="intro-content">
      <div class="intro-title">Connecting</div>
      <div class="intro-main">
        Connecting to <span>Itzz_daniel 🍊ㆍCommunity Server</span>
      </div>
      <div class="intro-dots">
        <div class="intro-dot"></div>
        <div class="intro-dot"></div>
        <div class="intro-dot"></div>
      </div>
    </div>
  </div>

  <!-- COOLDOWN SCREEN -->
  <div class="cooldown-overlay" id="cooldown">
    <div class="clock"></div>
    <div class="cooldown-text">
      Please wait <strong>2 hours</strong> before you submit another appeal.
    </div>
    <div class="cooldown-sub">
      Your appeal has been sent to the staff team for review.
    </div>
  </div>

  <!-- BAN APPEAL FORM -->
  <div class="form-wrapper" id="formWrapper">
    <div class="form-inner">
      <div class="form-title">
        Ban Appeal <span>Form</span>
      </div>
      <div class="form-sub">
        Fill this out honestly. Your answers help staff decide whether to lift your ban.
      </div>

      <label for="username">Discord Username</label>
      <input type="text" id="username" placeholder="Example: ItzzDaniel#0001">

      <label for="userid">Discord ID</label>
      <input type="text" id="userid" placeholder="Example: 123456789012345678">

      <label for="reason">Why were you banned? (and why should we unban you?)</label>
      <textarea id="reason" placeholder="Explain what happened, what you did wrong, and what will change."></textarea>

      <button class="submit-btn" id="submitAppeal">
        📨 Submit Appeal
      </button>

      <div class="status-text" id="statusText"></div>
    </div>
  </div>

  <script>
    // 🔗 REPLACE THIS WITH YOUR REAL WEBHOOK PRIVATELY
    const WEBHOOK_URL = "REPLACE_WITH_YOUR_WEBHOOK";

    const ROLE_PING = "<@&1482333430334099476>";
    const LOGO_URL = "https://media.discordapp.net/attachments/1482335825575546906/1482374492650213499/Panther-logo2-removebg-preview.png?format=webp&quality=lossless&width=573&height=573";

    const intro = document.getElementById("intro");
    const formWrapper = document.getElementById("formWrapper");
    const cooldown = document.getElementById("cooldown");
    const submitBtn = document.getElementById("submitAppeal");
    const statusText = document.getElementById("statusText");

    // Intro fade-out
    setTimeout(() => {
      intro.classList.add("hidden");
      formWrapper.classList.add("show");
    }, 3000);

    submitBtn.addEventListener("click", async () => {
      const username = document.getElementById("username").value.trim();
      const userid = document.getElementById("userid").value.trim();
      const reason = document.getElementById("reason").value.trim();

      statusText.className = "status-text";

      if (!username || !userid || !reason) {
        statusText.textContent = "Please fill out all fields before submitting.";
        statusText.classList.add("err");
        return;
      }

      submitBtn.disabled = true;
      statusText.textContent = "Sending your appeal to staff...";
      statusText.classList.add("ok");

      const embed = {
        title: "New Ban Appeal Submitted",
        color: 0x3b82f6,
        thumbnail: { url: LOGO_URL },
        fields: [
          {
            name: "👤 Discord Username",
            value: username,
            inline: false
          },
          {
            name: "🆔 Discord ID",
            value: userid,
            inline: false
          },
          {
            name: "📄 Reason / Explanation",
            value: reason.length > 1024 ? reason.slice(0, 1021) + "..." : reason,
            inline: false
          }
        ],
        footer: {
          text: "Itzz_daniel 🍊 • Ban Appeal System"
        },
        timestamp: new Date().toISOString()
      };

      try {
  const res = await fetch("https://discord.com/api/webhooks/1482416930639056947/TuFlChLxW_EowYMN3D3dOAvifS9fA7eJGH6N3DEyt74dVj0qTRpltB9Bzmk8BmxL8bcI", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      content: `${ROLE_PING} New ban appeal submitted.`,
      embeds: [embed]
    })
  });


        if (!res.ok) {
          throw new Error("❌ Webhook error");
        }

        // Show cooldown screen
        cooldown.classList.add("show");
        formWrapper.style.opacity = "0";
        formWrapper.style.pointerEvents = "none";
      } catch (err) {
        statusText.textContent = "Something went wrong sending your appeal. Please try again later.";
        statusText.classList.remove("ok");
        statusText.classList.add("err");
        submitBtn.disabled = false;
      }
    });
  </script>
</body>
</html>
