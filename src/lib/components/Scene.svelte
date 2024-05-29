<script>
  import { T, useTask } from '@threlte/core'
  import { OrbitControls } from '@threlte/extras'
	import { useGltf } from '@threlte/extras'
</script>

<T.PerspectiveCamera
  makeDefault
	position={[-25, 25, 45]}
	fov={35}
	>
  <OrbitControls
		enableDamping
		autoRotate={true}
		minDistance={50}
		maxDistance={100}
	/>
</T.PerspectiveCamera>

<T.DirectionalLight color="white" intensity={5} position={[10, 20, 0]}/>
<T.AmbientLight color="gainsboro" intensity={2}/>

{#await useGltf('/pc.glb') then gltf}
  <T is={gltf.scene}
		position={[0, 0, 0]}
		castShadow
		receiveShadow
	/>
{/await}
