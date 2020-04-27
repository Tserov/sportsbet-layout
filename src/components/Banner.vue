<template>
    <div class="banner">
        <img :src="`/images/${backgroundImage}`">
        <div class="content">
            <h3 class="title">
                {{title}}
            </h3>
            <p>
                {{content}}
            </p>
            <button class="btn btn-accent">
                {{buttonText}}
            </button>
        </div>
    </div>
</template>
<script>
export default {
  props: ['backgroundImage', 'title', 'content', 'buttonText'],
  name: 'Banner',
};
</script>
