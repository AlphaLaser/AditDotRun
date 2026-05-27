<script lang="ts">
	import { onMount, onDestroy } from 'svelte';

	// pixel art frames. each char is one pixel.
	//   . = transparent
	//   G = body (green)
	//   D = darker green (shading)
	//   W = white (eye)
	//   K = black (pupil / nostril)
	const COLS = 14;
	const ROWS = 11;

	const FRAMES: string[][] = [
		// frame A — legs spread (mid-stride)
		[
			'..........GGG.',
			'.........GGGGG',
			'.........GWKGG',
			'.........GGGGG',
			'........GGGGGD',
			'.G.....GGGGGGD',
			'GGGGGGGGGGGD..',
			'.GGGGGGGGGD...',
			'...G.....G....',
			'..G.......G...',
			'..G.......G...'
		],
		// frame B — legs together (other mid-stride)
		[
			'..........GGG.',
			'.........GGGGG',
			'.........GWKGG',
			'.........GGGGG',
			'........GGGGGD',
			'.G.....GGGGGGD',
			'GGGGGGGGGGGD..',
			'.GGGGGGGGGD...',
			'...G.....G....',
			'....G...G.....',
			'....G...G.....'
		]
	];

	const COLORS: Record<string, string> = {
		G: '#7AB85A',
		D: '#4F7A35',
		W: '#FFFFFF',
		K: '#1A1A1A'
	};

	type Pixel = { x: number; y: number; fill: string };

	const framePixels: Pixel[][] = FRAMES.map((rows) =>
		rows.flatMap((row, y) =>
			row.split('').flatMap((ch, x) => (ch in COLORS ? [{ x, y, fill: COLORS[ch] }] : []))
		)
	);

	let frameIndex = $state(0);
	let timer: ReturnType<typeof setInterval> | undefined;

	onMount(() => {
		timer = setInterval(() => {
			frameIndex = 1 - frameIndex;
		}, 220);
	});

	onDestroy(() => {
		if (timer) clearInterval(timer);
	});
</script>

<svg
	class="dino-walker"
	aria-hidden="true"
	viewBox="0 0 {COLS} {ROWS}"
	width="28"
	height="22"
	shape-rendering="crispEdges"
	preserveAspectRatio="xMidYMax meet"
>
	{#each framePixels[frameIndex] as p (p.x + ',' + p.y)}
		<rect x={p.x} y={p.y} width="1" height="1" fill={p.fill} />
	{/each}
</svg>

<style>
	.dino-walker {
		position: absolute;
		bottom: -1px;
		left: -32px;
		pointer-events: none;
		user-select: none;
		z-index: 1;
		image-rendering: pixelated;
		image-rendering: crisp-edges;
		will-change: left, transform;
		animation:
			dino-walk 26s linear infinite,
			dino-bob 0.44s steps(2, end) infinite;
	}

	@keyframes dino-walk {
		0% {
			left: -32px;
		}
		100% {
			left: calc(100% + 4px);
		}
	}

	@keyframes dino-bob {
		0% {
			transform: translateY(0);
		}
		50% {
			transform: translateY(-1px);
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.dino-walker {
			animation: none;
			left: 50%;
		}
	}
</style>
