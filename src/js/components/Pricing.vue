<template>
    <div class="d-flex flex-column">

        <div class="px-gutter">
            <div class="mb-3 row justify-content-between">
                <div class="col-5 p-0">
                    <div class="option-block active w-100">
                        <p class="text-size-14">${{ monthly }}/mo</p>
                        <p class="text-size-10">{{ months }} Monthly payments</p>
                    </div>
                </div>
                <div class="col-5 p-0">
                    <div class="option-block">
                        <p class="text-size-14">${{ basePrice }}</p>
                        <p class="text-size-10">Retail price</p>
                    </div>
                </div>
            </div>
        </div>

        <p class="text-size-10">$0 Down (for qualified customers) {{ monthly }}/mo for {{ months }} months; 0% APR Retail Price: ${{ basePrice }}</p>

    </div>
</template>

<script>

import _ from 'lodash'

export default {
  name: "Pricing",
  props: {
      basePrice: {
          required: true
      },
      months: {
          default: 24
      }
  },
  data: () => ({

  }),
  computed: {
      monthly() {
          let monthly = parseFloat(this.basePrice) / parseFloat(this.months)

          return monthly.toFixed(2)
      }
  }
}

</script>
