
<svelte:head>
	<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet" />
</svelte:head>


<div class="thin-centered">
	<nav class="navbar">
		<div class="navbar-left">:)</div>
		<div class="navbar-right">
			<a href="/essays" class="nav-link">mini(essays)</a>
			<a href="/socials" class="nav-link">socials</a>
			<!-- <a href="javascript:void(0)" class="nav-link">placeholder</a> -->
		</div>
	</nav>
		<main style="margin-top:2.5rem;">
			<h1>YO — ADIT HERE :D</h1>
						<p>i'm an army 
							<span class="tooltip-underline">
								brat
								<span class="tooltip-box">
									<span style="font-weight:700;">brat</span> (abbreviation)<br/>
									<span style="color:#888;">/bræt/</span><br/>
									born, raised, and transferred
								</span>
							</span>,
							who has spent my childhood in 9 different schools in 7 cities all over india. currently, i'm an undergrad at <a href="https://youtu.be/MShbP3OpASA?si=2S4O7T4Cwfd9VN0g&t=2997" target="_blank">aalto</a> in finland.
						</p>

                        <br/><br/>

                        <p><b>RANDOM COOL STUFF</b></p>
                        <ul>
                            <li>- waited 25 min in the parking to meet andrew ng at <a href="https://events.ycombinator.com/ai-sus" target="_blank">yc ai sus</a>.</li>
                            <li>- presented compling research at nml workshop @ neurips'23.</li>
                            <li>- finalist at national science fair (top 1% of 10,000+).</li>
                            <li>- attended <a href="https://linguistics.osu.edu/undergrad/sliys" target="_blank">linguistics camp</a> at ohio state on $1100 scholly.</li>
                            <li>- opened a lemonade stand when i was 9 and somehow made a loss.</li>
                        </ul>

                        <br/><br/>

                        <p><b>CURRENTLY WORKING ON</b></p>
                        <ul>
                            <li>- <a href="https://paebbl.com" target="_blank">paebbl.com</a>: building bedrock kbs, mcp servers, and ai agents.</li>
                            <li>- <a href="https://aaltoes.com" target="_blank">aaltoes.com</a>: organising hackathons and pushing build culture.</li>
                            <li>- <a href="https://burrow.wtf" target="_blank">burrow.wtf</a>: fun game to go down rabbit holes.</li>
                            <li>- <a href="https://getnabla.xyz" target="_blank">getnabla.xyz</a>: finding aliens faster than ever.</li>
                            <li>- <a href="https://aalto.fi/en" target="_blank">aalto.fi</a>: bs data science + quantum tech.</li>   
                        </ul>

                    </main>
</div>

<style>
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
	:global(html), :global(body) {
		font-family: 'JetBrains Mono', monospace;
		font-size: 14px;
		margin: 0;
		padding: 0;
		background: #fff;
	}
	h1 {
		font-size: 20px;
		font-weight: 700;
		margin: 1.5rem 0 1rem 0;
		font-family: 'JetBrains Mono', monospace;
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
	.tooltip-underline:hover {
		border-bottom: 1px solid #222;
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
