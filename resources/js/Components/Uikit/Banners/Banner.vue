<template>
    <div>
        <div
            v-if="show && message"
            :class="{ 'bg-indigo-500': style == 'success', 'bg-red-700': style == 'danger' }">
            <div class="max-w-screen-xl mx-auto py-2 px-3 sm:px-6 lg:px-8">
                <div class="flex items-center justify-between flex-wrap">
                    <div class="w-0 flex-1 flex items-center min-w-0">
                        <span
                            class="flex p-2 rounded-lg"
                            :class="{
                                'bg-indigo-600': style == 'success',
                                'bg-red-600': style == 'danger',
                            }">
                            <span
                                v-if="style == 'success'"
                                class="ff-check size-5 text-white"
                                aria-hidden="true"></span>

                            <span
                                v-if="style == 'danger'"
                                class="ff-warning size-5 text-white"
                                aria-hidden="true"></span>
                        </span>

                        <p class="ms-3 font-medium text-sm text-white truncate">
                            {{ message }}
                        </p>
                    </div>

                    <div class="shrink-0 sm:ms-3">
                        <button
                            type="button"
                            class="-me-1 flex p-2 rounded-md focus:outline-none sm:-me-2 transition"
                            :class="{
                                'hover:bg-indigo-600 focus:bg-indigo-600': style == 'success',
                                'hover:bg-red-600 focus:bg-red-600': style == 'danger',
                            }"
                            aria-label="Dismiss"
                            @click.prevent="show = false">
                            <span
                                class="ff-close size-5 text-white"
                                aria-hidden="true"></span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref, watchEffect } from 'vue';
import { usePage } from '@inertiajs/vue3';

const page = usePage();
const show = ref(true);
const style = ref('success');
const message = ref('');

watchEffect(async () => {
    style.value = page.props.jetstream.flash?.bannerStyle || 'success';
    message.value = page.props.jetstream.flash?.banner || '';
    show.value = true;
});
</script>
