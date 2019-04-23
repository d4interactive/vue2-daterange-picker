<template>
    <div class="ranges">
        <ul v-if="ranges">
            <li
                    v-for="(value, key) in ranges"
                    @click="$emit('clickRange', value, key,$event)"
                    :data-range-key="key"
                    :key="key"
                    :class="{active: key === label}"
            >{{key}}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: ['ranges', 'label']
    }
</script>
