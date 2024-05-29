<script>
	import { T } from '@threlte/core'
	import { OrbitControls } from '@threlte/extras'
	import PC from './pc.svelte'

	import { orbitRotate } from '$lib/store'
</script>

<T.PerspectiveCamera
  makeDefault
	position={[-25, 15, 45]}
	fov={35}
	>
  <OrbitControls
		enableDamping
		autoRotate={$orbitRotate}
		minDistance={40}
		maxDistance={100}
	/>
</T.PerspectiveCamera>

<T.AmbientLight color="gainsboro" intensity={2}/>

<PC />