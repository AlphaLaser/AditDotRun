<script>
  import { onMount } from "svelte";

  let song = null;
  let loading = true;
  let error = null;

  onMount(async () => {
    try {
      const res = await fetch(
        "https://lastfm-last-played.biancarosa.com.br/The_AlphaLaser/latest-song"
      );
      if (!res.ok) throw new Error("Failed to fetch song");

      song = await res.json();
    } catch (err) {
      error = err.message;
    } finally {
      loading = false;
    }
  });
</script>

<!--
idk a potential list of things i like??? porbs shouldnt include music 
coz then ts would fet WAY too long (title of your sex tape).




-->

<div class="thin-centered">
	<nav class="navbar">
		<div class="navbar-left">
			<a href="/" class="brand-link">
				adit.run()
			</a>
		</div>
		<div class="navbar-right">
			<!-- <a href="/essays" class="nav-link">home</a> -->
			<a href="/archive" class="nav-link">random(archive)</a>
			<a href="/hi" class="nav-link">say(hi)</a>
			<!-- <a href="javascript:void(0)" class="nav-link">placeholder</a> -->
		</div>
	</nav>

    <!-- <center>
		⚒️ under construction ⚒️
    </center> -->
	<br>YAP: <br>

	0. <a href="/essays/0">f'(x) = 0: optimizing for 'bare minimum'</a> <br>
	
	
<br>
	LAST PLAYED SONG:

{#if loading}
  <p>Loading latest song...</p>
{:else if error}
  <p style="color: red;">Error: {error}</p>
{:else}
  <div class="song">
    <h1>{song.track.name} by {song.track.artist["#text"]}</h1>

  </div>
{/if}
<br>


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
	a {
		color: #2563eb;
		text-decoration: underline;
		text-underline-offset: 2px;
		transition: color 0.2s;
	}
	a:hover {
		color: #1d4ed8;
		text-decoration-thickness: 2px;
	}
	.brand-link {
		color: #222;
		text-decoration: none;
		cursor: pointer;
	}
	.brand-link:hover {
		color: #222;
		text-decoration: none;
	}
	.contact-link {
		color: #2563eb;
		text-decoration: underline;
		text-underline-offset: 2px;
		transition: color 0.2s;
	}
	.contact-link:hover {
		color: #1d4ed8;
		text-decoration-thickness: 2px;
	}
	.tooltip-underline {
		position: relative;
		display: inline-block;
		border-bottom: 1px dashed #888;
		cursor: pointer;
		transition: border-color 0.2s, color 0.2s;
		color: #888;
	}
	.tooltip-underline:hover {
		border-bottom: 1px solid #222;
		color: #222;
	}
	.tooltip-box {
		display: none;
		position: absolute;
		left: 50%;
		top: 120%;
		transform: translateX(-50%);
		min-width: 210px;
		background: #fff;
		color: #222;
		border: 1px solid #e0e0e0;
		border-radius: 8px;
		box-shadow: 0 2px 12px 0 rgba(0,0,0,0.07);
		padding: 0.75rem 1rem;
		font-size: 13px;
		font-family: 'JetBrains Mono', monospace;
		z-index: 100;
		white-space: pre-line;
		pointer-events: none;
	}
	.tooltip-underline:hover .tooltip-box {
		display: block;
		animation: fadeIn 0.18s;
	}
	@keyframes fadeIn {
		from { opacity: 0; transform: translateX(-50%) translateY(10px); }
		to { opacity: 1; transform: translateX(-50%) translateY(0); }
	}
	.lastfm-box {
		background: #f7f7f8;
		border-radius: 10px;
		border: 1px solid #e0e0e0;
		padding: 1rem 1.2rem;
		margin: 0 auto 2rem auto;
		max-width: 350px;
		text-align: center;
	}
	.album-art {
		width: 64px;
		height: 64px;
		object-fit: cover;
		border-radius: 6px;
		margin: 0.5rem 0;
	}
</style>
