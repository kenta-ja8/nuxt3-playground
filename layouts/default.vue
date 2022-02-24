<template>
    <div id="screen">
        <div id="menu-area" class="has-background-info-dark">
            <template v-for="menu of menuList">
                <div class="menu-list">
                    <NuxtLink
                        :to="menu.path"
                        class="menu-link"
                        :class="{
                            'is-active': isMenuActive(menu.path)
                        }"
                    >{{ menu.label }}</NuxtLink>
                </div>
            </template>
        </div>
        <div id="content-area" class="has-background-white-ter">
            <slot />
        </div>
    </div>
</template>

<script setup lang="ts">
const route = useRoute()
const isMenuActive = computed(() => (path) => {
    return route.path == path
})
const menuList = [
    { label: 'CSS図形', path: '/css-shape', },
    { label: '視差スクロール', path: '/parallax-scrolling', },
]
</script>

<style lang="scss">
html,
body,
#__nuxt {
    width: 100%;
    height: 100%;
}

#screen {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
}
#menu-area {
    width: 12rem;
    overflow-wrap: break-word;
    padding: 0.5rem;
}
#content-area {
    flex-grow: 1;
    width: 100%;
    height: 100%;
    overflow-y: scroll;
}
.menu-list > a {
    color: #fff;
}
</style>