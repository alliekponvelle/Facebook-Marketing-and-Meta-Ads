<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Facebook Marketing and Meta Ads</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700&family=Manrope:wght@400;500;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --panel: rgba(248, 239, 221, 0.96);
      --panel-soft: rgba(255, 248, 234, 0.86);
      --text: #2e1a40;
      --muted: #66507b;
      --purple: #71419b;
      --purple-deep: #29123f;
      --gold: #d7b15c;
      --red: #b43b4d;
      --green: #368856;
      --line: rgba(113, 65, 155, 0.15);
      --shadow: 0 24px 60px rgba(8, 2, 15, 0.35);
      --radius: 28px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: "Manrope", sans-serif;
      background:
        radial-gradient(circle at top left, rgba(215, 177, 92, 0.12), transparent 22%),
        radial-gradient(circle at 85% 15%, rgba(113, 65, 155, 0.24), transparent 24%),
        linear-gradient(160deg, #0f0618 0%, #1c0c2c 38%, #30124b 72%, #12081d 100%);
      color: #f9f0dc;
      line-height: 1.6;
      min-height: 100vh;
    }

    .page {
      width: min(1180px, calc(100% - 32px));
      margin: 0 auto;
      padding: 28px 0 56px;
    }

    .hero {
      position: relative;
      overflow: hidden;
      padding: 56px 42px;
      border-radius: 0 0 34px 34px;
      background: linear-gradient(140deg, #160920 0%, #341552 34%, #71419b 70%, #d7b15c 100%);
      box-shadow: var(--shadow);
      isolation: isolate;
    }

    .hero::before,
    .hero::after {
      content: "";
      position: absolute;
      border-radius: 50%;
      background: rgba(255,255,255,0.08);
      filter: blur(2px);
      z-index: -1;
    }

    .hero::before {
      width: 260px;
      height: 260px;
      top: -100px;
      right: -60px;
    }

    .hero::after {
      width: 180px;
      height: 180px;
      bottom: -60px;
      left: 10px;
    }

    .eyebrow,
    .section-label,
    .pill {
      display: inline-flex;
      align-items: center;
      padding: 7px 14px;
      border-radius: 999px;
      font-size: 11px;
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .eyebrow {
      background: rgba(255,255,255,0.14);
      border: 1px solid rgba(255,255,255,0.22);
      color: #fff5dd;
    }

    .section-label {
      background: rgba(215, 177, 92, 0.16);
      color: var(--purple);
      margin-bottom: 14px;
    }

    .pill {
      background: rgba(113, 65, 155, 0.1);
      color: var(--purple-deep);
      margin: 0 6px 8px 0;
      letter-spacing: 0.08em;
    }

    h1, h2, h3 {
      margin: 0;
      font-family: "Cinzel", serif;
      font-weight: 700;
      letter-spacing: 0.02em;
    }

    h1 {
      margin-top: 18px;
      font-size: clamp(2.6rem, 7vw, 5rem);
      line-height: 0.96;
      max-width: 12ch;
    }

    .hero p {
      max-width: 74ch;
      margin: 18px 0 0;
      font-size: 1.04rem;
      color: rgba(255, 248, 235, 0.92);
    }

    .hero-grid,
    .grid-2,
    .grid-3,
    .grid-4 {
      display: grid;
      gap: 16px;
      margin-top: 18px;
    }

    .hero-grid {
      grid-template-columns: repeat(4, minmax(0, 1fr));
      margin-top: 28px;
    }

    .grid-2 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    .grid-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
    .grid-4 { grid-template-columns: repeat(4, minmax(0, 1fr)); }

    .hero-stat {
      padding: 16px;
      border-radius: 18px;
      background: rgba(255,255,255,0.12);
      border: 1px solid rgba(255,255,255,0.16);
      backdrop-filter: blur(8px);
    }

    .hero-stat strong {
      display: block;
      font-size: 1.2rem;
      margin-bottom: 4px;
      color: #fff5dd;
    }

    .section,
    .cta {
      margin-top: 18px;
      padding: 28px;
      background: var(--panel);
      color: var(--text);
      box-shadow: var(--shadow);
      border-radius: var(--radius);
      border: 1px solid rgba(255,255,255,0.28);
    }

    .section h2 {
      font-size: clamp(1.8rem, 4vw, 2.7rem);
      line-height: 1.02;
      margin-bottom: 12px;
    }

    .section p {
      margin: 0 0 14px;
      color: var(--muted);
    }

    .card,
    .lesson-card,
    .template-card,
    .warning-card {
      background: var(--panel-soft);
      border: 1px solid var(--line);
      border-radius: 22px;
      padding: 18px;
    }

    .lesson-card { border-top: 4px solid var(--purple); }
    .warning-card { border-top: 4px solid var(--red); }
    .template-card { border-top: 4px solid var(--green); }

    .card h3,
    .lesson-card h3,
    .template-card h3,
    .warning-card h3 {
      font-size: 1.08rem;
      color: var(--purple-deep);
      margin-bottom: 8px;
    }

    ul,
    ol {
      margin: 0;
      padding-left: 20px;
      color: var(--muted);
    }

    li { margin-bottom: 8px; }

    code,
    pre {
      font-family: Consolas, "Courier New", monospace;
    }

    pre {
      white-space: pre-wrap;
      margin: 12px 0 0;
      padding: 14px;
      border-radius: 16px;
      background: rgba(41, 18, 63, 0.08);
      border: 1px solid rgba(113, 65, 155, 0.12);
      color: var(--purple-deep);
      font-weight: 700;
    }

    a {
      color: var(--purple-deep);
      font-weight: 800;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 18px;
      overflow: hidden;
      border-radius: 18px;
      background: rgba(255, 248, 234, 0.72);
    }

    th,
    td {
      padding: 13px 14px;
      text-align: left;
      border-bottom: 1px solid var(--line);
      vertical-align: top;
      color: var(--muted);
      font-size: 0.95rem;
    }

    th {
      color: var(--purple-deep);
      background: rgba(215, 177, 92, 0.18);
      font-weight: 800;
    }

    tr:last-child td { border-bottom: 0; }

    .quote {
      padding: 18px;
      margin-top: 18px;
      border-radius: 22px;
      background: linear-gradient(135deg, rgba(215, 177, 92, 0.18), rgba(113, 65, 155, 0.08));
      border: 1px solid rgba(215, 177, 92, 0.22);
      color: var(--purple-deep);
      font-weight: 700;
    }

    .cta {
      text-align: center;
      background: linear-gradient(135deg, rgba(41, 18, 63, 0.98), rgba(113, 65, 155, 0.92));
      color: #fff4de;
    }

    .cta h2 {
      font-size: clamp(1.9rem, 4vw, 3rem);
      margin-bottom: 12px;
    }

    .cta p {
      max-width: 66ch;
      margin: 0 auto;
      color: rgba(255, 243, 221, 0.88);
    }

    @media (max-width: 980px) {
      .hero-grid,
      .grid-2,
      .grid-3,
      .grid-4 {
        grid-template-columns: 1fr;
      }

      table,
      thead,
      tbody,
      th,
      td,
      tr {
        display: block;
      }

      th { display: none; }

      td {
        border-bottom: 0;
        padding: 10px 14px;
      }

      tr {
        border-bottom: 1px solid var(--line);
        padding: 8px 0;
      }
    }

    @media (max-width: 640px) {
      .page {
        width: min(100% - 16px, 1180px);
      }

      .hero,
      .section,
      .cta {
        padding: 22px;
      }
    }
  </style>
</head>
<body>
  <div class="page">
    <section class="hero">
      <span class="eyebrow">Module 6</span>
      <h1>Facebook Marketing and Meta Ads</h1>
      <p>Learn how to use Facebook Pages, groups, organic content, Meta Business Suite, and beginner ad testing to grow attention, collect leads, and promote digital offers without wasting money.</p>
      <div class="hero-grid">
        <div class="hero-stat">
          <strong>Set Up</strong>
          <span>Create a clean Facebook business presence before running traffic</span>
        </div>
        <div class="hero-stat">
          <strong>Connect</strong>
          <span>Use posts, groups, comments, and conversations to warm up your audience</span>
        </div>
        <div class="hero-stat">
          <strong>Test</strong>
          <span>Run small ad tests with clear objectives, audiences, and creative</span>
        </div>
        <div class="hero-stat">
          <strong>Read Data</strong>
          <span>Use ad results to decide what to stop, adjust, or scale</span>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-label">Why It Matters</div>
      <h2>Facebook Still Moves Buyers</h2>
      <p>Facebook can work for digital sellers because it combines content, communities, retargeting, lead generation, and paid traffic. Students do not need to master everything at once. They need a clean setup, a focused offer, and a simple testing process.</p>
      <div class="quote">The goal is not to throw money at ads. The goal is to test small, learn fast, and only scale what shows signs of working.</div>
    </section>

    <section class="section">
      <div class="section-label">Module Promise</div>
      <h2>What Students Will Learn</h2>
      <div class="grid-3">
        <div class="card">
          <h3>Facebook Foundation</h3>
          <p>Students learn how Pages, profiles, groups, Meta Business Suite, and Ads Manager fit together.</p>
        </div>
        <div class="card">
          <h3>Organic Marketing</h3>
          <p>Students learn how to use posts, comments, groups, and content value before paying for ads.</p>
        </div>
        <div class="card">
          <h3>Business Page Setup</h3>
          <p>Students learn how to set up a Page that looks trustworthy and points people to the right offer.</p>
        </div>
        <div class="card">
          <h3>Ad Campaign Basics</h3>
          <p>Students learn campaign, ad set, ad, objective, budget, placement, audience, and creative basics.</p>
        </div>
        <div class="card">
          <h3>Audience Testing</h3>
          <p>Students learn how to test warm, interest-based, broad, and retargeting audiences.</p>
        </div>
        <div class="card">
          <h3>Reading Results</h3>
          <p>Students learn which metrics matter and how to decide whether to stop, adjust, or keep testing.</p>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-label">Lesson Plan</div>
      <h2>Full Module Outline</h2>
      <div class="grid-2">
        <div class="lesson-card">
          <span class="pill">Lesson 1</span>
          <h3>Facebook Marketing Basics</h3>
          <p>Facebook marketing includes more than paid ads. Students can use a business Page, personal profile, Facebook groups, posts, Reels, comments, DMs, and ads to create trust and send people toward an offer.</p>
          <p>Beginners should think of Facebook as a relationship and traffic platform. Organic content warms people up. Ads help test and amplify the message once the offer is clear.</p>
          <ul>
            <li>Page: public home for a business, brand, creator, or offer.</li>
            <li>Profile: personal identity and relationship-building space.</li>
            <li>Group: community or niche conversation space.</li>
            <li>Meta Business Suite: manage business activity and connected accounts.</li>
            <li>Ads Manager: build campaigns, ad sets, ads, budgets, and reporting.</li>
          </ul>
          <div class="quote">Student task: choose one Facebook goal: collect leads, send traffic, get messages, sell a product, or build authority.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 2</span>
          <h3>Create a Facebook Business Page</h3>
          <p>A Page gives students a public business presence. Meta describes Pages as spaces for businesses, brands, organizations, and public figures to share updates and connect with people.</p>
          <p>The Page should make the business easy to understand in seconds. Students do not need a complicated brand. They need clarity.</p>
          <ul>
            <li>Page name that matches the creator brand or offer.</li>
            <li>Category that fits the business.</li>
            <li>Short bio explaining who the Page helps.</li>
            <li>Profile photo and cover image.</li>
            <li>Action button pointing to the store, lead magnet, message, or booking link.</li>
            <li>Connected Instagram account if they use Instagram too.</li>
          </ul>
          <div class="quote">Page bio formula: I help [audience] [result] with [content/product/service].</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 3</span>
          <h3>Organic Facebook Content</h3>
          <p>Organic content helps students warm up the audience before asking for a sale. It also gives them free testing data about which topics people care about.</p>
          <ul>
            <li>Educational posts: teach one useful step.</li>
            <li>Story posts: share a lesson, mistake, or behind-the-scenes moment.</li>
            <li>Proof posts: share real wins, testimonials, or progress with permission.</li>
            <li>Offer posts: invite people to download, buy, book, or message.</li>
            <li>Conversation posts: ask a simple question related to the niche.</li>
            <li>Reels: repurpose short-form video content from TikTok or Instagram.</li>
          </ul>
          <div class="quote">Content rhythm: 3 value posts, 1 story/proof post, and 1 offer post each week.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 4</span>
          <h3>Facebook Groups and Promo Groups</h3>
          <p>Groups can help students find conversations around their niche, but they should not spam links. The strongest group strategy is to be useful first and promote only where the rules allow it.</p>
          <ul>
            <li>Read group rules before posting.</li>
            <li>Answer questions before dropping links.</li>
            <li>Use value posts to build trust.</li>
            <li>Only promote on promo days or allowed threads.</li>
            <li>Track which groups send clicks, leads, or buyers.</li>
            <li>Leave groups that are only spam and no buyers.</li>
          </ul>
          <div class="quote">Group comment formula: answer the question, give one useful tip, then invite them to message you or check your profile only if allowed.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 5</span>
          <h3>Meta Ads Manager Basics</h3>
          <p>Meta Ads Manager uses three levels: campaign, ad set, and ad. The campaign holds the objective. The ad set controls audience, budget, schedule, and placements. The ad contains the creative, copy, link, and call-to-action.</p>
          <ul>
            <li>Campaign: choose the goal.</li>
            <li>Ad set: choose audience, budget, schedule, placements, and optimization.</li>
            <li>Ad: choose image/video, headline, primary text, link, and CTA.</li>
            <li>Start simple before building complex structures.</li>
            <li>Name campaigns clearly so students can understand reports later.</li>
          </ul>
          <div class="quote">Simple naming example: Leads - Free Checklist - AI Creators - April 2026.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 6</span>
          <h3>Choosing the Right Ad Objective</h3>
          <p>Meta says advertisers should choose the objective that best supports their business goal. The objective tells the ad system what result to look for.</p>
          <ul>
            <li>Awareness: show the brand or message to more people.</li>
            <li>Traffic: send people to a website, store, landing page, or link.</li>
            <li>Engagement: get post engagement, video views, messages, or other interactions.</li>
            <li>Leads: collect contact information or get people into a lead funnel.</li>
            <li>Sales: optimize for purchases or conversion events when tracking is set up.</li>
            <li>Choose the objective based on the next action, not just the cheapest click.</li>
          </ul>
          <div class="quote">Beginner shortcut: use Leads for lead magnets, Traffic for store visits, Engagement for warming content, and Sales only when purchase tracking is ready.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 7</span>
          <h3>Audience Targeting Basics</h3>
          <p>Students should test audiences instead of guessing once and giving up. A strong offer can fail if it is shown to the wrong people.</p>
          <ul>
            <li>Warm audience: people who already know you, visited your page, engaged, clicked, or subscribed.</li>
            <li>Interest audience: people connected to topics, tools, brands, or behaviors related to the niche.</li>
            <li>Broad audience: Meta has more room to find people, especially when the creative is clear.</li>
            <li>Retargeting: show ads to people who interacted but did not take the next step.</li>
            <li>Avoid stacking too many interests at once because it makes the test harder to understand.</li>
          </ul>
          <div class="quote">Student task: create three audience ideas for one offer: warm, interest-based, and broad.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 8</span>
          <h3>The $5/Day Testing Strategy</h3>
          <p>A small daily budget helps students learn without risking too much. The goal is not instant profit. The goal is to test the offer, audience, creative, and landing page.</p>
          <ul>
            <li>Pick one offer or lead magnet.</li>
            <li>Pick one campaign objective.</li>
            <li>Test one audience at a time or use a simple structure with clear naming.</li>
            <li>Use 2 to 3 creatives if budget allows.</li>
            <li>Run for at least 3 days before judging too quickly, unless something is clearly broken.</li>
            <li>Track cost per result, clicks, landing page activity, and conversions.</li>
          </ul>
          <div class="quote">Simple test: $5/day for 3 to 5 days, one offer, one clear CTA, one result you are watching.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 9</span>
          <h3>Ad Creative That Gets Attention</h3>
          <p>The creative should make the right person stop and understand the offer quickly. A beautiful ad that does not communicate the problem will not perform.</p>
          <ul>
            <li>Hook: name the problem or desired result.</li>
            <li>Visual: show the product, result, face, screen recording, or simple graphic.</li>
            <li>Proof: use real proof only, with permission and accurate context.</li>
            <li>CTA: tell people exactly what to do next.</li>
            <li>Match the ad message to the landing page message.</li>
            <li>Test direct, story-based, and problem-solution angles.</li>
          </ul>
          <div class="quote">Ad formula: problem, quick value, offer, call-to-action.</div>
        </div>

        <div class="lesson-card">
          <span class="pill">Lesson 10</span>
          <h3>Reading Results and Making Decisions</h3>
          <p>Students need to know what the numbers are telling them. Do not scale emotion. Scale evidence.</p>
          <ul>
            <li>CPM: cost to reach 1,000 impressions.</li>
            <li>CTR: how many people clicked compared to how many saw the ad.</li>
            <li>CPC: cost per click.</li>
            <li>Cost per lead: cost to get a subscriber or form completion.</li>
            <li>Cost per purchase: cost to get a buyer.</li>
            <li>Conversion rate: percentage of visitors who take the desired action.</li>
            <li>Stop, adjust, or scale based on the goal and cost per result.</li>
          </ul>
          <div class="quote">Decision rule: if people are not clicking, fix the creative or audience. If people click but do not convert, fix the landing page, offer, price, or checkout path.</div>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-label">Campaign Builder</div>
      <h2>Simple Beginner Campaign Map</h2>
      <table>
        <thead>
          <tr>
            <th>Goal</th>
            <th>Suggested Objective</th>
            <th>Best Next Step</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Grow brand awareness</td>
            <td>Awareness</td>
            <td>Send people to follow, watch, or remember the brand.</td>
          </tr>
          <tr>
            <td>Send traffic to a store or lead magnet</td>
            <td>Traffic</td>
            <td>Make sure the page loads fast and matches the ad promise.</td>
          </tr>
          <tr>
            <td>Get comments, messages, or video views</td>
            <td>Engagement</td>
            <td>Use conversation-based content or a strong short-form video.</td>
          </tr>
          <tr>
            <td>Collect emails</td>
            <td>Leads</td>
            <td>Use one clear lead magnet and a simple opt-in page or lead form.</td>
          </tr>
          <tr>
            <td>Drive purchases</td>
            <td>Sales</td>
            <td>Use this when the offer, checkout, and conversion tracking are ready.</td>
          </tr>
        </tbody>
      </table>
    </section>

    <section class="section">
      <div class="section-label">Templates</div>
      <h2>Copy and Paste Swipe File</h2>
      <div class="grid-2">
        <div class="template-card">
          <h3>Facebook Page Bio</h3>
          <pre>I help [audience] [result] with [digital products / creator tools / coaching / AI resources]. Start here: [link]</pre>
        </div>
        <div class="template-card">
          <h3>Group Value Comment</h3>
          <pre>One thing that helps is [quick tip]. The biggest mistake is usually [mistake]. If you want the full checklist, I have it linked on my profile.</pre>
        </div>
        <div class="template-card">
          <h3>Lead Magnet Ad Copy</h3>
          <pre>Struggling with [problem]? I made a free [resource] that shows you how to [specific result]. Grab it here: [link]</pre>
        </div>
        <div class="template-card">
          <h3>Digital Product Ad Copy</h3>
          <pre>If you are trying to [goal], this [guide/template/system] helps you [result]. Inside, you get [benefit 1], [benefit 2], and [benefit 3]. Get it here: [link]</pre>
        </div>
        <div class="template-card">
          <h3>Retargeting Ad Copy</h3>
          <pre>Still thinking about [offer]? If [problem] is what has been slowing you down, this resource gives you the next steps in one place.</pre>
        </div>
        <div class="template-card">
          <h3>Ad Testing Notes</h3>
          <pre>Campaign:
Objective:
Audience:
Creative:
Budget:
Start date:
Result watched:
What worked:
What to test next:</pre>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-label">Checklists</div>
      <h2>Student Downloads to Include</h2>
      <div class="grid-2">
        <div class="template-card">
          <h3>Before Running Ads Checklist</h3>
          <ol>
            <li>Facebook Page is set up with profile image, cover, bio, and action button.</li>
            <li>Offer or lead magnet is clear.</li>
            <li>Landing page, store page, or lead form is working.</li>
            <li>Checkout or opt-in path has been tested.</li>
            <li>Refund, disclosure, or compliance wording is included when needed.</li>
            <li>Audience idea is written down.</li>
            <li>Ad creative and copy match the landing page.</li>
            <li>Budget and testing window are clear.</li>
          </ol>
        </div>
        <div class="template-card">
          <h3>$5/Day Test Checklist</h3>
          <ol>
            <li>Choose one offer.</li>
            <li>Choose one objective.</li>
            <li>Choose one audience test.</li>
            <li>Create 1 to 3 ad creatives.</li>
            <li>Set budget to $5/day.</li>
            <li>Let the test run long enough to collect data.</li>
            <li>Check clicks, cost per result, and conversion behavior.</li>
            <li>Change one thing at a time before retesting.</li>
          </ol>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-label">Common Mistakes</div>
      <h2>What Students Should Avoid</h2>
      <div class="grid-3">
        <div class="warning-card">
          <h3>Running Ads Too Soon</h3>
          <p>Do not run traffic to an unclear offer, broken checkout, weak landing page, or empty Page.</p>
        </div>
        <div class="warning-card">
          <h3>Choosing the Wrong Objective</h3>
          <p>If the goal is leads, choose a lead-focused setup. If the goal is purchases, make sure sales tracking is ready.</p>
        </div>
        <div class="warning-card">
          <h3>Testing Too Much at Once</h3>
          <p>If audience, creative, offer, price, and page all change at the same time, students will not know what caused the result.</p>
        </div>
        <div class="warning-card">
          <h3>Ignoring Organic Feedback</h3>
          <p>Organic comments and questions can reveal the best hooks, objections, and ad angles.</p>
        </div>
        <div class="warning-card">
          <h3>Using Risky Claims</h3>
          <p>Do not promise guaranteed income, fake results, or misleading testimonials in ad copy.</p>
        </div>
        <div class="warning-card">
          <h3>Scaling Too Fast</h3>
          <p>Do not increase budget just because one day looked good. Look for stable results over time.</p>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-label">Knowledge Check</div>
      <h2>Quick Student Quiz</h2>
      <div class="grid-2">
        <div class="card">
          <h3>Question 1</h3>
          <p>What are the three levels inside Meta Ads Manager?</p>
          <div class="quote">Answer: Campaign, ad set, and ad.</div>
        </div>
        <div class="card">
          <h3>Question 2</h3>
          <p>What should students choose first before building a campaign?</p>
          <div class="quote">Answer: The business goal or objective, such as leads, traffic, engagement, awareness, or sales.</div>
        </div>
        <div class="card">
          <h3>Question 3</h3>
          <p>If people click the ad but do not opt in or buy, what should students check?</p>
          <div class="quote">Answer: Landing page, offer clarity, price, checkout path, load speed, and message match.</div>
        </div>
        <div class="card">
          <h3>Question 4</h3>
          <p>Should students spam promo groups with links?</p>
          <div class="quote">Answer: No. Read group rules, give value, and only promote where promotion is allowed.</div>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-label">Sources</div>
      <h2>Research Links</h2>
      <p>Use these as platform references when recording walkthroughs or updating student resources.</p>
      <ul>
        <li><a href="https://www.facebook.com/help/614916958524168">Facebook Help Center: Create a Page</a></li>
        <li><a href="https://www.facebook.com/business/pages/manage">Meta for Business: Manage Your Facebook Page</a></li>
        <li><a href="https://www.facebook.com/help/messenger-app/621956575422138/">Meta Help Center: Create Ad Campaigns in Ads Manager</a></li>
        <li><a href="https://www.facebook.com/business/ads/ad-objectives">Meta for Business: Ad Objectives</a></li>
        <li><a href="https://www.facebookblueprint.com/student/path/211543-meta-advertising-course">Meta Blueprint: Get Started With Advertising on Facebook and Instagram</a></li>
        <li><a href="https://www.facebookblueprint.com/student/catalog">Meta Blueprint Learning Catalog</a></li>
        <li><a href="https://www.ftc.gov/business-guidance/advertising-marketing">FTC Advertising and Marketing Basics</a></li>
        <li><a href="https://www.ftc.gov/business-guidance/resources/disclosures-101-social-media-influencers">FTC Disclosures 101 for Social Media Influencers</a></li>
      </ul>
    </section>

    <section class="cta">
      <h2>Test Small, Learn Fast</h2>
      <p>Facebook and Meta ads work best when the offer is clear, the audience is focused, the creative speaks to a real problem, and each test teaches the next move.</p>
    </section>
  </div>
</body>
</html>
