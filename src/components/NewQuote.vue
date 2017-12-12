<template>
    <div class="row">
        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3 form-group">
            <label>Quote</label>
            <textarea name="" id="" cols="30" rows="10" class="form-control" v-model="quote"></textarea>
        </div>
        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3 form-group">
            <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
        </div>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                quote: ''
            }
        },
        methods: {
            createNew () {
                this.$emit('quoteAdded', this.quote)
                this.quote = ''
            }
        }
    }
</script>

<style>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }

    .quote {
        cursor: pointer;
    }

    .quote:hover {
        background-color: #ffe2e2;
    }
</style>
