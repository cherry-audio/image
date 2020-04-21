<template>
    <panel-item :field="field">
        <div slot="value">
            <div class="w-1/3 min-h-24" v-if="field.value">
                <media class="flex items-center border border-40 bg-20" :media="field.value"></media>
            </div>
            <div v-else>-</div>
        </div>
    </panel-item>
</template>

<script>
import Media from "./Media.vue";

export default {
    props: ["resource", "resourceName", "resourceId", "field"],
    components: {
        Media
    }
};
</script>
