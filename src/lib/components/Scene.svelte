<script>
  import { T, useTask } from '@threlte/core'
  import { OrbitControls } from '@threlte/extras'
	import { useGltf } from '@threlte/extras'

	let rotation = 0
  useTask((delta) => {
    rotation += delta/10
  })
</script>

<T.PerspectiveCamera
  makeDefault
	position.x={-20}
	position.y={20}
	position.z={80}
	>
  <OrbitControls enableDamping />
</T.PerspectiveCamera>

<T.DirectionalLight color="white" intensity={5} position={[10, 20, 20]}/>
<T.AmbientLight color="gainsboro" intensity={2}/>

{#await useGltf('/pc.glb') then gltf}
  <T is={gltf.scene}
		position={[0, 0, 0]}
		castShadow
		receiveShadow
		rotation.y={rotation}
	/>
{/await}
