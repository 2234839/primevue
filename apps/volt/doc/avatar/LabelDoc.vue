<template>
    <DocSectionText v-bind="$attrs">
        <p>A letter Avatar is defined with the <i>label</i> property.</p>
    </DocSectionText>
    <div class="card">
        <div class="flex flex-wrap gap-8">
            <div class="flex-auto">
                <h5>Label</h5>
                <Avatar label="P" class="mr-2" size="xlarge" />
                <Avatar label="V" class="mr-2" size="large" style="background-color: #ece9fc; color: #2a1261" />
                <Avatar label="U" class="mr-2" style="background-color: #dee9fc; color: #1a2551" />
            </div>

            <div class="flex-auto">
                <h5>Circle</h5>
                <Avatar label="P" class="mr-2" size="xlarge" shape="circle" />
                <Avatar label="V" class="mr-2" size="large" style="background-color: #ece9fc; color: #2a1261" shape="circle" />
                <Avatar label="U" class="mr-2" style="background-color: #dee9fc; color: #1a2551" shape="circle" />
            </div>

            <div class="flex-auto">
                <h5>Badge</h5>
                <OverlayBadge value="4" severity="danger">
                    <Avatar label="U" size="xlarge" />
                </OverlayBadge>
            </div>
        </div>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Avatar from '@/volt/Avatar.vue';
import OverlayBadge from '@/volt/OverlayBadge.vue';
import { ref } from 'vue';

const code = ref(`
<template>
    <div class="card">
        <div class="flex flex-wrap gap-8">
            <div class="flex-auto">
                <h5>Label</h5>
                <Avatar label="P" class="mr-2" size="xlarge" />
                <Avatar label="V" class="mr-2" size="large" style="background-color: #ece9fc; color: #2a1261" />
                <Avatar label="U" class="mr-2" style="background-color: #dee9fc; color: #1a2551" />
            </div>

            <div class="flex-auto">
                <h5>Circle</h5>
                <Avatar label="P" class="mr-2" size="xlarge" shape="circle" />
                <Avatar label="V" class="mr-2" size="large" style="background-color: #ece9fc; color: #2a1261" shape="circle" />
                <Avatar label="U" class="mr-2" style="background-color: #dee9fc; color: #1a2551" shape="circle" />
            </div>

            <div class="flex-auto">
                <h5>Badge</h5>
                <OverlayBadge value="4" severity="danger">
                    <Avatar label="U" size="xlarge" />
                </OverlayBadge>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import Avatar from '@/volt/Avatar.vue';
import OverlayBadge from '@/volt/OverlayBadge.vue';
<\/script>
`);
</script>
