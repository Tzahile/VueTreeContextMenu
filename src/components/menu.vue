<template>
    <div id="mymenu" class="mymenu">
        <ul v-if="click" tabindex="-1" v-el="right" @blur="closeMenu" :style="[{top:top}, {left:left}]">
            <li label="option1" value="remove item">
            </li>
            <li label="option2" value="new item">
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'mymenu',
        props: {
            isFolder: Boolean,
            //click: Boolean,
        },
        data: {
            top: '0px',
            left: '0px',
        }
    }
</script>