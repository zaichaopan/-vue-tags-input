<template>
    <v-tags-input :tags="tags"
                  @update="tags => $emit('update', tags)">
        <div class="tags-input"
             slot-scope="{tags, removeTag, inputBinding, inputEventHandlers}">
            <span class="tags-input-tag"
                  v-for="(tag, index) in tags"
                  :key="index">
                <span>{{ tag }}</span>
                <button type="button"
                        class="tags-input-remove"
                        @click="removeTag(tag)">&times;</button>
            </span>
            <input class="tags-input-text"
                   placeholder="Add tag..."
                   v-on="inputEventHandlers"
                   v-bind="inputBinding">
        </div>
    </v-tags-input>
</template>

<script>
import VTagsInput from "./v-tags-input";

export default {
    components: {
        VTagsInput
    },
    model: {
        prop: "tags",
        event: "update"
    },
    props: {
        tags: {
            type: Array,
            default: () => {
                return [];
            }
        }
    }
};
</script>

