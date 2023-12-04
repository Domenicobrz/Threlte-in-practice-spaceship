<script>
	import { T } from '@threlte/core';
	import { ContactShadows, Float, Grid, OrbitControls } from '@threlte/extras';
	import Spaceship from './models/spaceship.svelte';
</script>

<T.PerspectiveCamera makeDefault position={[-5, 6, 10]} fov={25}>
	<OrbitControls enableDamping target={[0, 0, 0]} />
</T.PerspectiveCamera>

<T.DirectionalLight intensity={1.8} position={[0, 10, 0]} castShadow shadow.bias={-0.0001} />
<T.AmbientLight intensity={0.2} />

<Grid
	position.y={-0.001}
	cellColor="#ffffff"
	sectionColor="#ffffff"
	sectionThickness={0}
	fadeDistance={25}
	cellSize={2}
/>

<Spaceship />
