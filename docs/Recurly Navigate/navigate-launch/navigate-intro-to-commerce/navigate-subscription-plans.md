---
title: Subscription Plans
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
  .rc-hero,.rc-complete{background:var(--offblack);color:white;border-radius:16px}
  .rc-hero{padding:56px 40px 48px;text-align:center;margin-bottom:0}
  .rc-badge{display:inline-block;background:var(--yellow);color:var(--offblack);border-radius:20px;padding:6px 18px;font-size:13px;font-weight:700;letter-spacing:1px;text-transform:uppercase;margin-bottom:20px}
  .rc-hero h1{font-size:2.4rem;font-weight:800;line-height:1.15;margin-bottom:14px;color:var(--offwhite)}
  .rc-hero>p{font-size:1.05rem;opacity:.8;max-width:600px;margin:0 auto 32px;color:var(--lightgray)}
  .rc-hero-stats{display:flex;justify-content:center;gap:40px;flex-wrap:wrap}
  .rc-num{font-size:1.8rem;font-weight:800;color:var(--yellow)}
  .rc-lbl{font-size:.8rem;color:var(--lightgray);text-transform:uppercase;letter-spacing:.5px}
  .rc-nav{display:flex;flex-wrap:wrap;gap:10px;margin:24px 0 28px}
  .rc-nav a{display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:12px;border:1px solid var(--lightgray);background:white;color:var(--darkgray);text-decoration:none;font-size:.88rem;font-weight:700;transition:border-color .2s,box-shadow .2s,opacity .2s}
  .rc-nav a:hover{border-color:var(--yellow);box-shadow:0 2px 8px rgba(255,215,6,.2);color:var(--offblack);text-decoration:none}
  .rc-nav a.rc-active{border-color:var(--yellow);background:var(--yellow);color:var(--offblack)}
  .rc-snum{display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:50%;background:var(--offblack);color:var(--yellow);font-size:12px;font-weight:700;flex-shrink:0}
  .rc-container{padding:0 0 80px}
  .rc-sec{display:block;margin-bottom:56px}
  .rc-sec-header{display:flex;align-items:flex-start;gap:20px;margin-bottom:32px}
  .rc-sec-icon{width:56px;height:56px;border-radius:16px;display:flex;align-items:center;justify-content:center;font-size:26px;flex-shrink:0;background:var(--yellow)}
  .rc-sec-header h2{font-size:1.7rem;font-weight:800;margin-bottom:6px;color:var(--offblack)}
  .rc-sec-header>div>p{color:var(--gray);font-size:.95rem;line-height:1.5}
  .rc-video-card{display:flex;align-items:center;gap:24px;background:var(--darkgray);border-radius:16px;padding:32px;margin-bottom:24px;text-decoration:none;transition:opacity .2s}
  .rc-video-card:hover{opacity:.88;text-decoration:none}
  .rc-play{width:60px;height:60px;border-radius:50%;background:var(--yellow);color:var(--offblack);display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
  .rc-vmeta{color:white}
  .rc-vtag{font-size:11px;text-transform:uppercase;letter-spacing:1px;color:var(--lightgray);margin-bottom:6px}
  .rc-vmeta h3{font-size:1.05rem;font-weight:700;margin-bottom:4px;color:var(--offwhite)}
  .rc-vmeta p{font-size:.85rem;color:var(--lightgray);margin:0}
  .rc-steps{display:flex;flex-direction:column;gap:16px;margin-bottom:28px}
  .rc-step{background:var(--offwhite);border-radius:14px;padding:22px 26px;border:1px solid var(--lightgray);display:flex;gap:18px;align-items:flex-start;transition:box-shadow .2s}
  .rc-step:hover{box-shadow:0 4px 16px rgba(13,13,11,.08)}
  .rc-sbadge{width:38px;height:38px;border-radius:10px;background:var(--offblack);color:var(--yellow);font-weight:800;font-size:15px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
  .rc-step h3{font-size:.98rem;font-weight:700;margin-bottom:5px;color:var(--offblack)}
  .rc-step p{font-size:.87rem;color:var(--gray);line-height:1.6;margin:0}
  .rc-subhead{font-size:1rem;font-weight:700;margin-bottom:16px;color:var(--offblack)}
  .rc-2col{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:26px}
  .rc-opt{background:var(--offwhite);border:1px solid var(--lightgray);border-radius:14px;padding:18px;transition:border-color .2s,box-shadow .2s}
  .rc-opt:hover{border-color:var(--yellow);box-shadow:0 2px 12px rgba(255,215,6,.2)}
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
  .rc-cb{width:22px;height:22px;border-radius:6px;border:2px solid var(--lightgray);flex-shrink:0;margin-top:1px;background:white;display:flex;align-items:center;justify-content:center;font-size:12px;color:var(--gray)}
  .rc-clab{font-size:.88rem;color:var(--darkgray);line-height:1.4}
  .rc-clab span{display:block;font-size:.78rem;color:var(--gray);margin-top:2px}
  .rc-sec-nav{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-top:24px;flex-wrap:wrap}
  .rc-btn-prev,.rc-btn-next,.rc-btn-disabled{display:inline-flex;align-items:center;justify-content:center;padding:11px 18px;border-radius:10px;font-weight:700;font-size:.88rem;text-decoration:none;border:1px solid var(--lightgray)}
  .rc-btn-prev{background:white;color:var(--darkgray)}
  .rc-btn-next{background:var(--yellow);color:var(--offblack);border-color:var(--yellow)}
  .rc-link-btn{display:inline-flex;align-items:center;gap:8px;background:var(--yellow);color:var(--offblack);text-decoration:none;padding:11px 22px;border-radius:10px;font-weight:700;font-size:.88rem;transition:opacity .2s;margin-bottom:8px;margin-right:8px}
  .rc-link-btn:hover{opacity:.85;text-decoration:none}
  .rc-link-sec{background:var(--offwhite);color:var(--darkgray);border:1px solid var(--lightgray)}
  .rc-link-sec:hover{background:var(--brightgray)}
  @media(max-width:640px){.rc-hero h1{font-size:1.7rem}.rc-2col{grid-template-columns:1fr}.rc-hero-stats{gap:20px}.rc-sec-header{flex-direction:column;gap:12px}.rc-hero{padding:36px 20px 32px}.rc-video-card{flex-direction:column;padding:24px}.rc-nav{flex-direction:column}.rc-sec-nav{flex-direction:column;align-items:stretch}}
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
    <a class="rc-active" href="https://docs.recurly.com/recurly-commerce/docs/navigate-subscription-plans"><span class="rc-snum">2</span>Subscription Plans</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-storefront-setup"><span class="rc-snum">3</span>Storefront Setup</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-customer-portal"><span class="rc-snum">4</span>Customer Portal</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-notifications-commerce"><span class="rc-snum">5</span>Notifications</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-integrations-commerce"><span class="rc-snum">6</span>Integrations</a>
    <a href="https://docs.recurly.com/recurly-commerce/docs/navigate-launch-commerce"><span class="rc-snum">✓</span>Launch!</a>
  </nav>

  <div class="rc-container">
    <div class="rc-sec">
      <div class="rc-sec-header">
        <div class="rc-sec-icon">🏷️</div>
        <div>
          <h2>Step 1: Create Your Subscription Plans</h2>
          <p>Your subscription plan defines <em>what</em> customers subscribe to, <em>how often</em> they're billed, and <em>what discounts</em> apply. This is the foundation everything else is built on.</p>
        </div>
      </div>

      <div class="rc-video-card" style="padding: 0; overflow: hidden; height: 480px;">
        <iframe 
          src="https://drive.google.com/file/d/1WzuHBw53KIPXWd2OlqYGM-qR61RIBAiyD3F5uSivW4g/preview" 
          width="100%" 
          height="100%" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
        </iframe>
      </div>
      <div class="rc-steps">
        <div class="rc-step"><div class="rc-sbadge">1</div><div><h3>Open Recurly Commerce → Subscription Plans</h3><p>In your Shopify admin, open the Recurly Commerce app and navigate to <strong>Subscription Plans</strong>. Click <strong>+ Create Offer</strong> in the top-right corner to get started.</p></div></div>
        <div class="rc-step"><div class="rc-sbadge">2</div><div><h3>Select Your Products</h3><p>Choose which Shopify products (SKUs) will be available as subscriptions. Your Shopify catalog must already be synced, and each product can only be assigned to one plan at a time.</p></div></div>
        <div class="rc-step"><div class="rc-sbadge">3</div><div><h3>Set Billing Frequency Options</h3><p>Click <strong>+ Add Option</strong> to define delivery frequencies (e.g., every 1 month, every 2 months). Offer multiple frequencies so customers can choose what fits their lifestyle.</p></div></div>
        <div class="rc-step"><div class="rc-sbadge">4</div><div><h3>Configure Discounts</h3><p>Assign a discount percentage to each frequency tier. Larger discounts for more frequent orders incentivize subscriptions and improve retention.</p></div></div>
        <div class="rc-step"><div class="rc-sbadge">5</div><div><h3>Configure Advanced Options (Optional)</h3><p>Enable gift subscriptions, product swaps, one-time add-ons, free trials, prepaid plans, or term commitments. These can be added now or anytime later.</p></div></div>
        <div class="rc-step"><div class="rc-sbadge">6</div><div><h3>Publish Your Offer</h3><p>When satisfied with your setup, click <strong>Publish Offer</strong> in the top-right. Your subscription plan is now live on the product pages you configured. 🎉</p></div></div>
      </div>

      <h3 class="rc-subhead">📐 Subscription Plan Types — What to Offer</h3>
      <div class="rc-2col">
        <div class="rc-opt"><div class="rc-oicon">🔄</div><h4>Recurring (Subscribe & Save)</h4><p>The classic model. Customers receive products on a set schedule and save a percentage vs. one-time purchase. Great for consumables and everyday essentials.</p><span class="rc-tag">Most Common</span></div>
        <div class="rc-opt"><div class="rc-oicon">💳</div><h4>Prepaid Plans</h4><p>Customers pay upfront for multiple deliveries (e.g., 3-month bundle). Great for gift subscriptions and improving cash flow from day one.</p><span class="rc-tag">Higher AOV</span></div>
        <div class="rc-opt"><div class="rc-oicon">🎁</div><h4>Gift Subscriptions</h4><p>Let customers send subscriptions as gifts. Toggle the "Add gift option" setting when creating your plan to enable the gift flag at checkout.</p><span class="rc-tag">Boosts Acquisition</span></div>
        <div class="rc-opt"><div class="rc-oicon">🆓</div><h4>Free Trials</h4><p>Let customers try before they commit. Trial ending reminder emails are sent automatically 3 days before the trial ends.</p><span class="rc-tag">Reduces Friction</span></div>
      </div>

      <div class="rc-tip">
        <span class="rc-tipicon">💡</span>
        <div><h4>Pro Tip · Discount Strategy</h4><p>Offering a slightly larger discount for your most frequent delivery option (e.g., 15% off monthly vs. 10% off every 2 months) pushes customers toward higher order frequency — which means more predictable revenue and better LTV for you.</p></div>
      </div>

      <div class="rc-checklist">
        <div class="rc-cl-header"><span>✅</span><h3>Step 1 Checklist</h3></div>
        <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Shopify catalog is synced with Recurly Commerce<span>Confirm products appear when creating an offer</span></div></div>
        <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">At least one subscription plan created and published<span>Check for green "Published" status</span></div></div>
        <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Delivery frequencies and discounts configured<span>At least 1-2 frequency options per plan</span></div></div>
        <div class="rc-cli"><div class="rc-cb">✓</div><div class="rc-clab">Advanced options reviewed (gifts, trials, add-ons)<span>Enable what's relevant to your business</span></div></div>
      </div>

      <div class="rc-sec-nav">
        <a class="rc-btn-prev" href="https://docs.recurly.com/recurly-commerce/docs/navigate-intro-to-commerce">← Intro</a>
        <a class="rc-btn-next" href="https://docs.recurly.com/recurly-commerce/docs/navigate-storefront-setup">Next: Storefront Setup →</a>
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
