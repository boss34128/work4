<template>
<div>
    <button @click="$like" class="button-a" id="blue">Like
    </button>
    <button @click="$love" class="button-a" id="pink">Love
    </button>
    <button @click="$laugh" class="button-a" id="green">Laugh
    </button>
    <button @click="$wow" class="button-a" id="yellow">Wow
    </button>
    <button @click="$sad" class="button-a" id="purple">Sad
    </button>
    <button @click="$angry" class="button-a" id="red">Angry
    </button>
</div>
</template>

<script>
export default {
    data: function () {
        return {
            like: 0,
            love: 0,
            laugh: 0,
            wow: 0,
            sad: 0,
            angry: 0,
            count: 0
        }
    },
    props: {
        lable: String
    },
    methods: {
        $like: function () {
            this.like = 1
            this.$emit('cc', this.like)
            this.$emit('bb', this.like)
        },
        $love: function () {
            this.love = 10
            this.$emit('cc', this.love)
            this.$emit('bb', this.love)
        },
        $laugh: function () {
            this.laugh = 5
            this.$emit('cc', this.laugh)
            this.$emit('bb', this.laugh)
        },
        $wow: function () {
            this.wow = 20
            this.$emit('cc', this.wow)
            this.$emit('bb', this.wow)
        },
        $sad: function () {
            this.sad = -5
            this.$emit('cc', this.sad)
            this.$emit('bb', this.sad)
        },
        $angry: function () {
            this.angry = 50
            this.$emit('cc', this.angry)
            this.$emit('bb', this.angry)
        }
    }
}
</script>

<style>
.button-a {
    background-color: rgba(100, 100, 100, 0.473);
    border: none;
    padding: 5px 5px 5px 5px;
    text-align: center;
    display: inline-block;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 10px;
    border: 0.5px solid white;
    width: 60px;
}
.button-a-font-dd {
    background-color: white;
    border: none;
    color: #636364;
    padding: 5px 5px 5px 5px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 10px;
    border: 0.5px solid #ffffff;
    width: 60px;
}
button:hover#blue {
    color: blue;
}
button:hover#pink {
    color: rgb(255, 0, 191);
}
button:hover#yellow {
    color: yellow;
}
button:hover#purple {
    color: purple;
}
button:hover#red {
    color: red;
}
button:hover#green {
    color: rgb(25, 255, 25);
}
  
</style>