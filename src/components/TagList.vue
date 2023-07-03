<template>
    <div>
        <h2>Tags:</h2>
        <ul>
            <li v-for="tag in tags" :key="tag">{{ tag }}</li>
        </ul>
    </div>
</template>
  
<script>
export default {
    props: {
        tags: {
            type: Array,
            required: true
        }
    }
};
</script>
  