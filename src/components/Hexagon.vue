<template>
    <li>
        <div class="hexagon">
            <div class="content">
                <div class="icons">
                    <div class="icon" v-for="icon in icons" :key="icon.id">
                        <i :class="icon" class="fa-lg"></i>
                    </div>
                </div>
                <h3 class="title">
                    {{ title }}
                </h3>
                <div class="employer">
                    {{ employer }}
                </div>
                <div class="location">
                    {{ location }}
                </div>
            </div>
        </div>
    </li>
</template>

<script>
    export default {
        name: "Hexagon",
        components: {
        },
        props: [
            'title', 'employer', 'location', 'icons'
        ],
        data: function () {
            return {
            }
        }
    }
</script>

<style>
    .content {
        display: flex;
        flex-direction: column;
        padding-top: 45px;
        padding-bottom: 45px;
        height: 200px;
        justify-content: center;
    }

    .icons {
        display: flex;
        flex-direction: row;
        justify-content: center;
    }

    .icons .icon {
        padding-right: 5px;
        padding-left: 5px;
    }

    .employer {
        font-style: italic;
    }

    .card-title {
        box-shadow: 0 2px 6px 0 hsla(0, 0%, 0%, 0.2);
    }
</style>