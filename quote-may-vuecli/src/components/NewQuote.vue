<template>
    <div class="row">
        <form action="">
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-12  form-group">
                <label for="">Quote</label>
                <textarea class="form-control" cols="1000" rows="3" v-model="quote"></textarea>
            </div>    
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <button class="btn btn-primary" type="submit" @click.prevent="createNew">Add Quote</button>
            </div>     
        </form>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            quote:''
        };
    },
    methods : {
        createNew () {
            //it emit to parent
            this.$emit('quoteAdded', this.quote);
            this.quote = '';
        }
    }
}
</script>

<style>

</style>


