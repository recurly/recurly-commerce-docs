---
title: Intro to Commerce
deprecated: false
hidden: true
metadata:
  robots: index
---
<HTMLBlock>{`
<style>
  .rc-guide {
    --yellow: #FFD706;
    --orange: #FF8200;
    --vermillion: #FF5810;
    --salmon: #FF9D88;
    --offblack: #0D0D0B;
    --darkgray: #32312D;
    --gray: #807D73;
    --lightgray: #CCC9B8;
    --brightgray: #F1EFE3;
    --offwhite: #FFFDF2;
    font-family: 'Segoe UI', system-ui, sans-serif;
  }

  .rc-hero {
    background: var(--offblack);
    color: white;
    padding: 56px 40px 48px;
    text-align: center;
    border-radius: 16px;
    margin-bottom: 0;
  }

  .rc-badge {
    display: inline-block;
    background: var(--yellow);
    color: var(--offblack);
    border-radius: 20px;
    padding: 6px 18px;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 20px;
  }

  .rc-hero h1 {
    font-size: 2.4rem;
    font-weight: 800;
    line-height: 1.15;
    margin-bottom: 14px;
    color: var(--offwhite);
  }

  .rc-hero > p {
    font-size: 1.05rem;
    opacity: 0.8;
    max-width: 600px;
    margin: 0 auto 32px;
    color: var(--lightgray);
  }

  .rc-hero-stats {
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
  }

  .rc-num {
    font-size: 1.8rem;
    font-weight: 800;
    color: var(--yellow);
  }

  .rc-lbl {
    font-size: 0.8rem;
    color: var(--lightgray);
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  .rc-nav {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin: 24px 0 28px;
  }

  .rc-nav a {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 14px;
    border-radius: 12px;
    border: 1px solid var(--lightgray);
    background: white;
    color: var(--darkgray);
    text-decoration: none;
    font-size: 0.88rem;
    font-weight: 700;
    transition: border-color 0.2s, box-shadow 0.2s, opacity 0.2s;
  }

  .rc-nav a:hover {
    border-color: var(--yellow);
    box-shadow: 0 2px 8px rgba(255, 215, 6, 0.2);
    color: var(--offblack);
    text-decoration: none;
  }

  .rc-nav a.rc-active {
    border-color: var(--yellow);
    background: var(--yellow);
    color: var(--offblack);
  }

  .rc-snum {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    background: var(--offblack);
    color: var(--yellow);
    font-size: 12px;
    font-weight: 700;
    flex-shrink: 0;
  }

  .rc-container {
    padding: 0 0 80px;
  }

  .rc-sec {
    display: block;
    margin-bottom: 56px;
  }

  .rc-sec-header {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    margin-bottom: 32px;
  }

  .rc-sec-icon {
    width: 56px;
    height: 56px;
    border-radius: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 26px;
    flex-shrink: 0;
    background: var(--yellow);
  }

  .rc-sec-header h2 {
    font-size: 1.7rem;
    font-weight: 800;
    margin-bottom: 6px;
    color: var(--offblack);
  }

  .rc-sec-header > div > p {
    color: var(--gray);
    font-size: 0.95rem;
    line-height: 1.5;
  }

  .rc-video-card {
    display: flex;
    align-items: center;
    gap: 24px;
    background: var(--darkgray);
    border-radius: 16px;
    padding: 32px;
    margin-bottom: 24px;
    text-decoration: none;
    transition: opacity 0.2s;
  }

  .rc-video-card:hover {
    opacity: 0.88;
    text-decoration: none;
  }

  .rc-play {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background: var(--yellow);
    color: var(--offblack);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    flex-shrink: 0;
  }

  .rc-vmeta {
    color: white;
  }

  .rc-vtag {
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: var(--lightgray);
    margin-bottom: 6px;
  }

  .rc-vmeta h3 {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 4px;
    color: var(--offwhite);
  }

  .rc-vmeta p {
    font-size: 0.85rem;
    color: var(--lightgray);
    margin: 0;
  }

  .rc-3col {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 14px;
    margin-bottom: 24px;
  }

  .rc-wi {
    background: var(--offwhite);
    border-radius: 14px;
    padding: 20px;
    border: 1px solid var(--lightgray);
    text-align: center;
  }

  .rc-wi-icon {
    font-size: 30px;
    margin-bottom: 10px;
  }

  .rc-wi h4 {
    font-size: 0.88rem;
    font-weight: 700;
    margin-bottom: 5px;
    color: var(--offblack);
  }

  .rc-wi p {
    font-size: 0.80rem;
    color: var(--gray);
    line-height: 1.5;
    margin: 0;
  }

  .rc-card {
    background: var(--offwhite);
    border-radius: 16px;
    padding: 28px;
    border: 1px solid var(--lightgray);
    margin-bottom: 24px;
  }

  .rc-subhead {
    font-size: 1rem;
    font-weight: 700;
    margin-bottom: 16px;
    color: var(--offblack);
  }

  .rc-journey {
    display: flex;
    overflow-x: auto;
    padding-bottom: 8px;
  }

  .rc-jstep {
    flex: 1;
    min-width: 100px;
    text-align: center;
    position: relative;
  }

  .rc-jstep::after {
    content: '→';
    position: absolute;
    right: -12px;
    top: 10px;
    font-size: 18px;
    color: var(--lightgray);
  }

  .rc-jstep:last-child::after {
    display: none;
  }

  .rc-jdot {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    background: var(--offblack);
    color: var(--yellow);
    font-size: 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 6px;
  }

  .rc-jlbl {
    font-size: 0.72rem;
    font-weight: 700;
    color: var(--darkgray);
  }

  .rc-warning {
    background: #FFF8E6;
    border: 1px solid var(--orange);
    border-radius: 14px;
    padding: 16px 20px;
    margin-bottom: 24px;
    display: flex;
    gap: 14px;
    align-items: flex-start;
  }

  .rc-wicon {
    font-size: 20px;
    flex-shrink: 0;
  }

  .rc-warning p {
    font-size: 0.87rem;
    color: var(--darkgray);
    line-height: 1.55;
    margin: 0;
  }

  .rc-tip {
    background: var(--offwhite);
    border: 2px solid var(--yellow);
    border-radius: 14px;
    padding: 20px 24px;
    margin-bottom: 24px;
    display: flex;
    gap: 16px;
    align-items: flex-start;
  }

  .rc-tipicon {
    font-size: 24px;
    flex-shrink: 0;
  }

  .rc-tip h4 {
    font-size: 0.82rem;
    font-weight: 700;
    color: var(--offblack);
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-bottom: 4px;
  }

  .rc-tip p {
    font-size: 0.87rem;
    color: var(--darkgray);
    line-height: 1.55;
    margin: 0;
  }

  .rc-sec-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    margin-top: 24px;
    flex-wrap: wrap;
  }

  .rc-btn-prev,
  .rc-btn-next,
  .rc-btn-disabled {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 11px 18px;
    border-radius: 10px;
    font-weight: 700;
    font-size: 0.88rem;
    text-decoration: none;
    border: 1px solid var(--lightgray);
  }

  .rc-btn-prev {
    background: white;
    color: var(--darkgray);
  }

  .rc-btn-next {
    background: var(--yellow);
    color: var(--offblack);
    border-color: var(--yellow);
  }

  .rc-btn-disabled {
    background: var(--brightgray);
    color: var(--gray);
    cursor: default;
  }

  .rc-link-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--yellow);
    color: var(--offblack);
    text-decoration: none;
    padding: 11px 22px;
    border-radius: 10px;
    font-weight: 700;
    font-size: 0.88rem;
    transition: opacity 0.2s;
    margin-bottom: 8px;
    margin-right: 8px;
  }

  .rc-link-btn:hover {
    opacity: 0.85;
    text-decoration: none;
  }

  .rc-link-sec {
    background: var(--offwhite);
    color: var(--darkgray);
    border: 1px solid var(--lightgray);
  }

  .rc-link-sec:hover {
    background: var(--brightgray);
  }

  @media (max-width: 640px) {
    .rc-hero h1 { font-size: 1.7rem; }
    .rc-3col { grid-template-columns: 1fr; }
    .rc-hero-stats { gap: 20px; }
    .rc-sec-header { flex-direction: column; gap: 12px; }
    .rc-hero { padding: 36px 20px 32px; }
    .rc-video-card { flex-direction: column; padding: 24px; }
    .rc-nav { flex-direction: column; }
    .rc-sec-nav { flex-direction: column; align-items: stretch; }
  }
</style>

<div class="rc-guide">
  <div class="rc-hero">
    <div class="rc-badge">🚀 Getting Started</div>
    <h1>Welcome to Recurly Commerce</h1>
    <p>You've installed the app — now let's get your subscriptions live. Follow these 6 steps and you'll be up and running in no time.</p>
    <div class="rc-hero-stats">
      <div><div class="rc-num">6</div><div class="rc-lbl">Setup Steps</div></div>
      <div><div class="rc-num">~60</div><div class="rc-lbl">Min to Launch</div></div>
      <div><div class="rc-num">0</div><div class="rc-lbl">Code Required</div></div>
    </div>
  </div>

  <nav class="rc-nav">
    <a class="rc-active" href="https://docs.recurly.com/recurly-commerce/docs/navigate-intro-to-commerce-navigate"><span class="rc-snum">1</span>Intro</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-subscription-plans"><span class="rc-snum">2</span>Subscription Plans</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-storefront-setup"><span class="rc-snum">3</span>Storefront Setup</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-customer-portal"><span class="rc-snum">4</span>Customer Portal</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-notifications-commerce"><span class="rc-snum">5</span>Notifications</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-integrations-commerce"><span class="rc-snum">6</span>Integrations</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-launch-commerce"><span class="rc-snum">✓</span>Launch!</a>
  </nav>

  <div class="rc-container">
    <div class="rc-sec">
      <div class="rc-sec-header">
        <div class="rc-sec-icon">🧭</div>
        <div>
          <h2>What is Recurly Commerce?</h2>
          <p>A quick orientation before you dive in — understand what you just installed and what it can do for your Shopify store.</p>
        </div>
      </div>

      <div class="rc-video-card" style="padding: 0; overflow: hidden; height: 480px;">
        <iframe 
          src="https://drive.google.com/file/d/1lahRtRmcqIenNmYvGZ3qLR8FJ7t-1IDG/preview" 
          width="100%" 
          height="100%" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
        </iframe>
      </div>
      <div class="rc-3col">
        <div class="rc-wi"><div class="rc-wi-icon">📦</div><h4>Subscription Management</h4><p>Create recurring product offers with flexible billing frequencies and discounts — all without touching code.</p></div>
        <div class="rc-wi"><div class="rc-wi-icon">🛍️</div><h4>Native Shopify Integration</h4><p>Everything lives inside your Shopify admin. No separate dashboard to juggle — it's all connected.</p></div>
        <div class="rc-wi"><div class="rc-wi-icon">💳</div><h4>Revenue Recovery</h4><p>Automatically retries failed payments and notifies customers so you lose less revenue to billing hiccups.</p></div>
      </div>

      <div class="rc-card">
        <h3 class="rc-subhead">🗺️ Your Onboarding Journey</h3>
        <div class="rc-journey">
          <div class="rc-jstep"><div class="rc-jdot">📋</div><div class="rc-jlbl">Choose Plan</div></div>
          <div class="rc-jstep"><div class="rc-jdot">🏷️</div><div class="rc-jlbl">Create Sub Plans</div></div>
          <div class="rc-jstep"><div class="rc-jdot">🛒</div><div class="rc-jlbl">Set Up Storefront</div></div>
          <div class="rc-jstep"><div class="rc-jdot">👤</div><div class="rc-jlbl">Customer Portal</div></div>
          <div class="rc-jstep"><div class="rc-jdot">🔔</div><div class="rc-jlbl">Notifications</div></div>
          <div class="rc-jstep"><div class="rc-jdot">🔗</div><div class="rc-jlbl">Integrations</div></div>
        </div>
      </div>

      <div class="rc-warning">
        <span class="rc-wicon">⚠️</span>
        <p><strong>Before you begin:</strong> Make sure the Shopify user setting up Recurly Commerce has <strong>"Approve app charges"</strong> permission enabled. Without this, you won't be able to activate a plan. Check this under Shopify Admin → Settings → Users &amp; Permissions.</p>
      </div>

      <div class="rc-tip">
        <span class="rc-tipicon">💡</span>
        <div>
          <h4>Pro Tip · Set Your Goal First</h4>
          <p>Before configuring anything, ask yourself: <em>What products do I want to offer as subscriptions? How often should customers receive them?</em> Having a clear picture of your offer structure will make every step below feel fast and intuitive.</p>
        </div>
      </div>

      <div class="rc-sec-nav">
        <span class="rc-btn-disabled">🎯 Start Path</span>
        <a class="rc-btn-next" href="https://docs.recurly.com/recurly-commerce/docs/navigate-subscription-plans">Next: Subscription Plans →</a>
      </div>

      <div style="margin-top:24px;">
        <h3 class="rc-subhead">📚 Additional Resources</h3>
        <a class="rc-link-btn" href="https://navigate.recurly.com/commerce/launch-smarter/" target="_blank" rel="noopener noreferrer">▶ Full On-Demand Video</a>
        <a class="rc-link-btn rc-link-sec" href="https://docs.recurly.com/recurly-commerce/docs/navigate-getting-started-rc" target="_blank" rel="noopener noreferrer">📖 Recurly Docs</a>
        <a class="rc-link-btn rc-link-sec" href="https://support.recurly.com" target="_blank" rel="noopener noreferrer">🎧 Recurly Support</a>
        <a class="rc-link-btn rc-link-sec" href="https://docs.google.com/presentation/d/1hEvBMcNC7PpQj-Fl-IMz6QM6cLfLi92ECI5gq_A_XbI/edit" target="_blank" rel="noopener noreferrer">📊 Presentation Deck</a>
      </div>
    </div>
  </div>
</div>
`}</HTMLBlock>

<br />
