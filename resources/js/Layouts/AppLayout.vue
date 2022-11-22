<template>
    <div>
        <Head :title="title" />
        <div class="min-h-screen bg-gray-100">
            <Nav></Nav>

            <!-- Page Heading -->
            <header v-if="$slots.header" class="bg-gray-600 shadow">
                <div class="max-w-7xl mx-auto py-2 px-4 sm:px-6 lg:px-8">
                    <h2 class="text-white text-center leading-tight">
                        Lorem ipsum dolor sit amet.
                    </h2>
                </div>
            </header>

            <!-- Page Content -->
            <main>
                <slot />
            </main>

            <Footer></Footer>
        </div>
    </div>
</template>

<script>
    import { Head } from '@inertiajs/inertia-vue3';
    import Nav from '@/Components/Nav.vue';
    import Footer from '@/Components/Footer.vue';

    export default {
        props: {
            title: String,
        },
        components: {
            Head,
            Nav,
            Footer
        }
    }

</script>
