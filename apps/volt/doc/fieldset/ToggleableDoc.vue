<template>
    <DocSectionText v-bind="$attrs">
        <p>Content of the fieldset can be expanded and collapsed when <i>toggleable</i> option is enabled.</p>
    </DocSectionText>
    <div class="card">
        <Fieldset legend="Header" toggleable>
            <p class="m-0">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            </p>
        </Fieldset>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Fieldset from '@/volt/Fieldset.vue';
import { ref } from 'vue';

const code = ref(`
<template>
    <Fieldset legend="Header" toggleable>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        </p>
    </Fieldset>
</template>

<script setup lang="ts">
import Fieldset from '@/volt/Fieldset.vue';
<\/script>
`);
</script>
