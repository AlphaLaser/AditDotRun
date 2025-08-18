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
    <br/><br/>
	i'll respond fastest on 
	<span class="tooltip-underline">
		discord
		<span class="tooltip-box">
			<!-- <span style="font-weight:700;">discord</span><br/> -->
			<!-- <span style="color:#888;">/ˈdɪs.kɔːrd/</span><br/> -->
			@the_alphalaser
		</span>
	</span>
	but feel free to reach out to me on 
    <a href="mailto:aditmagotra@gmail.com" class="contact-link">email</a>, 
    <a href="https://twitter.com/aditmag" class="contact-link" target="_blank">twitter</a>, 
    <a href="https://www.linkedin.com/in/aditmagotra/" class="contact-link" target="_blank">linkedin</a>, or 
    <a href="https://www.instagram.com/aditmagotra/" class="contact-link" target="_blank">instagram</a>!
<br/><br/>
<!-- <img alt="The project logo" src={image} /> -->
 <img src="/me.jpeg" alt="literally me" />
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
</style>
