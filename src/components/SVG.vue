<template>
    <svg :width="square ? square : width"
         :height="square ? square : height"
         :class="classes"
         :fill="fill"
         xmlns="http://www.w3.org/2000/svg"
         xmlns:xlink="http://www.w3.org/1999/xlink"
    >
        <use :xlink:href="'#' + name"></use>
    </svg>
</template>

<script>
    export default {
        name: "vue-svg",

        props: {
            name: {
                type: String,
                defautl: '',
                required: true
            },
            width: {
                type: String,
                defautl: '16',
                // required: () => !this.square
            },
            height: {
                type: String,
                defautl: '16',
                // required: () => !this.square
            },
            classes: {
                type: String,
                default: ''
            },
            square: {
                type: String,
                defautl: null
            },
            fill: {
                type: String,
                defautl: '#000000'
            },
            color: {
                type: String,
                defautl: '#000000'
            }
        }
    }
</script>