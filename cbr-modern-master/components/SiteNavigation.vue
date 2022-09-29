<!-- this component can hold site navigation -->
<!-- if we put it here we can avoid having to repeat the code -->
<template>
	<nav>
  <NuxtLink to="/">
      Home
    </NuxtLink>
    <NuxtLink to="/about">
      About
    </NuxtLink>
    <NuxtLink to="/events2">
      Events
    </NuxtLink>
		<NuxtLink to="/buildings">
      Buildings
    </NuxtLink>
    <NuxtLink to="/videos">
      Videos
    </NuxtLink>
    <NuxtLink to="/links">
      Links
    </NuxtLink>
    <NuxtLink to="/partners">
      Partners
    </NuxtLink>
	</nav>
</template>

<script>
import NuxtLogo from './NuxtLogo.vue';

</script>