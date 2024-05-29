<script>
	import { T, useTask } from '@threlte/core'
	import { OrbitControls } from '@threlte/extras'
	import { Sky } from '@threlte/extras'
	import PC from './pc.svelte'

	let rotation = 0
	useTask((delta) => {
		rotation += delta / 5
	})
</script>

<Sky elevation={1.45} rayleigh={3} exposure={0.3} turbidity={10} azimuth={0} />

<T.PerspectiveCamera
  makeDefault
	position={[-25, 2, 55]}
	fov={50}
	>
  <OrbitControls
		enableDamping
		autoRotate={false}
		minDistance={40}
		maxDistance={100}
	/>
</T.PerspectiveCamera>

<PC rotation.y={rotation} />