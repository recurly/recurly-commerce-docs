---
title: Notifications
deprecated: false
hidden: true
metadata:
  robots: index
---
<HTMLBlock>{`
<style>
  .rc-guide{--yellow:#FFD706;--orange:#FF8200;--vermillion:#FF5810;--offblack:#0D0D0B;--darkgray:#32312D;--gray:#807D73;--lightgray:#CCC9B8;--brightgray:#F1EFE3;--offwhite:#FFFDF2;font-family:'Segoe UI',system-ui,sans-serif}
  .rc-hero{background:var(--offblack);color:#fff;padding:56px 40px 48px;text-align:center;border-radius:16px;margin-bottom:0}
  .rc-badge{display:inline-block;background:var(--yellow);color:var(--offblack);border-radius:20px;padding:6px 18px;font-size:13px;font-weight:700;letter-spacing:1px;text-transform:uppercase;margin-bottom:20px}
  .rc-hero h1{font-size:2.4rem;font-weight:800;line-height:1.15;margin-bottom:14px;color:var(--offwhite)}
  .rc-hero>p{font-size:1.05rem;opacity:.8;max-width:600px;margin:0 auto 32px;color:var(--lightgray)}
  .rc-hero-stats{display:flex;justify-content:center;gap:40px;flex-wrap:wrap}
  .rc-num{font-size:1.8rem;font-weight:800;color:var(--yellow)}
  .rc-lbl{font-size:.8rem;color:var(--lightgray);text-transform:uppercase;letter-spacing:.5px}
  .rc-nav{display:flex;flex-wrap:wrap;gap:10px;margin:24px 0 28px}
  .rc-nav a{display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:12px;border:1px solid var(--lightgray);background:#fff;color:var(--darkgray);text-decoration:none;font-size:.88rem;font-weight:700}
  .rc-nav a:hover{border-color:var(--yellow);box-shadow:0 2px 8px rgba(255,215,6,.2);color:var(--offblack);text-decoration:none}
  .rc-nav a.rc-active{border-color:var(--yellow);background:var(--yellow);color:var(--offblack)}
  .rc-snum{display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:50%;background:var(--offblack);color:var(--yellow);font-size:12px;font-weight:700;flex-shrink:0}
  .rc-sec{display:block;margin-bottom:56px}
  .rc-sec-header{display:flex;align-items:flex-start;gap:20px;margin-bottom:32px}
  .rc-sec-icon{width:56px;height:56px;border-radius:16px;display:flex;align-items:center;justify-content:center;font-size:26px;flex-shrink:0;background:var(--yellow)}
  .rc-sec-header h2{font-size:1.7rem;font-weight:800;margin-bottom:6px;color:var(--offblack)}
  .rc-sec-header>div>p{color:var(--gray);font-size:.95rem;line-height:1.5}
  .rc-video-card{display:flex;align-items:center;gap:24px;background:var(--darkgray);border-radius:16px;padding:32px;margin-bottom:24px;text-decoration:none}
  .rc-video-card:hover{opacity:.88;text-decoration:none}
  .rc-video-alt{background:#32312D;margin-top:-8px}
  .rc-play{width:60px;height:60px;border-radius:50%;background:var(--yellow);color:var(--offblack);display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
  .rc-play-orange{background:var(--orange);color:#fff}
  .rc-vmeta{color:#fff}
  .rc-vtag{font-size:11px;text-transform:uppercase;letter-spacing:1px;color:var(--lightgray);margin-bottom:6px}
  .rc-vmeta h3{font-size:1.05rem;font-weight:700;margin-bottom:4px;color:var(--offwhite)}
  .rc-vmeta p{font-size:.85rem;color:var(--lightgray);margin:0}
  .rc-steps{display:flex;flex-direction:column;gap:16px;margin-bottom:28px}
  .rc-step{background:var(--offwhite);border-radius:14px;padding:22px 26px;border:1px solid var(--lightgray);display:flex;gap:18px;align-items:flex-start}
  .rc-sbadge{width:38px;height:38px;border-radius:10px;background:var(--offblack);color:var(--yellow);font-weight:800;font-size:15px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
  .rc-step h3{font-size:.98rem;font-weight:700;margin-bottom:5px;color:var(--offblack)}
  .rc-step p{font-size:.87rem;color:var(--gray);line-height:1.6;margin:0}
  .rc-tip{background:var(--offwhite);border:2px solid var(--yellow);border-radius:14px;padding:20px 24px;margin-bottom:24px;display:flex;gap:16px;align-items:flex-start}
  .rc-tipicon{font-size:24px;flex-shrink:0}
  .rc-tip h4{font-size:.82rem;font-weight:700;color:var(--offblack);text-transform:uppercase;letter-spacing:.5px;margin-bottom:4px}
  .rc-tip p{font-size:.87rem;color:var(--darkgray);line-height:1.55;margin:0}
  .rc-warning{background:#FFF8E6;border:1px solid var(--orange);border-radius:14px;padding:16px 20px;margin-bottom:24px;display:flex;gap:14px;align-items:flex-start}
  .rc-wicon{font-size:20px;flex-shrink:0}
  .rc-warning p{font-size:.87rem;color:var(--darkgray);line-height:1.55;margin:0}
  .rc-checklist{background:var(--offwhite);border-radius:16px;border:1px solid var(--lightgray);overflow:hidden;margin-bottom:28px}
  .rc-cl-header{padding:16px 22px;border-bottom:1px solid var(--brightgray);display:flex;align-items:center;gap:10px;background:var(--offblack)}
  .rc-cl-header h3{font-size:.88rem;font-weight:700;text-transform:uppercase;letter-spacing:.5px;color:var(--yellow);margin:0}
  .rc-cli{padding:13px 22px;border-bottom:1px solid var(--brightgray);display:flex;align-items:flex-start;gap:14px}
  .rc-cli:last-child{border-bottom:none}
  .rc-cb{width:22px;height:22px;border-radius:6px;border:2px solid var(--lightgray);flex-shrink:0;margin-top:1px;background:#fff;display:flex;align-items:center;justify-content:center;font-size:12px;color:var(--gray)}
  .rc-clab{font-size:.88rem;color:var(--darkgray);line-height:1.4}
  .rc-clab span{display:block;font-size:.78rem;color:var(--gray);margin-top:2px}
  .rc-sec-nav{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-top:24px;flex-wrap:wrap}
  .rc-btn-prev,.rc-btn-next{display:inline-flex;align-items:center;justify-content:center;padding:11px 18px;border-radius:10px;font-weight:700;font-size:.88rem;text-decoration:none;border:1px solid var(--lightgray)}
  .rc-btn-prev{background:#fff;color:var(--darkgray)}
  .rc-btn-next{background:var(--yellow);color:var(--offblack);border-color:var(--yellow)}
  .rc-subhead{font-size:1rem;font-weight:700;margin-bottom:16px;color:var(--offblack)}
  .rc-link-btn{display:inline-flex;align-items:center;gap:8px;background:var(--yellow);color:var(--offblack);text-decoration:none;padding:11px 22px;border-radius:10px;font-weight:700;font-size:.88rem;margin-bottom:8px;margin-right:8px}
  .rc-link-sec{background:var(--offwhite);color:var(--darkgray);border:1px solid var(--lightgray)}
  @media(max-width:640px){.rc-hero h1{font-size:1.7rem}.rc-2col{grid-template-columns:1fr}.rc-hero-stats{gap:20px}.rc-sec-header{flex-direction:column;gap:12px}.rc-video-card{flex-direction:column;padding:24px}.rc-nav,.rc-sec-nav{flex-direction:column;align-items:stretch}}
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
    <a class="rc-active" href="https://docs.recurly.com/recurly-commerce/docs/navigate-notifications-commerce"><span class="rc-snum">5</span>Notifications</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-integrations-commerce"><span class="rc-snum">6</span>Integrations</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-launch-commerce"><span class="rc-snum">✓</span>Launch!</a>
  </nav>

  <div class="rc-sec">
    <div class="rc-sec-header">
      <div class="rc-sec-icon">🔔</div>
      <div>
        <h2>Step 4: Configure Notifications</h2>
        <p>Subscribers who feel informed stay longer. Set up automated emails and SMS to keep customers in the loop at every stage — from first order to renewal.</p>
      </div>
    </div>

    <div class="rc-video-card" style="padding: 0; overflow: hidden; height: 480px;">
      <iframe 
        src="https://drive.google.com/file/d/1ucFUfkmnG4_sYTybWNzb08jfWTTWScYz_5UeZiFJmI0/preview" 
        width="100%" 
        height="100%" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>

    <div class="rc-video-card rc-video-alt" style="padding: 0; overflow: hidden; height: 480px;">
      <iframe 
        src="https://drive.google.com/file/d/1cIEPUE97awZVH17kXggJC4oANRbOa8XV3CHM5jld_4k/preview" 
        width="100%" 
        height="100%" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>

    <div class="rc-steps">
      <div class="rc-step"><div class="rc-sbadge">1</div><div><h3>Go to Notifications in Recurly Commerce</h3><p>Open the Notifications tab in your app dashboard. Here you'll manage all transactional emails and SMS across the subscriber lifecycle.</p></div></div>
      <div class="rc-step"><div class="rc-sbadge">2</div><div><h3>Configure Transactional Emails</h3><p>Enable and customize automated emails for key events: order placed, upcoming renewal, failed payment, subscription paused, and more. These are free and built-in.</p></div></div>
      <div class="rc-step"><div class="rc-sbadge">3</div><div><h3>Enable SMS Alerts (Optional)</h3><p>Add concise SMS notifications for high-urgency moments like payment failures or upcoming order alerts. SMS drives faster action than email for billing issues.</p></div></div>
      <div class="rc-step"><div class="rc-sbadge">4</div><div><h3>Set Up Renewal Reminders</h3><p>Configure how many days before renewal to notify customers (1–180 days). This reduces "I didn't know I was going to be charged" disputes and builds trust.</p></div></div>
      <div class="rc-step"><div class="rc-sbadge">5</div><div><h3>Brand Your Email Templates</h3><p>Customize subject lines, copy, and visual styling to match your brand. Branded emails feel personal — generic ones get ignored or marked as spam.</p></div></div>
    </div>

    <div class="rc-tip">
      <span class="rc-tipicon">💡</span>
      <div><h4>Pro Tip · The Notifications That Matter Most</h4><p>Prioritize these three from day one: (1) <strong>Upcoming renewal reminder</strong> — sent 3–5 days before charge, prevents disputes. (2) <strong>Failed payment alert</strong> — fast communication recovers revenue before subscribers churn passively. (3) <strong>Order confirmation</strong> — builds excitement and trust after every charge.</p></div>
    </div>

    <div class="rc-warning">
      <span class="rc-wicon">⚠️</span>
      <p><strong>Compliance note:</strong> In many regions, renewal reminder emails are legally required before charging a customer. Make sure renewal reminders are enabled before you go live — this protects both your customers and your business.</p>
    </div>

    <div class="rc-checklist">
      <div class="rc-cl-header"><span>✅</span><h3>Step 4 Checklist</h3></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Order confirmation email enabled and branded<span>Sent immediately after every subscription charge</span></div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Upcoming renewal reminder configured (3–7 days prior)<span>Reduces disputes and builds subscriber trust</span></div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Failed payment notification enabled<span>Critical for passive churn prevention</span></div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Email templates branded (logo, colors, tone of voice)<span>Consistency with your store builds trust</span></div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">SMS alerts reviewed (enable if available on your plan)<span>High-urgency events benefit from SMS reach</span></div></div>
    </div>

    <div class="rc-sec-nav">
      <a class="rc-btn-prev" href="https://docs.recurly.com/recurly-commerce/docs/navigate-customer-portal">← Customer Portal</a>
      <a class="rc-btn-next" href="https://docs.recurly.com/recurly-commerce/docs/navigate-integrations-commerce">Next: Integrations →</a>
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
