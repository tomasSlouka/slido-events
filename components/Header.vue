<template>
    <div class='wrapper'>
        <div class='container-narrow grid col-2 auto justify-content-space-between align-items-center'>

            <nuxt-link to='/' tag='h1'>slido <span>events</span></nuxt-link>
            <nuxt-link to='/event/add' tag='button' class='button cta'>Create New Event</nuxt-link>

        </div>
    </div>
</template>

<style scoped>
.wrapper {
    box-shadow: 0 0.125rem 0.125rem rgba(0,0,0,.1);
}
.container-narrow {
    margin-top: 0px;
    margin-bottom: 0px;
}
h1 {
    color: #39ac37;
    position: relative;
    cursor: pointer;
}
h1 > span {
    position: absolute;
    top: 16px;
    left: 37px;
    color: #256c24;
    font-size: 14px;
    z-index: 1;
}
</style>
