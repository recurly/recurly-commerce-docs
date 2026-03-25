---
title: Ready to Launch!
deprecated: false
hidden: true
metadata:
  robots: index
---
<HTMLBlock>{`
<style>
  .rc-guide{
    --yellow:#FFD706;
    --orange:#FF8200;
    --vermillion:#FF5810;
    --salmon:#FF9D88;
    --offblack:#0D0D0B;
    --darkgray:#32312D;
    --gray:#807D73;
    --lightgray:#CCC9B8;
    --brightgray:#F1EFE3;
    --offwhite:#FFFDF2;
    font-family:'Segoe UI',system-ui,sans-serif;
  }

  .rc-hero{
    background:var(--offblack);
    color:#fff;
    padding:56px 40px 48px;
    text-align:center;
    border-radius:16px;
    margin-bottom:0;
  }

  .rc-badge{
    display:inline-block;
    background:var(--yellow);
    color:var(--offblack);
    border-radius:20px;
    padding:6px 18px;
    font-size:13px;
    font-weight:700;
    letter-spacing:1px;
    text-transform:uppercase;
    margin-bottom:20px;
  }

  .rc-hero h1{
    font-size:2.4rem;
    font-weight:800;
    line-height:1.15;
    margin-bottom:14px;
    color:var(--offwhite);
  }

  .rc-hero > p{
    font-size:1.05rem;
    opacity:.8;
    max-width:600px;
    margin:0 auto 32px;
    color:var(--lightgray);
  }

  .rc-hero-stats{
    display:flex;
    justify-content:center;
    gap:40px;
    flex-wrap:wrap;
  }

  .rc-num{
    font-size:1.8rem;
    font-weight:800;
    color:var(--yellow);
  }

  .rc-lbl{
    font-size:.8rem;
    color:var(--lightgray);
    text-transform:uppercase;
    letter-spacing:.5px;
  }

  .rc-nav{
    display:flex;
    flex-wrap:wrap;
    gap:10px;
    margin:24px 0 28px;
  }

  .rc-nav a{
    display:inline-flex;
    align-items:center;
    gap:8px;
    padding:10px 14px;
    border-radius:12px;
    border:1px solid var(--lightgray);
    background:#fff;
    color:var(--darkgray);
    text-decoration:none;
    font-size:.88rem;
    font-weight:700;
    transition:border-color .2s, box-shadow .2s, opacity .2s;
  }

  .rc-nav a:hover{
    border-color:var(--yellow);
    box-shadow:0 2px 8px rgba(255,215,6,.2);
    color:var(--offblack);
    text-decoration:none;
  }

  .rc-nav a.rc-active{
    border-color:var(--yellow);
    background:var(--yellow);
    color:var(--offblack);
  }

  .rc-snum{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    width:24px;
    height:24px;
    border-radius:50%;
    background:var(--offblack);
    color:var(--yellow);
    font-size:12px;
    font-weight:700;
    flex-shrink:0;
  }

  .rc-sec{
    display:block;
    margin-bottom:56px;
  }

  .rc-complete{
    background:var(--offblack);
    border-radius:16px;
    padding:40px;
    text-align:center;
    margin-bottom:28px;
    color:#fff;
  }

  .rc-complete h2{
    font-size:1.8rem;
    font-weight:800;
    margin:12px 0 10px;
    color:var(--yellow);
  }

  .rc-complete p{
    color:var(--lightgray);
    font-size:.95rem;
    margin:0;
  }

  .rc-checklist{
    background:var(--offwhite);
    border-radius:16px;
    border:1px solid var(--lightgray);
    overflow:hidden;
    margin-bottom:28px;
  }

  .rc-cl-header{
    padding:16px 22px;
    border-bottom:1px solid var(--brightgray);
    display:flex;
    align-items:center;
    gap:10px;
    background:var(--offblack);
  }

  .rc-cl-header h3{
    font-size:.88rem;
    font-weight:700;
    text-transform:uppercase;
    letter-spacing:.5px;
    color:var(--yellow);
    margin:0;
  }

  .rc-cli{
    padding:13px 22px;
    border-bottom:1px solid var(--brightgray);
    display:flex;
    align-items:flex-start;
    gap:14px;
  }

  .rc-cli:last-child{
    border-bottom:none;
  }

  .rc-cb{
    width:22px;
    height:22px;
    border-radius:6px;
    border:2px solid var(--lightgray);
    flex-shrink:0;
    margin-top:1px;
    background:#fff;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:12px;
    color:var(--gray);
  }

  .rc-clab{
    font-size:.88rem;
    color:var(--darkgray);
    line-height:1.4;
  }

  .rc-card{
    background:var(--offwhite);
    border-radius:16px;
    padding:28px;
    border:1px solid var(--lightgray);
    margin-bottom:24px;
  }

  .rc-subhead{
    font-size:1rem;
    font-weight:700;
    margin-bottom:16px;
    color:var(--offblack);
  }

  .rc-steps{
    display:flex;
    flex-direction:column;
    gap:16px;
    margin-bottom:28px;
  }

  .rc-step{
    background:var(--offwhite);
    border-radius:14px;
    padding:22px 26px;
    border:1px solid var(--lightgray);
    display:flex;
    gap:18px;
    align-items:flex-start;
    transition:box-shadow .2s;
  }

  .rc-step:hover{
    box-shadow:0 4px 16px rgba(13,13,11,.08);
  }

  .rc-sbadge-orange,
  .rc-sbadge-verm,
  .rc-sbadge-dark{
    width:38px;
    height:38px;
    border-radius:10px;
    font-weight:800;
    font-size:15px;
    display:flex;
    align-items:center;
    justify-content:center;
    flex-shrink:0;
  }

  .rc-sbadge-orange{
    background:var(--orange);
    color:#fff;
  }

  .rc-sbadge-verm{
    background:var(--vermillion);
    color:#fff;
  }

  .rc-sbadge-dark{
    background:var(--darkgray);
    color:var(--yellow);
  }

  .rc-step h3{
    font-size:.98rem;
    font-weight:700;
    margin-bottom:5px;
    color:var(--offblack);
  }

  .rc-step p{
    font-size:.87rem;
    color:var(--gray);
    line-height:1.6;
    margin:0;
  }

  .rc-tip{
    background:var(--offwhite);
    border:2px solid var(--yellow);
    border-radius:14px;
    padding:20px 24px;
    margin-bottom:24px;
    display:flex;
    gap:16px;
    align-items:flex-start;
  }

  .rc-tipicon{
    font-size:24px;
    flex-shrink:0;
  }

  .rc-tip h4{
    font-size:.82rem;
    font-weight:700;
    color:var(--offblack);
    text-transform:uppercase;
    letter-spacing:.5px;
    margin-bottom:4px;
  }

  .rc-tip p{
    font-size:.87rem;
    color:var(--darkgray);
    line-height:1.55;
    margin:0;
  }

  .rc-sec-nav{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:12px;
    margin-top:24px;
    flex-wrap:wrap;
  }

  .rc-btn-prev,
  .rc-btn-disabled{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding:11px 18px;
    border-radius:10px;
    font-weight:700;
    font-size:.88rem;
    text-decoration:none;
    border:1px solid var(--lightgray);
  }

  .rc-btn-prev{
    background:#fff;
    color:var(--darkgray);
  }

  .rc-btn-disabled{
    background:var(--brightgray);
    color:var(--gray);
    cursor:default;
  }

  .rc-link-btn{
    display:inline-flex;
    align-items:center;
    gap:8px;
    background:var(--yellow);
    color:var(--offblack);
    text-decoration:none;
    padding:11px 22px;
    border-radius:10px;
    font-weight:700;
    font-size:.88rem;
    transition:opacity .2s;
    margin-bottom:8px;
    margin-right:8px;
  }

  .rc-link-btn:hover{
    opacity:.85;
    text-decoration:none;
  }

  .rc-link-sec{
    background:var(--offwhite);
    color:var(--darkgray);
    border:1px solid var(--lightgray);
  }

  .rc-link-sec:hover{
    background:var(--brightgray);
  }

  @media(max-width:640px){
    .rc-hero h1{font-size:1.7rem}
    .rc-hero{padding:36px 20px 32px}
    .rc-hero-stats{gap:20px}
    .rc-nav{flex-direction:column}
    .rc-sec-nav{flex-direction:column;align-items:stretch}
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
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-intro-to-commerce"><span class="rc-snum">1</span>Intro</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-subscription-plans"><span class="rc-snum">2</span>Subscription Plans</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-storefront-setup"><span class="rc-snum">3</span>Storefront Setup</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-customer-portal"><span class="rc-snum">4</span>Customer Portal</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-notifications-commerce"><span class="rc-snum">5</span>Notifications</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-integrations-commerce"><span class="rc-snum">6</span>Integrations</a>
    <a class="rc-active" href="https://docs.recurly.com/recurly-commerce/docs/navigate-launch-commerce"><span class="rc-snum">✓</span>Launch!</a>
  </nav>

  <div class="rc-sec">
    <div class="rc-complete">
      <div style="font-size:48px;">🚀</div>
      <h2>You're Ready to Launch!</h2>
      <p>You've completed all the essential setup steps. Here's your final checklist before you go live.</p>
    </div>

    <div class="rc-checklist">
      <div class="rc-cl-header"><span>🏁</span><h3>Final Pre-Launch Checklist</h3></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Subscription plan published with correct products and frequencies</div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Storefront widget live and tested on product pages (desktop + mobile)</div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Customer Portal configured with self-service options and churn flow</div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Renewal reminder and failed payment notifications active</div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Email templates branded to match your store</div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Priority integration(s) connected and verified</div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Placed a test subscription order to verify end-to-end experience</div></div>
    </div>

    <div class="rc-card">
      <h3 class="rc-subhead">📈 What to Focus On After Launch</h3>
      <div class="rc-steps">
        <div class="rc-step"><div class="rc-sbadge-orange">📊</div><div><h3>Monitor Your Analytics Dashboard</h3><p>Check General Analytics and Subscription Analytics weekly. Watch your MRR, churn rate, and active subscriber count — these are your north-star metrics.</p></div></div>
        <div class="rc-step"><div class="rc-sbadge-verm">🔄</div><div><h3>Review Failed Payment Reports</h3><p>Passive churn from failed payments is the silent revenue killer. Review weekly and ensure your dunning (retry) settings are optimized.</p></div></div>
        <div class="rc-step"><div class="rc-sbadge-dark">💌</div><div><h3>Survey Canceling Customers</h3><p>Use your cancellation flow to collect feedback. The reasons customers cancel tell you exactly what to fix — whether it's price, frequency, or product fit.</p></div></div>
      </div>
    </div>

    <div class="rc-tip">
      <span class="rc-tipicon">🎯</span>
      <div><h4>Your 30-Day Goal</h4><p>Focus on <strong>3 things</strong>: (1) Get your first 10 subscribers. (2) Make sure every subscriber receives their renewal reminder on time. (3) Review your cancellation reasons and iterate on your churn prevention flow. Everything else comes second.</p></div>
    </div>

    <div class="rc-sec-nav">
      <a class="rc-btn-prev" href="https://docs.recurly.com/recurly-commerce/docs/navigate-integrations-commerce">← Integrations</a>
      <span class="rc-btn-disabled">🎉 You're Done!</span>
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
`}</HTMLBlock>

<br />
