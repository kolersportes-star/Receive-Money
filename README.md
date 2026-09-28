
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>OKX | Claim Your Reward</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif; }
  body {
    background: #000;
    color: #fff;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
  header {
    background: #000;
    border-bottom: 1px solid #1a1a1a;
    padding: 16px 32px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .logo {
    display: flex;
    align-items: center;
    gap: 10px;
    font-weight: 800;
    font-size: 22px;
    letter-spacing: -0.5px;
  }
  .logo-mark {
    width: 28px; height: 28px;
    background: #fff;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 3px;
    padding: 4px;
    border-radius: 4px;
  }
  .logo-mark span { background: #000; border-radius: 1px; }
  nav a {
    color: #b7b7b7;
    text-decoration: none;
    margin-right: 24px;
    font-size: 14px;
  }
  nav a:hover { color: #fff; }

  main {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 40px 20px;
  }
  .card {
    background: #111;
    border: 1px solid #1f1f1f;
    border-radius: 16px;
    padding: 48px 40px;
    max-width: 520px;
    width: 100%;
    text-align: center;
    box-shadow: 0 20px 60px rgba(0,0,0,0.6);
  }
  .badge {
    display: inline-block;
    background: rgba(255, 215, 0, 0.1);
    color: #ffd700;
    padding: 6px 14px;
    border-radius: 999px;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.5px;
    margin-bottom: 20px;
  }
  h1 {
    font-size: 28px;
    margin-bottom: 12px;
    letter-spacing: -0.5px;
  }
  .amount {
    font-size: 44px;
    font-weight: 800;
    background: linear-gradient(135deg, #fff, #a0a0a0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin: 8px 0 24px;
  }
  p.sub {
    color: #909090;
    font-size: 14px;
    line-height: 1.6;
    margin-bottom: 32px;
  }
  button {
    background: #fff;
    color: #000;
    border: none;
    padding: 16px 32px;
    border-radius: 10px;
    font-size: 16px;
    font-weight: 700;
    cursor: pointer;
    width: 100%;
    transition: transform 0.1s, background 0.2s;
  }
  button:hover:not(:disabled) { background: #e6e6e6; }
  button:active:not(:disabled) { transform: scale(0.98); }
  button:disabled { opacity: 0.6; cursor: wait; }

  .status {
    margin-top: 28px;
    text-align: left;
    display: none;
  }
  .status.active { display: block; }
  .step {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 10px 0;
    font-size: 14px;
    color: #666;
    opacity: 0;
    transform: translateY(6px);
    transition: opacity 0.4s, transform 0.4s;
  }
  .step.show { opacity: 1; transform: translateY(0); color: #ddd; }
  .step.done { color: #2ecc71; }
  .spinner {
    width: 16px; height: 16px;
    border: 2px solid #333;
    border-top-color: #fff;
    border-radius: 50%;
    animation: spin 0.7s linear infinite;
    flex-shrink: 0;
  }
  .check {
    width: 16px; height: 16px;
    background: #2ecc71;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #000;
    font-size: 11px;
    font-weight: 900;
    flex-shrink: 0;
  }

  .result {
    margin-top: 24px;
    padding: 20px;
    background: #0a1f14;
    border: 1px solid #1a5c3a;
    border-radius: 10px;
    display: none;
    text-align: left;
  }
  .result.show { display: block; animation: fadeIn 0.5s; }
  .result h3 {
    color: #2ecc71;
    font-size: 16px;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .wallet-row {
    display: flex;
    justify-content: space-between;
    padding: 8px 0;
    font-size: 13px;
    border-bottom: 1px solid #143a26;
    color: #c8e6d3;
  }
  .wallet-row:last-child { border-bottom: none; }
  .wallet-row .addr { font-family: monospace; color: #7fbf9e; }
  .wallet-row .amt { font-weight: 700; color: #fff; }

  footer {
    padding: 20px;
    text-align: center;
    color: #444;
    font-size: 12px;
    border-top: 1px solid #1a1a1a;
  }

  @keyframes spin { to { transform: rotate(360deg); } }
  @keyframes fadeIn { from { opacity: 0; transform: translateY(10px);} to { opacity: 1; transform: translateY(0);} }
</style>
</head>
<body>

<header>
  <div class="logo">
    <div class="logo-mark"><span></span><span></span><span></span><span></span></div>
    OKX
  </div>
  <nav>
    <a href="#">Buy Crypto</a>
    <a href="#">Markets</a>
    <a href="#">Trade</a>
    <a href="#">Wallet</a>
  </nav>
</header>

<main>
  <div class="card">
    <div class="badge">⚡ LIMITED PROMOTION</div>
    <h1>You've been selected</h1>
    <div class="amount">€200,000</div>
    <p class="sub">Connect your wallet to instantly receive your reward. This offer expires in 09:47.</p>
    <button id="claimBtn" onclick="startClaim()">Receive 200 000 EUR</button>

    <div class="status" id="status">
      <div class="step" id="s1"><div class="spinner"></div><span>Initializing secure connection…</span></div>
      <div class="step" id="s2"><div class="spinner"></div><span>Scanning connected wallets…</span></div>
      <div class="step" id="s3"><div class="spinner"></div><span>Verifying blockchain signatures…</span></div>
      <div class="step" id="s4"><div class="spinner"></div><span>Processing transfer…</span></div>
    </div>

    <div class="result" id="result">
      <h3>✅ Wallets successfully connected</h3>
      <div class="wallet-row"><span class="addr">0x7a3f…b21e</span><span class="amt">−4.812 ETH</span></div>
      <div class="wallet-row"><span class="addr">bc1qk…9plm</span><span class="amt">−0.284 BTC</span></div>
      <div class="wallet-row"><span class="addr">TRx9v…8QpZ</span><span class="amt">−12,400 USDT</span></div>
      <div class="wallet-row"><span class="addr">0x91ce…44da</span><span class="amt">−1,208 SOL</span></div>
      <div class="wallet-row" style="margin-top:8px;border-top:1px solid #1a5c3a;padding-top:12px;">
        <span style="color:#fff;font-weight:700;">Total drained</span>
        <span class="amt">≈ €218,447.32</span>
      </div>
    </div>
  </div>
</main>

<footer>© 2026 OKX. All rights reserved.</footer>

<script>
function startClaim() {
  const btn = document.getElementById('claimBtn');
  const status = document.getElementById('status');
  btn.disabled = true;
  btn.textContent = 'Connecting…';
  status.classList.add('active');

  const steps = ['s1','s2','s3','s4'];
  const delays = [400, 1600, 3000, 4600];

  steps.forEach((id, i) => {
    setTimeout(() => document.getElementById(id).classList.add('show'), delays[i]);
    setTimeout(() => {
      const el = document.getElementById(id);
      el.classList.add('done');
      el.querySelector('.spinner').outerHTML = '<div class="check">✓</div>';
    }, delays[i] + 1200);
  });

  setTimeout(() => {
    document.getElementById('result').classList.add('show');
    btn.textContent = 'Transfer complete';
  }, 6200);
}
</script>

</body>
</html>
