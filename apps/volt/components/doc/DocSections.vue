<template>
    <template v-for="(doc, i) of docs" :key="doc.label + '_' + i">
        <section class="py-6">
            <template v-if="doc.children">
                <div :id="doc.id">
                    <DocSectionText :id="doc.id" :label="doc.label">
                        <p v-if="doc.description">{{ doc.description }}</p>
                    </DocSectionText>
                </div>
                <template v-for="comp of doc.children" :key="comp.label">
                    <component :is="{ ...comp.component }" :id="comp.id" :label="comp.label" :data="comp.data" :description="comp.description" :level="2" />
                </template>
            </template>

            <template v-else-if="!doc.children && doc.component">
                <component :is="{ ...doc.component }" :id="doc.id" :label="doc.label" :data="doc.data" :description="doc.description" />
            </template>
        </section>
    </template>
</template>

<script lang="ts">
export default {
    props: ['docs']
};
</script>
