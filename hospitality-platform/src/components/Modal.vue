<template>
  <div>
  <div class="modal-dialog modal-xl">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">Hotel</h5>
        <Button buttonType="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"/>
      </div>
      <div class="modal-body">
        <slot>

        </slot>
      </div>
    </div>
  </div>
</div>
</template>

<script>
// import Images from "@/components/Images"
import Button from "@/components/Button"

export default {
  name: 'Modal',
  components: {
    // Images,
    Button
  }
}
</script>