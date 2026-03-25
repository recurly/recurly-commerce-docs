---
title: Customer Portal
deprecated: false
hidden: true
metadata:
  robots: index
---
<HTMLBlock>{`
<style>
  .rc-guide{--yellow:#FFD706;--orange:#FF8200;--offblack:#0D0D0B;--darkgray:#32312D;--gray:#807D73;--lightgray:#CCC9B8;--brightgray:#F1EFE3;--offwhite:#FFFDF2;font-family:'Segoe UI',system-ui,sans-serif}
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
  .rc-play{width:60px;height:60px;border-radius:50%;background:var(--yellow);color:var(--offblack);display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
  .rc-vmeta{color:#fff}
  .rc-vtag{font-size:11px;text-transform:uppercase;letter-spacing:1px;color:var(--lightgray);margin-bottom:6px}
  .rc-vmeta h3{font-size:1.05rem;font-weight:700;margin-bottom:4px;color:var(--offwhite)}
  .rc-vmeta p{font-size:.85rem;color:var(--lightgray);margin:0}
  .rc-steps{display:flex;flex-direction:column;gap:16px;margin-bottom:28px}
  .rc-step{background:var(--offwhite);border-radius:14px;padding:22px 26px;border:1px solid var(--lightgray);display:flex;gap:18px;align-items:flex-start}
  .rc-sbadge{width:38px;height:38px;border-radius:10px;background:var(--offblack);color:var(--yellow);font-weight:800;font-size:15px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
  .rc-step h3{font-size:.98rem;font-weight:700;margin-bottom:5px;color:var(--offblack)}
  .rc-step p{font-size:.87rem;color:var(--gray);line-height:1.6;margin:0}
  .rc-subhead{font-size:1rem;font-weight:700;margin-bottom:16px;color:var(--offblack)}
  .rc-2col{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:26px}
  .rc-opt{background:var(--offwhite);border:1px solid var(--lightgray);border-radius:14px;padding:18px}
  .rc-oicon{font-size:22px;margin-bottom:8px}
  .rc-opt h4{font-size:.92rem;font-weight:700;margin-bottom:5px;color:var(--offblack)}
  .rc-opt p{font-size:.82rem;color:var(--gray);line-height:1.5;margin:0}
  .rc-tag{display:inline-block;margin-top:10px;padding:3px 10px;border-radius:20px;font-size:11px;font-weight:700;background:var(--offblack);color:var(--yellow)}
  .rc-tip{background:var(--offwhite);border:2px solid var(--yellow);border-radius:14px;padding:20px 24px;margin-bottom:24px;display:flex;gap:16px;align-items:flex-start}
  .rc-tipicon{font-size:24px;flex-shrink:0}
  .rc-tip h4{font-size:.82rem;font-weight:700;color:var(--offblack);text-transform:uppercase;letter-spacing:.5px;margin-bottom:4px}
  .rc-tip p{font-size:.87rem;color:var(--darkgray);line-height:1.55;margin:0}
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
  .rc-link-btn{display:inline-flex;align-items:center;gap:8px;background:var(--yellow);color:var(--offblack);text-decoration:none;padding:11px 22px;border-radius:10px;font-weight:700;font-size:.88rem;margin-bottom:8px;margin-right:8px}
  .rc-link-sec{background:var(--offwhite);color:var(--darkgray);border:1px solid var(--lightgray)}
  @media(max-width:640px){.rc-hero h1{font-size:1.7rem}.rc-2col{grid-template-columns:1fr}.rc-hero-stats{gap:20px}.rc-sec-header{flex-direction:column;gap:12px}.rc-hero{padding:36px 20px 32px}.rc-video-card{flex-direction:column;padding:24px}.rc-nav,.rc-sec-nav{flex-direction:column;align-items:stretch}}
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
    <a class="rc-active" href="https://docs.recurly.com/recurly-commerce/docs/navigate-customer-portal"><span class="rc-snum">4</span>Customer Portal</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-notifications-commerce"><span class="rc-snum">5</span>Notifications</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-integrations-commerce"><span class="rc-snum">6</span>Integrations</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-launch-commerce"><span class="rc-snum">✓</span>Launch!</a>
  </nav>

  <div class="rc-sec">
    <div class="rc-sec-header">
      <div class="rc-sec-icon">👤</div>
      <div>
        <h2>Step 3: Configure the Customer Portal</h2>
        <p>The Customer Portal is where your subscribers manage everything about their subscription. A well-configured portal reduces support tickets and keeps customers from cancelling.</p>
      </div>
    </div>

    <div class="rc-video-card" style="padding: 0; overflow: hidden; height: 480px;">
      <iframe 
        src="https://drive.google.com/file/d/1bB2CgaV8TvZ0J8XE4834PgdY9z99pR7fZyA9lNzz7Bo/preview" 
        width="100%" 
        height="100%" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
    <div class="rc-steps">
      <div class="rc-step"><div class="rc-sbadge">1</div><div><h3>Navigate to Customer Portal in the App</h3><p>In Recurly Commerce, click the <strong>Customer Portal</strong> tab. Note: this feature must be enabled on your plan before it becomes available.</p></div></div>
      <div class="rc-step"><div class="rc-sbadge">2</div><div><h3>Enable Self-Service Actions</h3><p>Toggle the subscriber permissions you want to allow. Each toggle applies immediately after saving, so review carefully before clicking Save.</p></div></div>
      <div class="rc-step"><div class="rc-sbadge">3</div><div><h3>Match Your Brand</h3><p>Customize portal colors, fonts, borders, and copy to align with your storefront. A seamless experience between your store and portal builds trust.</p></div></div>
      <div class="rc-step"><div class="rc-sbadge">4</div><div><h3>Set Up Cancellation Flows</h3><p>Configure what happens when a subscriber tries to cancel — offer a pause, a discount, or gather feedback. This is one of your most powerful churn prevention tools.</p></div></div>
    </div>

    <h3 class="rc-subhead">🎛️ Self-Service Permissions — What to Enable</h3>
    <div class="rc-2col">
      <div class="rc-opt"><div class="rc-oicon">⏭️</div><h4>Skip Next Delivery</h4><p>Let customers skip without cancelling. Perfect for vacations or "I still have some left" moments. Prevents a cancel that was really just a pause.</p><span class="rc-tag">Highly Recommended</span></div>
      <div class="rc-opt"><div class="rc-oicon">📅</div><h4>Change Renewal Date</h4><p>Allow customers to push or pull their next charge date. Flexibility here reduces "I got charged before I expected" cancellations.</p><span class="rc-tag">Recommended</span></div>
      <div class="rc-opt"><div class="rc-oicon">🔀</div><h4>Swap Products</h4><p>Let subscribers switch SKUs within a plan. Keep them in the ecosystem even when preferences change — swapping is always better than cancelling.</p><span class="rc-tag">Recommended</span></div>
      <div class="rc-opt"><div class="rc-oicon">⏸️</div><h4>Pause Subscription</h4><p>Offer an indefinite or limited pause instead of a hard cancel. Customers who pause are far more likely to resume than those who cancel outright.</p><span class="rc-tag">Churn Saver</span></div>
    </div>

    <div class="rc-tip">
      <span class="rc-tipicon">💡</span>
      <div><h4>Pro Tip · Churn Prevention Flows</h4><p>Before a subscriber can cancel, show them a retention offer — a discount, a skip option, or a pause. This single feature can recover a significant percentage of would-be cancellations. Set it up before you go live so it's working from day one.</p></div>
    </div>

    <div class="rc-checklist">
      <div class="rc-cl-header"><span>✅</span><h3>Step 3 Checklist</h3></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Customer Portal feature confirmed active on your plan<span>Check Plan settings if this section is unavailable</span></div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Self-service permissions configured (skip, swap, pause, etc.)<span>Enable at least skip + change renewal date</span></div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Portal branding matched to your storefront<span>Colors, fonts, and copy aligned</span></div></div>
      <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Cancellation/churn prevention flow configured<span>At minimum, offer a pause or discount before cancel</span></div></div>
    </div>

    <div class="rc-sec-nav">
      <a class="rc-btn-prev" href="https://docs.recurly.com/recurly-commerce/docs/navigate-storefront-setup">← Storefront Setup</a>
      <a class="rc-btn-next" href="https://docs.recurly.com/recurly-commerce/docs/navigate-notifications-commerce">Next: Notifications →</a>
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
