---
layout: page
title: Nordic Love Data Week 2027
menu_title: Home
menu_icon: house-door
---

<style>
  .ldw27 { --red: #9a0000; --pink: #eaaab7; --blush: #f7dde3; --muted: #5c5c5c; }

  .ldw27 .hero {
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(0, 1.05fr);
    gap: 2.5rem;
    align-items: center;
    margin-bottom: 2rem;
  }
  .ldw27 .hero img {
    border-radius: 3px;
    transform: rotate(-2deg);
    box-shadow: 0 16px 30px rgba(120, 20, 35, .2);
  }
  .ldw27 .hero h2 {
    font-size: 2.2rem;
    line-height: 1.1;
    margin: 0 0 .25rem;
  }
  .ldw27 .dates {
    font-size: 1.3rem;
    font-weight: 600;
    color: var(--red);
    margin: 0 0 1.1rem;
  }
  .ldw27 .btn-dark { background: var(--red); color: #fff !important; }
  .ldw27 .btn-dark:hover { outline-color: var(--red) !important; }

  .ldw27 .lede { font-size: 1.05rem; margin: 0 0 .6rem; }
  .ldw27 .sub { color: var(--muted); margin: 0 0 1.2rem; }

  .ldw27 .theme {
    background: var(--blush);
    border-top: 5px solid var(--red);
    border-bottom: 5px solid var(--red);
    padding: 2.2rem 1.8rem 2.4rem;
    margin: 2.5rem 0;
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(0, 1.15fr);
    gap: 2.5rem;
    align-items: start;
  }
  .ldw27 .theme__eyebrow {
    display: inline-block;
    background: var(--red);
    color: #fff;
    font-weight: 700;
    font-size: 1rem;
    padding: 6px 15px;
    margin: 0 0 1rem;
  }
  .ldw27 .theme h3 {
    font-size: 2.6rem;
    line-height: 1.04;
    letter-spacing: -.025em;
    color: var(--red);
    margin: 0 0 .5rem;
  }
  .ldw27 .theme__blurb { font-size: 1.1rem; margin: 0; }
  .ldw27 .theme__hint { color: var(--muted); font-size: .95rem; margin: 1rem 0 0; }
  .ldw27 .theme ul { list-style: none; margin: 0; padding: 0; }
  .ldw27 .theme li {
    display: grid;
    grid-template-columns: auto minmax(0, 1fr);
    gap: 1rem;
    align-items: baseline;
    padding: .8rem 0;
    border-top: 1px solid rgba(154, 0, 0, .22);
  }
  .ldw27 .theme li:last-child { border-bottom: 1px solid rgba(154, 0, 0, .22); }
  .ldw27 .theme b { color: var(--red); white-space: nowrap; }

  .ldw27 .notes {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 1.8rem;
    margin-top: 2rem;
  }
  .ldw27 .notes h4 { margin: 0 0 .3rem; font-size: 1.02rem; }
  .ldw27 .notes p { margin: 0; color: var(--muted); font-size: .95rem; }

  @media screen and (max-width: 800px) {
    .ldw27 .hero,
    .ldw27 .theme { grid-template-columns: 1fr; gap: 1.6rem; }
    .ldw27 .hero h2 { font-size: 1.8rem; }
    .ldw27 .theme h3 { font-size: 2rem; }
    .ldw27 .theme { padding: 1.6rem 1.2rem 1.8rem; }
  }
</style>

<div class="ldw27">

  <section class="hero">
    <div>
      <img src="{{ '/assets/Save-the-date-27.png' | relative_url }}"
           alt="Save the date: the next Love Data Week takes place 8 to 12 February 2027.">
    </div>
    <div>
      <h2>We will be back next February.</h2>
      <p class="dates">8&ndash;12 February 2027</p>
      <p class="lede">Nordic Love Data Week is a week of free online sessions on research data, run together by universities across the Nordics.</p>
      <p class="sub">The 2027 programme is being planned now. Sessions will be announced here as they are confirmed.</p>
      <p>
        <a class="btn btn-dark" href="{{ '/2026/' | relative_url }}">See the 2026 week</a>
        <a class="btn" href="https://github.com/{{ site.github_repo }}">Follow on GitHub</a>
      </p>
    </div>
  </section>

  <section class="theme">
    <div>
      <p class="theme__eyebrow">This year's theme</p>
      <h3>Handle with care</h3>
      <p class="theme__blurb">Research data needs looking after. For one week in February, we talk about how.</p>
      <p class="theme__hint">Want to run a session? Get in touch with the <a href="{{ '/about/' | relative_url }}">organising team</a>.</p>
    </div>
    <ul>
      <li><b>Keep it safe</b><span>Security, privacy and the rules that apply to your data</span></li>
      <li><b>Keep it tidy</b><span>Organising and documenting data so others can follow it</span></li>
      <li><b>Plan ahead</b><span>Deciding early where data will live and how long you keep it</span></li>
      <li><b>Use it well</b><span>Sharing and reusing data responsibly, yours and other people's</span></li>
    </ul>
  </section>

  <section class="notes">
    <div>
      <h4>Everything from 2026 is still here</h4>
      <p>The <a href="{{ '/agenda/' | relative_url }}">full agenda</a> and the <a href="{{ '/videos-slides/' | relative_url }}">slides and recordings</a> from last February remain online.</p>
    </div>
    <div>
      <h4>Where's the Data Day</h4>
      <p>The self-run day for research groups <a href="{{ '/where-is-the-data-day/' | relative_url }}">returns in 2027</a>, with a new name to match the theme.</p>
    </div>
    <div>
      <h4>Love Data Week worldwide</h4>
      <p>Hundreds of institutions take part each February. See the <a href="https://www.icpsr.umich.edu/sites/icpsr/about/news-events/international-love-data-week">international listing</a>.</p>
    </div>
  </section>

</div>
