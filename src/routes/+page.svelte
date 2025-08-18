<svelte:head>
	<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet" />
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Crimson+Text:ital,wght@0,400;0,600;0,700;1,400;1,600;1,700&family=Noto+Serif+Dogra&display=swap" rel="stylesheet">

</svelte:head>


<div class="thin-centered">
	<nav class="navbar">
		<div class="navbar-left">
			<a href="/" class="brand-link">
			  adit.run()
			</a>
		</div>
		<div class="navbar-right">
			<!-- <a href="/essays" class="nav-link">home</a> -->
			<a href="/essays" class="nav-link">random(thoughts)</a>
			<a href="/socials" class="nav-link">say(hi)</a>
			<!-- <a href="javascript:void(0)" class="nav-link">placeholder</a> -->
		</div>
	</nav>
		<main style="margin-top:2.5rem;">
			<!-- <h1>YO — ADIT HERE :D</h1> -->
			 <h1>ADIT | आदित <!-- ADD SUPPORT FOR NOTO SANS DOGRA HERE --></h1>
			<p>i’m a 19y/o army 
							<span class="tooltip-underline">
								brat
								<span class="tooltip-box">
									<span style="font-weight:700;">brat</span> (abbreviation)<br/>
									<span style="color:#888;">/bræt/</span><br/>
									born, raised, and transferred
								</span>
							</span>, currently studying at <a href="https://youtu.be/MShbP3OpASA?si=2S4O7T4Cwfd9VN0g&t=2997" target="_blank">aalto</a> in finland, who grew up attending 9 schools in 7 cities across india before graduating from <a href="https://youtu.be/8w8oGfe7TbE" target="_blank">sanskriti school</a>, new delhi.
						</p>

                        <br/><br/>

                        <p><b>STUFF I DID</b></p>
                        <ul>
                            <li>- waited 25 min in the parking to meet andrew ng at <a href="https://events.ycombinator.com/ai-sus" target="_blank">yc ai sus</a>.</li>
                            <li>- presented compling research at nml workshop @ neurips'23.</li>
                            <li>- finalist at national science fair (top 1% of 10,000+).</li>
                            <li>- attended <a href="https://linguistics.osu.edu/undergrad/sliys" target="_blank">linguistics camp</a> at ohio state on $1100 scholly.</li>
                            <li>- nicknamed
								<span class="tooltip-underline">
								कबाड़ी
								<span class="tooltip-box">
									<span style="font-weight:700;">कबाड़ी</span> (kabadi)<br/>
									<span style="color:#888;">/kəˈbɑː.ɽiː/</span><br/>
									scrap dealer
								</span>
							</span>
							at home for hoarding junk to build stuff.</li>
                        </ul>

                        <br/><br/>

                        <p><b>WHAT IM UPTO RN</b></p>
                        <ul>
                            <li>- <a href="https://paebbl.com" target="_blank">paebbl.com</a>: building bedrock kbs, mcp servers, and ai agents.</li>
                            <li>- <a href="https://aaltoes.com" target="_blank">aaltoes.com</a>: organising hackathons and pushing build culture.</li>
                            <li>- <a href="https://burrow.wtf" target="_blank">burrow.wtf</a>: chrome ext to auto login with a temp mail.</li>
                            <li>- <a href="https://kaggle.com" target="_blank">kaggle.com</a>: working on some really fun comps with friends.</li>
                            <li>- <a href="https://aalto.fi/en" target="_blank">aalto.fi</a>: bs data science + quantum tech.</li>   
                        </ul>

						<br/><br/>

						<!-- New light grey text box above previous work section -->
						<div class="custom-text-box">
							<!-- Put your text here -->
							<p>i've been a huge fan of cartoons for as long as i can remember. 
								when i look back, i realise how much i loved it when the 
								characters just built things: <br/><br/>
								- mr. bean and super trolley with a BILLION features. <br/>	
								- phineas and ferb's nanobots. <br/>
								- tom blueprinting the perfect mousetrap. <br/>
								- mr. fox welding the evening away in his workshop. <br/><br/>

								that's the high i've been chasing ever since -- mini hot air balloons, msw logo programs, 

				
								

								
							
							</p>
						</div>

						<br/><br/>

                        <p><b>PREVIOUS WORK</b></p>
                        <ul>
                            <li>- <a href="https://smu.edu.sg" target="_blank">smu.edu.sg</a>: intern @ social nlp lab under dr wei gao.</li>
                            <li>- <a href="#" target="_blank">projectbeta.club</a>: tech/startup club president.</li>
                            <li>- <a href="#" target="_blank">slingshotahead.com</a>: growth/community — 10xed their discord.</li>  
                        </ul>

						<br/><br/>

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
	.brand-link {
		color: #222;
		text-decoration: none;
		cursor: pointer;
	}
	.brand-link:hover {
		color: #222;
		text-decoration: none;
	}
	.custom-text-box {
		background: #f7f7f8;
		border-radius: 0px;
		padding: 1.2rem 1.5rem;
		margin: 0 auto;
		box-sizing: border-box;
		font-size: 14px;
		color: #222;
	}
</style>
