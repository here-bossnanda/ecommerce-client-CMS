<template>
    <div class="col-md-12 mt-5">
        <div class="card">
            <div class="card-header">
                <h6 class="card-title">Add New Category</h6>
            </div>
            <div class="card-body">
                <category-form ref="formCategory"></category-form>
                <div class="form-group">
                    <button class="btn btn-primary btn-sm btn-block" @click.prevent="submit">
                        <i class="fa fa-save"></i> Add New
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import FormCategory from './Form'

export default {
  name: 'AddCategory',
  methods: {
    submit () {
      this.$refs.formCategory.submit()
    }
  },
  components: {
    'category-form': FormCategory
  }
}
</script>
