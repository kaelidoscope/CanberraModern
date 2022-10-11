<!-- this component can hold site navigation -->
<!-- if we put it here we can avoid having to repeat the code -->
<template>
  <nav>
    <ul>
      <li>
        <NuxtLink to="/">
          Home
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about">
          About
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/events">
          Events
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/buildings">
          Buildings
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/videos">
          Videos
        </NuxtLink>
      </li>
      <li>  
        <NuxtLink to="/links">
          Links
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/partners">
          Partners
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script>
//import NuxtLogo from './NuxtLogo.vue';

</script>
<style> 
/* route and active route will show in bold as it matches*/
a.nuxt-link-active {
  font-weight: bold;
}
/*Exact link will display in the CM blue colour style*/
a.nuxt-link-exact-active {
  color: #7187c1;
}

ul {
  list-style-type: none;
  padding: 0;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

nav {
  padding: 0 1rem;
}
a,
a:visited {
  text-decoration: none;
  color: inherit;

}
a:hover {
  color: #7187c1;
}
</style>