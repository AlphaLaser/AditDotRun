<script>
  // Placeholder for essays data
  const essays = [
    {
      title: 'You Only Get One Shot',
      month: 'August 2025',
      summary: 'do not miss a chance to blow.'
    },
    {
      title: 'Air Jordans, Purple Sunbirds, and Nancy Sinatra.',
      month: 'Jan 2024',
      summary: 'my commonapp essay :)'
    }
  ];
  // Group essays by month
  let grouped = {};
  essays.forEach(e => {
    if (!grouped[e.month]) grouped[e.month] = [];
    grouped[e.month].push(e);
  });
</script>

<div class="thin-centered">
  <nav class="navbar">
    <div class="navbar-left">:)</div>
    <div class="navbar-right">
      <a href="/micro-essays" class="nav-link">mini(essays)</a>
      <a href="/socials" class="nav-link">socials</a>
    </div>
  </nav>
  <br/>
  <div class="essays-header">"bro thinks he's paul graham"</div>
  {#each Object.keys(grouped) as month}
    <div class="month-section">
      <div class="month-title">{month}</div>
      {#each grouped[month] as essay}
        <div class="essay-rect">
          <div class="essay-title">{essay.title}</div>
          <div class="essay-summary">{essay.summary}</div>
        </div>
      {/each}
    </div>
  {/each}
</div>

<style>
  .thin-centered {
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
    width: 40vw;
    min-width: 320px;
    max-width: 600px;
    margin: 1.5rem auto 3rem auto;
    padding: 2rem 2vw;
    background: transparent;
    box-sizing: border-box;
  }
  .essays-header {
    font-size: 15px;
    color: #222;
    margin-bottom: 2.5rem;
    text-align: center;
    font-family: 'JetBrains Mono', monospace;
  }
  .month-section {
    margin-bottom: 2.5rem;
  }
  .month-title {
    font-size: 15px;
    color: #888;
    margin-bottom: 1.2rem;
    font-weight: 700;
    font-family: 'JetBrains Mono', monospace;
  }
  .essay-rect {
    background: #fff;
    border: 1px solid #bbb;
    border-radius: 0;
    padding: 1.5rem 1.5rem 1.2rem 1.5rem;
    margin-bottom: 1.2rem;
    box-shadow: none;
  }
  .essay-title {
    font-size: 14px;
    font-weight: 700;
    margin-bottom: 0.5rem;
    font-family: 'JetBrains Mono', monospace;
  }
  /* .essay-by removed */
  .navbar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 0 1.5rem 0;
    box-sizing: border-box;
    font-family: 'JetBrains Mono', monospace;
    background: white;
    z-index: 10;
    border-bottom: 1px solid #eee;
    position: static;
  }
  .navbar-left {
    font-weight: 700;
    letter-spacing: 0.05em;
    color: #222;
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
  }
  .navbar-right {
    display: flex;
    gap: 2rem;
  }
  .nav-link {
    color: #2563eb;
    text-decoration: underline;
    font-size: 14px;
    font-family: 'JetBrains Mono', monospace;
    transition: color 0.2s;
    text-underline-offset: 2px;
  }
  .nav-link:hover {
    color: #1d4ed8;
    text-decoration-thickness: 2px;
  }
  .essay-summary {
    font-size: 14px;
    color: #888;
    font-family: 'JetBrains Mono', monospace;
  }
</style>
