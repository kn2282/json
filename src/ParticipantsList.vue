<template>
  <div>
    <ol>
        <li v-for="person in list">
            <!-- bindings -->
        </li>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list']
  };
</script>

