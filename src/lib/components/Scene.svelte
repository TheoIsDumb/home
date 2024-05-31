<script>
	import { T } from "@threlte/core";
	import { OrbitControls } from "@threlte/extras";
	import { Sky } from "@threlte/extras";
	import PC from "./pc.svelte";
</script>

<Sky
	elevation={1.45}
	rayleigh={3}
	exposure={0.3}
	turbidity={10}
	azimuth={90}
	intensity={0.2}
/>

<T.PerspectiveCamera makeDefault position={[-25, 10, 55]} fov={70}>
	<OrbitControls
		enableDamping
		autoRotate={true}
		minDistance={40}
		maxDistance={100}
	/>
</T.PerspectiveCamera>

<PC />