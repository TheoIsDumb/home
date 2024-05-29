<script>
	import { T, useTask } from '@threlte/core'
	import { OrbitControls } from '@threlte/extras'
	import PC from './pc.svelte'

	let rotation = 0
	useTask((delta) => {
		rotation += delta / 5
	})
</script>

<T.PerspectiveCamera
  makeDefault
	position={[-25, 15, 45]}
	fov={35}
	>
  <OrbitControls
		enableDamping
		autoRotate={false}
		minDistance={40}
		maxDistance={100}
	/>
</T.PerspectiveCamera>

<T.AmbientLight color="gainsboro" intensity={2}/>

<PC rotation.y={rotation} />